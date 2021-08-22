---
title: texm3x2pad – ps
description: Executa a multiplicação da primeira linha de uma multiplicação de matriz de duas linhas. Essa instrução deve ser combinada com texm3x2tex - ps ou texm3x2depth - ps. Consulte qualquer uma dessas instruções para obter detalhes sobre como usar o texmpad.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55943d2a62f49e6bdb45d893385f0824898d665ee4a4065c4f8c8ed75c2f8249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485436"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad – ps

Executa a multiplicação da primeira linha de uma multiplicação de matriz de duas linhas. Essa instrução deve ser combinada [com texm3x2tex - ps](texm3x2tex---ps.md) ou [texm3x2depth - ps](texm3x2depth---ps.md). Consulte qualquer uma dessas instruções para obter detalhes sobre como usar o texmpad.

## <a name="syntax"></a>Syntax



| tex3x2pad dst, src |
|--------------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução não pode ser usada por si só.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




