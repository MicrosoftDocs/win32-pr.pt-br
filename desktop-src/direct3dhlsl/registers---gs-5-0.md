---
title: Registros-gs_5_0
description: Os seguintes registros de entrada e saída são implementados no sombreador de geometria versão 5 \_ 0.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e0bac8baf9be8428b53fa7949229361edf04132079a7a6ca6989dab92c44aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023496"
---
# <a name="registers---gs_5_0"></a>Registros-GS \_ 5 \_ 0

Os seguintes registros de entrada e saída são implementados no sombreador de geometria versão 5 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Contagem              | R/W | Dimensão         | Indexável por r\# | Padrões | Requer DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | R/W | 4                 | Não               | Nenhum     | Sim          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | R/W | 4                 | Sim              | Nenhum     | Sim          |
| Entrada de 32 bits (elemento de vértice de v \[ \] \[ \] )             | 32                 | R   | 4 (COMP) \* 32 (Vert) | Sim              | Nenhum     | Sim          |
| ID primitiva de entrada de 32 bits (vPrim)                 | 1                  | R   | 1                 | Não               | Nenhum     | Sim          |
| ID de instância de entrada de 32 bits (vInstanceID)            | 1                  | R   | 1                 | Não               | Nenhum     | Sim          |
| Elemento em um recurso de entrada (t \# )                | 128                | R   | 1                 | Não               | Nenhum     | Sim          |
| Amostra (s \# )                                     | 16                 | R   | 1                 | Não               | Nenhum     | Sim          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )          | 15                 | R   | 4                 | Sim (conteúdo)    | Nenhum     | Sim          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] ) | 1                  | R   | 4                 | Sim (conteúdo)    | Nenhum     | Sim          |



 

## <a name="output-registers"></a>Registros de saída



| Tipo de registro                                               | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para Ops com vários resultados) | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| Elemento de dados de vértice de saída de 32 bits (o \# )                     | 32    | W   | N/D       | N/D              | 4        | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




