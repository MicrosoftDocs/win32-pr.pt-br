---
title: Instrução for
description: Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- para instrução HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cbcf06f28a327e18aa9f31b417dc1911411d0c9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119072"
---
# <a name="for-statement"></a>Instrução for

Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.

\[*Atributo* \] para ( *Inicializador; Condicional; Iterador* ) { *Bloco de instrução*; }



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Um parâmetro opcional que controla como a instrução é compilada. Quando nenhum atributo for especificado, o compilador tentará primeiro emitir uma versão rolada do loop e, se isso falhar, ou se algumas operações serão mais fáceis se o loop tiver sido desenrolado, retornará para uma versão não listada do loop.



| Atributo             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Unroll the loop until it stops executing. Opcionalmente, pode especificar o número máximo de vezes que o loop deve ser executado. Não compatível com o **\[ atributo loop. \]**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Gere o código que usa o controle de fluxo para executar cada iteração do loop. Não compatível com o **\[ atributo unroll. \]**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Reduz o tempo de compilação, mas produz otimizações menos agressivas. Se você usar esse atributo, o compilador não desenrola os loops.<br/> Esse atributo afeta apenas destinos de modelo de sombreador que suportam instruções [de quebra.](dx-graphics-hlsl-break.md) Esse atributo está disponível no modelo de sombreador [ \_ versus 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) e posterior. Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e posterior quando o compilador compila loops. O compilador simula loops por padrão para avaliar se ele pode unroll-los. Se você não quiser que o compilador unroll loops, use esse atributo para reduzir o tempo de compilação. <br/> |
| permitir \_ condição \_ uav | Permite que uma condição de encerramento de loop do sombreador de computação seja baseada em uma leitura UAV. O loop não deve conter intrínsecos de sincronização.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*
</dt> <dd>

O valor inicial do contador de loops.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Uma expressão [condicional](dx-graphics-hlsl-expressions.md). Se a expressão condicional for avaliada como true, o bloco de instrução será executado. O loop termina quando a expressão é avaliada como false.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterador*
</dt> <dd>

Atualize o valor do contador de loop.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*
</dt> <dd>

Uma ou mais [instruções HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Os **\[ atributos \] unroll** **\[ e loop \]** são mutuamente exclusivos e gerarão erros do compilador quando ambos são especificados.

Os **\[ atributos \] de condição fastopt** e **\[ \_ allow uav \_ \]** serão ignorados se **\[ o unroll \]** for especificado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de fluxo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





