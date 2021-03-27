---
title: Registros-gs_5_0
description: Os seguintes registros de entrada e saída são implementados no sombreador de geometria versão 5 \_ 0.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282b32dd1c8fcb327c273b0fbf3aa51bdb002c2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292692"
---
# <a name="registers---gs_5_0"></a>Registros-GS \_ 5 \_ 0

Os seguintes registros de entrada e saída são implementados no sombreador de geometria versão 5 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Contagem              | R/W | Dimensão         | Indexável por r\# | Padrões | Requer DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | R/W | 4                 | Não               | Nenhum     | Yes          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | R/W | 4                 | Sim              | Nenhum     | Yes          |
| Entrada de 32 bits (elemento de vértice de v \[ \] \[ \] )             | 32                 | R   | 4 (COMP) \* 32 (Vert) | Yes              | Nenhum     | Yes          |
| ID primitiva de entrada de 32 bits (vPrim)                 | 1                  | R   | 1                 | Não               | Nenhum     | Yes          |
| ID de instância de entrada de 32 bits (vInstanceID)            | 1                  | R   | 1                 | Não               | Nenhum     | Yes          |
| Elemento em um recurso de entrada (t \# )                | 128                | R   | 1                 | Não               | Nenhum     | Yes          |
| Amostra (s \# )                                     | 16                 | R   | 1                 | Não               | Nenhum     | Yes          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )          | 15                 | R   | 4                 | Sim (conteúdo)    | Nenhum     | Yes          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] ) | 1                  | R   | 4                 | Sim (conteúdo)    | Nenhum     | Yes          |



 

## <a name="output-registers"></a>Registros de saída



| Tipo de registro                                               | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para Ops com vários resultados) | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| Elemento de dados de vértice de saída de 32 bits (o \# )                     | 32    | W   | N/D       | N/D              | 4        | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




