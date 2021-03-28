---
title: DSX-PS
description: Calcule a taxa de alteração na direção x do destino de renderização.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916883"
---
# <a name="dsx---ps"></a>DSX-PS

Calcule a taxa de alteração na direção x do destino de renderização.

## <a name="syntax"></a>Syntax



| DSX DST, src |
|--------------|



 

Em que:

-   o DST é um registro de destino.
-   src é um registro de fonte de entrada.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dsx                   |      |      |      |      |      | x    | x     | x    | x     |



 

A taxa de alterações computadas do registro de origem é uma aproximação no conteúdo do mesmo registro em pixels adjacentes que executam o sombreador de pixel na etapa de bloqueio com o pixel atual.

As instruções DSX e [DSY](dsy---ps.md) calculam o resultado examinando o conteúdo atual do registro de origem (por componente) para os vários pixels na área local em execução na etapa de bloqueio. A fórmula exata usada para computar o gradiente varia de acordo com o hardware, mas deve ser consistente com a maneira como o hardware faz as mesmas operações como parte do processo de cálculo de nível de detalhe para amostragem de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




