---
title: label - ps
description: Marque a próxima instrução como tendo um índice de rótulo. | label - ps
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 921abbc0518182eaef17326082a395e5c5729d8ab550610fe71c8dfabe46dd4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854196"
---
# <a name="label---ps"></a>label - ps

Marque a próxima instrução como tendo um índice de rótulo.

## <a name="syntax"></a>Syntax



| label l\# |
|-----------|



 

em \# que identifica o número do rótulo.

Para ps \_ 2 \_ x, o número do rótulo deve estar entre 0 e 15.

Para ps \_ 2 \_ sw, ps 3 0 e ps 3 sw, o número do rótulo deve estar entre 0 e \_ \_ \_ \_ 2047.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução define um rótulo localizado na próxima instrução do sombreador. A instrução de rótulo só pode estar presente diretamente após uma instrução [ret](ret---ps.md) (que define o final da sub-rotina anterior ou programa principal).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




