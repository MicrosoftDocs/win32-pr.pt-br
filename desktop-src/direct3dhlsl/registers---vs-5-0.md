---
title: Registros-vs_5_0
description: Os seguintes registros de entrada e saída são implementados no sombreador de vértice versão 5 \_ 0.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9c80125a4640e558872e29e435d48e7420bbd6c504577a5e0c84781f8a47d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853896"
---
# <a name="registers---vs_5_0"></a>Registros-vs \_ 5 \_ 0

Os seguintes registros de entrada e saída são implementados no sombreador de vértice versão 5 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                      | Contagem              | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                  | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Não               | Nenhum     | Sim          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )             | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Sim              | Nenhum     | Sim          |
| entrada de 32 bits (v \# )                                 | 32                 | R   | 4         | Sim              | Nenhum     | Sim          |
| Elemento em um recurso de entrada (t \# )                 | 128                | R   | 1         | Não               | Nenhum     | Sim          |
| Amostra (s \# )                                      | 16                 | R   | 1         | Não               | Nenhum     | Sim          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )           | 15                 | R   | 4         | Sim (conteúdo)    | Nenhum     | Sim          |
| referência de ConstantBuffer de iImmediate (índice de ICB \[ \] ) | 1                  | R   | 4         | Sim (conteúdo)    | Nenhum     | Sim          |



 

## <a name="output-registers"></a>Registros de saída



| Tipo de registro                                                      | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operações com vários resultados) | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| Elemento de dados de vértice de saída de 32 bits (o \# )                            | 32    | W   | 4         | N/D              | N/D      | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




