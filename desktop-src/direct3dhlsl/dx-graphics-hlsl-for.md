---
title: Instrução for
description: Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- HLSL de instrução for
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084167"
---
# <a name="for-statement"></a>Instrução for

Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.



|                                                                                       |
|---------------------------------------------------------------------------------------|
| \[*Atributo* \] para ( *inicializador; Condiciona Iterador* ) { *bloco de instruções*;} |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*
</dt> <dd>

Um parâmetro opcional que controla como a instrução é compilada. Quando nenhum atributo for especificado, o compilador tentará primeiro emitir uma versão revertida do loop e, se isso falhar, ou se algumas operações forem mais fáceis se o loop fosse cancelado, o voltará a uma versão não lançada do loop.



| Atributo             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| não acumular (x)             | Desverta o loop até que ele pare de ser executado. Opcionalmente, pode especificar o número máximo de vezes que o loop é executado. Não compatível com o atributo **\[ loop \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Gere o código que usa o controle de fluxo para executar cada iteração do loop. Não compatível com o atributo **\[ unroll \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Reduz o tempo de compilação, mas produz otimizações menos agressivas. Se você usar esse atributo, o compilador não desrolará loops.<br/> Esse atributo afeta somente os destinos de modelo de sombreador que dão suporte a instruções de [quebra](dx-graphics-hlsl-break.md) . Esse atributo está disponível no modelo do sombreador [versus \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e no [sombreador, modelo 3](dx-graphics-hlsl-sm3.md) e posterior. Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e mais tarde, quando o compilador compila loops. O compilador simula loops por padrão para avaliar se ele pode desroll-los. Se você não quiser que o compilador desverta loops, use esse atributo para reduzir o tempo de compilação. <br/> |
| permitir \_ \_ condição UAV | Permite que uma condição de encerramento de loop de sombreador de computação seja baseada em uma leitura de UAV. O loop não deve conter intrínsecos de sincronização.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*
</dt> <dd>

O valor inicial do contador de loops.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condiciona*
</dt> <dd>

Uma [expressão](dx-graphics-hlsl-expressions.md)condicional. Se a expressão condicional for avaliada como true, o bloco de instrução será executado. O loop termina quando a expressão é avaliada como falsa.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Repeti*
</dt> <dd>

Atualize o valor do contador de loop.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*
</dt> <dd>

Uma ou mais [instruções HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Os atributos **\[ desroll \]** e **\[ loop \]** são mutuamente exclusivos e gerarão erros de compilador quando ambos forem especificados.

Os atributos de **\[ \_ \_ condição \]** **\[ \] fastopt** e Allow UAV serão ignorados se o **\[ canroll \]** for especificado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de fluxo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





