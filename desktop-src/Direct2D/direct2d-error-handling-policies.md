---
title: Políticas de tratamento de erros Direct2D
description: 'Este tópico descreve as políticas de tratamento de erros do Direct2D. Ele contém as seguintes seções:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, tratamento de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917588"
---
# <a name="direct2d-error-handling-policies"></a>Políticas de tratamento de erros Direct2D

Este tópico descreve as políticas de tratamento de erros do Direct2D. Ele contém as seguintes seções:

-   [Uso de HRESULT](#use-of-hresult)
-   [Valor de retorno das funções em lote](#return-value-of-batched-functions)
-   [Entrada inválida](#invalid-input)
    -   [Ponteiro de saída](#output-pointer)
    -   [Parâmetro obrigatório](#required-parameter)
-   [Os RECTs de entrada NaN e inadequadamente ordenados](#nan-and-poorly-ordered-input-rects)
    -   [NaN como entrada](#nan-as-input)
    -   [Esretângulos de entrada ordenados incorretamente](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Uso de HRESULT

Se uma função não estiver em lote e puder ter uma falha de tempo de execução, ela deverá retornar **HRESULT** para indicar uma falha. Uma falha de tempo de execução é qualquer falha que não pode ser evitada em tempo de design, como memória insuficiente.

## <a name="return-value-of-batched-functions"></a>Valor de retorno das funções em lote

Funções em lote em Direct2D são as funções que são processadas como uma única unidade quando [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) é chamado. Eles são os comandos de desenho entre [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw** ou comandos em [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Para essas funções, os erros são relatados no momento em que o lote é concluído. O erro é retornado após **EndDraw** para comandos de desenho e, após **fechar** , para **GeometrySink**.

RenderTargets interromperá o desenho se um estado de erro for definido, mas um aplicativo puder chamar [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) para redefinir o estado de erro e retomar o desenho.

As funções **Get** e **set** não têm valor de retorno. No entanto, se uma função **set** tiver uma entrada inválida, a camada de depuração gerará uma mensagem. Nesse caso, nenhum estado de erro é definido e a função **set** não faz nada.

## <a name="invalid-input"></a>Entrada inválida

Direct2D faz referência a ponteiros de saída e parâmetros obrigatórios que resultam em violações de acesso quando os ponteiros são inválidos ou **nulos**.

### <a name="output-pointer"></a>Ponteiro de saída

Direct2D desreferencia um ponteiro de saída e o atribui a **NULL** imediatamente ao inserir a função. Isso causará uma violação de acesso se um chamador passar em **NULL** como o ponteiro para o valor de retorno. Essa política também se aplica a matrizes de ponteiros. Para outros parâmetros de saída, como uma struct, a desreferência acontece mais tarde e também resulta em uma violação de acesso. No entanto, há alguns métodos que têm ponteiros de saída opcionais (isto é, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) que não causarão uma violação de acesso.

### <a name="required-parameter"></a>Parâmetro obrigatório

Se **NULL** for passado para qualquer função que exija um valor válido, a função desreferenciará o ponteiro insatisfatório no início, resultando em uma violação de acesso. Para parâmetros de entrada opcionais, **NULL** é um valor válido que resulta em algum padrão razoável.

## <a name="nan-and-poorly-ordered-input-rects"></a>Os RECTs de entrada NaN e inadequadamente ordenados

Em Direct2D, NaN é considerada uma entrada válida e os RETÂNGULOs de entrada ordenados inadequadamente são classificados.

### <a name="nan-as-input"></a>NaN como entrada

NaN é considerado uma entrada válida, embora normalmente resulte na primitiva que contém o NaN não Drawing. A API Direct2D não fornece filtragem explícita de NaN para validar a entrada.

### <a name="poorly-ordered-input-rects"></a>Esretângulos de entrada ordenados incorretamente

Os RETÂNGULOs de entrada ordenados incorretamente são classificados de forma que os cantos superior, esquerdo e inferior sejam corretamente especificados. Para saída, retângulos vazios têm a seguinte aparência: {Infinity, Infinity, FloatMax, FloatMax}.

 

 