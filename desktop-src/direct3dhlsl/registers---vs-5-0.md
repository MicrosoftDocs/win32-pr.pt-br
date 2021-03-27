---
title: Registros-vs_5_0
description: Os seguintes registros de entrada e saída são implementados no sombreador de vértice versão 5 \_ 0.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1dc211f5f3dd8819577c796849dcb86012cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967046"
---
# <a name="registers---vs_5_0"></a>Registros-vs \_ 5 \_ 0

Os seguintes registros de entrada e saída são implementados no sombreador de vértice versão 5 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                      | Contagem              | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                  | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Não               | Nenhum     | Yes          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )             | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Sim              | Nenhum     | Yes          |
| entrada de 32 bits (v \# )                                 | 32                 | R   | 4         | Sim              | Nenhum     | Yes          |
| Elemento em um recurso de entrada (t \# )                 | 128                | R   | 1         | Não               | Nenhum     | Yes          |
| Amostra (s \# )                                      | 16                 | R   | 1         | Não               | Nenhum     | Yes          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )           | 15                 | R   | 4         | Sim (conteúdo)    | Nenhum     | Yes          |
| referência de ConstantBuffer de iImmediate (índice de ICB \[ \] ) | 1                  | R   | 4         | Sim (conteúdo)    | Nenhum     | Yes          |



 

## <a name="output-registers"></a>Registros de saída



| Tipo de registro                                                      | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operações com vários resultados) | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| Elemento de dados de vértice de saída de 32 bits (o \# )                            | 32    | W   | 4         | N/D              | N/D      | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




