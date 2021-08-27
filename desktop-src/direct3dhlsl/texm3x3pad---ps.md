---
title: texm3x3pad-PS
description: Executa a primeira ou segunda linha multiplicada por uma multiplicação de três linhas. Essa instrução deve ser usada em combinação com texm3x3-PS, texm3x3spec-PS, texm3x3vspec-PS ou texm3x3tex-PS.
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10e473b30417d6797ffe227eff11b0d5d607264560bfd8506b76f333e0275cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787702"
---
# <a name="texm3x3pad---ps"></a>texm3x3pad-PS

Executa a primeira ou segunda linha multiplicada por uma multiplicação de três linhas. Essa instrução deve ser usada em combinação com [texm3x3-PS](texm3x3---ps.md), [texm3x3spec-PS](texm3x3spec---ps.md), [texm3x3vspec-PS](texm3x3vspec---ps.md)ou [texm3x3tex-PS](texm3x3tex---ps.md).

## <a name="syntax"></a>Syntax



| texm3x3pad DST, src |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3pad            | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução não pode ser usada por si só.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




