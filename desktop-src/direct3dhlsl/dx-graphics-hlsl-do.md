---
title: Instrução do (Ocidl. h)
description: Execute uma série de instruções continuamente até que a expressão condicional falhe.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- HLSL da instrução
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172991"
---
# <a name="do-statement"></a>Instrução do

Execute uma série de instruções continuamente até que a expressão condicional falhe.



|                                                                     |
|---------------------------------------------------------------------|
| \[*Atributo* \] { *Statement Block*;} while ( *condicional* ); |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*
</dt> <dd>

Um parâmetro opcional que controla como a instrução é compilada.



| Atributo | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Reduz o tempo de compilação, mas produz otimizações menos agressivas. Se você usar esse atributo, o compilador não desrolará loops.<br/> Esse atributo afeta somente os destinos de modelo de sombreador que dão suporte a instruções de [quebra](dx-graphics-hlsl-break.md) . Esse atributo está disponível no modelo do sombreador [versus \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e no [sombreador, modelo 3](dx-graphics-hlsl-sm3.md) e posterior. Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e mais tarde, quando o compilador compila loops. O compilador simula loops por padrão para avaliar se ele pode desroll-los. Se você não quiser que o compilador desverta loops, use esse atributo para reduzir o tempo de compilação.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*
</dt> <dd>

Uma ou mais [instruções](dx-graphics-hlsl-statement-blocks.md).

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condiciona*
</dt> <dd>

Uma [expressão](dx-graphics-hlsl-expressions.md)condicional. O bloco de instrução é executado antes da expressão ser avaliada. O loop é encerrado quando a expressão é avaliada como false.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de fluxo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





