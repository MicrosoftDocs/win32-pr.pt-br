---
title: Registros-cs_5_0
description: Os seguintes registros de entrada e saída são implementados no sombreador de computação versão 5 \_ 0.
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01d761fba2b126559e18caf7cf917482d83fec952798b80c3ffc756a5bf3418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023576"
---
# <a name="registers---cs_5_0"></a>Registros-cs \_ 5 \_ 0

Os seguintes registros de entrada e saída são implementados no sombreador de computação versão 5 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                        | Contagem                                                  | R/W | Dimensão                        | Indexável por r\# | Padrões | Requer DCL |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                    | 4096 (r \# + x \# \[ n \] )                                     | R/W | 4                                | Não               | Nenhum     | Sim          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )               | 4096 (r \# + x \# \[ n \] )                                     | R/W | 4                                | Sim              | Nenhum     | Sim          |
| Memória compartilhada do grupo de threads de 32 bits (g \# \[ n \] )         | 8192 (soma de todos os decls de memória compartilhada para o grupo de threads) | R/W | 1 (pode ser declarada várias maneiras) | Sim              | Nenhum     | Sim          |
| Elemento em um recurso de entrada (t \# )                   | 128                                                    | R   | 1                                | Não               | Nenhum     | Sim          |
| Amostra (s \# )                                        | 16                                                     | R   | 1                                | Não               | Nenhum     | Sim          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )             | 15                                                     | R   | 4                                | Sim (conteúdo)   | Nenhum     | Sim          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] )    | 1                                                      | R   | 4                                | Sim (conteúdo)    | Nenhum     | Sim          |
| ThreadID (vThreadID.xyz)                             | 1                                                      | R   | 3                                | Não               | N/D      | Sim          |
| ThreadGroupID (vThreadGroupID.xyz)                   | 1                                                      | R   | 3                                | Não               | N/D      | Sim          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)               | 1                                                      | R   | 3                                | Não               | N/D      | Sim          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened) | 1                                                      | R   | 1                                | Não               | N/D      | Sim          |



 

## <a name="output-registers"></a>Registros de saída



| Tipo de registro                                               | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para Ops com vários resultados) | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| Modo de exibição de acesso não ordenado (u \# )                                 | 8     | R/W | 1         | Não               | Não       | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




