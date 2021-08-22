---
title: Direct2D Políticas de tratamento de erro
description: 'Este tópico descreve as políticas de Direct2D de tratamento de erro. Ele contém as seguintes seções:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, tratamento de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3be48c5d80cbbd971f63392efaf6b902ff6187e0a2687df25ccc728efafbfab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318026"
---
# <a name="direct2d-error-handling-policies"></a>Direct2D Políticas de tratamento de erro

Este tópico descreve as políticas de Direct2D de tratamento de erro. Ele contém as seguintes seções:

-   [Uso de HRESULT](#use-of-hresult)
-   [Valor de retorno de funções em lote](#return-value-of-batched-functions)
-   [Entrada inválida](#invalid-input)
    -   [Ponteiro de saída](#output-pointer)
    -   [Parâmetro obrigatório](#required-parameter)
-   [RECTs de entrada naN e mal ordenados](#nan-and-poorly-ordered-input-rects)
    -   [NaN como entrada](#nan-as-input)
    -   [RECTs de entrada mal ordenados](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Uso de HRESULT

Se uma função não for em lote e puder ter uma falha em tempo de executar, ela deverá retornar **HRESULT** para indicar uma falha. Uma falha em tempo de run time é qualquer falha que não pode ser evitada em tempo de design, como falta de memória.

## <a name="return-value-of-batched-functions"></a>Valor de retorno de funções em lote

As funções em lote Direct2D são as funções processadas como uma única unidade quando [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) é chamado. Eles são os comandos de desenho [**entre BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) **e EndDraw** ou comandos [**em GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Para essas funções, os erros são relatados no momento em que o lote é concluído. O erro é retornado após **EndDraw para** comandos de desenho e após **Fechar** para **GeometrySink.**

RenderTargets param de desenhar se um estado de erro estiver definido, mas um aplicativo pode chamar [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) para redefinir o estado de erro e retomar o desenho.

**As** funções Get **e Set** não têm nenhum valor de retorno. No entanto, se uma **função Set** tiver uma entrada inválida, a camada de depuração gerará uma mensagem. Nesse caso, nenhum estado de erro é definido e a **função Set** não faz nada.

## <a name="invalid-input"></a>Entrada inválida

Direct2D desreferências ponteiros de saída e parâmetros necessários que resultam em violações de acesso quando os ponteiros são inválidos ou **NULL.**

### <a name="output-pointer"></a>Ponteiro de saída

Direct2D desreferencia um ponteiro de saída e o atribui a **NULL** imediatamente após a inserção da função. Isso causará uma violação de acesso se um chamador passar **NULL** como o ponteiro para o valor de retorno. Essa política também se aplica a matrizes de ponteiros. Para outros parâmetros de saída, como um struct, a desreferência ocorre mais tarde e também resulta em uma violação de acesso. No entanto, há alguns métodos que têm ponteiros de saída opcionais (ou seja, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) que não causarão uma violação de acesso.

### <a name="required-parameter"></a>Parâmetro obrigatório

Se **NULL** for passado para qualquer função que exija um valor válido, a função desreferencia o ponteiro ruim no início, resultando em uma violação de acesso. Para parâmetros de entrada opcionais, **NULL** é um valor válido que resulta em algum padrão razoável.

## <a name="nan-and-poorly-ordered-input-rects"></a>RECTs de entrada naN e mal ordenados

No Direct2D, NaN é considerado uma entrada válida e RECTs de entrada mal ordenadas são classificação.

### <a name="nan-as-input"></a>NaN como entrada

O NaN é considerado uma entrada válida, embora normalmente resulta no primitivo que contém o não desenho naN. A API Direct2D não fornece filtragem explícita de NaN para validar a entrada.

### <a name="poorly-ordered-input-rects"></a>RECTs de entrada mal ordenados

RECTs de entrada mal ordenados são classificação para que os cantos superior, esquerdo e inferior direito sejam especificados corretamente. Para saída, retângulos vazios são assim: {Infinity, Infinity, FloatMax, FloatMax}.

 

 