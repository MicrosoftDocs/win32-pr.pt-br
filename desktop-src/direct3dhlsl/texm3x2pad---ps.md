---
title: texm3x2pad-PS
description: Executa a primeira multiplicação de linha de uma multiplicação de duas linhas. Essa instrução deve ser combinada com texm3x2tex-PS ou texm3x2depth-PS. Consulte uma destas instruções para obter detalhes sobre como usar o texmpad.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823454"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad-PS

Executa a primeira multiplicação de linha de uma multiplicação de duas linhas. Essa instrução deve ser combinada com [texm3x2tex-PS](texm3x2tex---ps.md) ou [texm3x2depth-PS](texm3x2depth---ps.md). Consulte uma destas instruções para obter detalhes sobre como usar o texmpad.

## <a name="syntax"></a>Syntax



| tex3x2pad DST, src |
|--------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução não pode ser usada por si só.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




