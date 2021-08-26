---
title: Instrução While
description: Executa um bloco de instrução até que a expressão condicional falhe.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- Instrução while HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4e9ae7dc0d8280c9b9823d77dcfe5968243a1ddebdaf78e76b03651ee465034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983156"
---
# <a name="while-statement"></a>Instrução While

Executa um bloco de instrução até que a expressão condicional falhe.

\[*Atributo* \] while ( *Conditional* ) { *Statement Block*; }



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Um parâmetro opcional que controla como a instrução é compilada.



| Atributo             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Unroll the loop until it stops executing. Opcionalmente, você pode especificar o número máximo de vezes que o loop pode ser executado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | Use instruções de controle de fluxo no sombreador compilado; não desemrolle o loop.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Reduz o tempo de compilação, mas produz otimizações menos agressivas. Se você usar esse atributo, o compilador não desenrola os loops.<br/> Esse atributo afeta apenas destinos de modelo de sombreador que suportam instruções [de quebra.](dx-graphics-hlsl-break.md) Esse atributo está disponível no modelo de sombreador [ \_ versus 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) e posterior. Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e posterior quando o compilador compila loops. O compilador simula loops por padrão para avaliar se ele pode unroll-los. Se você não quiser que o compilador unroll loops, use esse atributo para reduzir o tempo de compilação.<br/> |
| permitir \_ condição \_ uav | Permite que uma condição de encerramento de loop do sombreador de computação seja baseada em uma leitura UAV. O loop não deve conter intrínsecos de sincronização.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Uma expressão [condicional](dx-graphics-hlsl-expressions.md). Se a expressão for avaliada como true, o bloco de instrução será executado. O loop termina quando a expressão é avaliada como false.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*
</dt> <dd>

Uma ou mais [instruções](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[Flow Controle](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





