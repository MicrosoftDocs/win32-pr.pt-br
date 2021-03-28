---
title: Registros-ps_5_0
description: Os seguintes registros de entrada e saída são implementados no sombreador de pixel versão 5 \_ 0.
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d945e06ed3ae1847e15a32da973709b8ceb241ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916578"
---
# <a name="registers---ps_5_0"></a>Registros-PS \_ 5 \_ 0

Os seguintes registros de entrada e saída são implementados no sombreador de pixel versão 5 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Contagem              | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Não               | Nenhum     | Yes          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Sim              | Nenhum     | Yes          |
| Atributo de entrada de 32 bits (v \# )                      | 32                 | R   | 4         | Sim              | Nenhum     | Yes          |
| Elemento em um recurso de entrada (t \# )                | 128                | R   | 1         | Não               | Nenhum     | Yes          |
| Amostra (s \# )                                     | 16                 | R   | 1         | Não               | Nenhum     | Yes          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )          | 15                 | R   | 4         | Sim (conteúdo)    | Nenhum     | Yes          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] ) | 1                  | R   | 4         | Sim (conteúdo)    | Nenhum     | Yes          |



 

## <a name="output-registers"></a>Registros de saída



| Tipo de registro                                                      | Contagem                   | R/W | Dimensão                                | Indexável por r\# | Padrões | Requer DCL |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operações com vários resultados) | N/D                     | W   | N/D                                      | N/D              | N/D      | Não           |
| Elemento de saída de 32 bits (o \# )                                        | 8                       | W   | 4                                        | N/D              | N/D      | Não           |
| Modo de exibição de acesso não ordenado (u \# )                                        | 8- \# de rendertargets | R/W | Componentes de registro do D3D11 \_ PS \_ cs \_ UAV \_ \_ | Não               | Não       | Sim          |
| 32-bit \[ 0,0 f.. 1.0 \] oDepth (profundidade de saída flutuante)                  | 1                       | W   | 1                                        | N/D              | N/D      | Sim          |
| máscara de exemplo de saída UINT de 32 bits (oMask)                             | 1                       | W   | 1                                        | N/D              | N/D      | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




