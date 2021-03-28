---
title: DSY-PS
description: Calcule a taxa de alteração na direção y do destino de renderização.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365207"
---
# <a name="dsy---ps"></a>DSY-PS

Calcule a taxa de alteração na direção y do destino de renderização.

## <a name="syntax"></a>Syntax



| DSY DST, src |
|--------------|



 

Em que:

-   o DST é um registro de destino.
-   src é um registro de fonte de entrada.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dsy                   |      |      |      |      |      | x    | x     | x    | x     |



 

A taxa de alterações computadas do registro de origem é uma aproximação no conteúdo do mesmo registro em pixels adjacentes que executam o sombreador de pixel na etapa de bloqueio com o pixel atual.

As instruções [DSX](dsx---ps.md) e DSY calculam o resultado examinando o conteúdo atual do registro de origem (por componente) para os vários pixels na área local em execução na etapa de bloqueio. A fórmula exata usada para computar o gradiente varia de acordo com o hardware, mas deve ser consistente com a maneira como o hardware faz as mesmas operações como parte do processo de cálculo de nível de detalhe para amostragem de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




