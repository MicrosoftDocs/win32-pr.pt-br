---
title: Registros-ds_5_0
description: Os seguintes registros de entrada e saída são implementados no sombreador de domínio versão 5 \_ 0.
ms.assetid: 8AE00EC6-0BDC-4F63-B95C-FF434B98D7CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b787f4a1f7e647a49340d49796dc2986e442178f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292693"
---
# <a name="registers---ds_5_0"></a>Registros-DS \_ 5 \_ 0

Os seguintes registros de entrada e saída são implementados no sombreador de domínio versão 5 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                              | Contagem                | R/W | Dimensão                           | Indexável por r\# | Padrões | Requer DCL |
|------------------------------------------------------------|----------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                          | 4096 (r \# + x \# \[ n \] )   | R/W | 4                                   | Não               | Nenhum     | Yes          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )                     | 4096 (r \# + x \# \[ n \] )   | R/W | 4                                   | Sim              | Nenhum     | Yes          |
| Pontos de controle de entrada de 32 bits ( \[ elemento de vértice VCP \] \[ \] )     | 32 consulte a observação 1 abaixo. | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Yes              | Nenhum     | Yes          |
| Constantes de patch de entrada de 32 bits (vértice do VPC \[ \] )               | 32 consulte a observação 2 abaixo. | R   | 4                                   | Sim              | Nenhum     | Yes          |
| local de entrada de 32 bits no domínio (vDomain. XY, vDomain.xyz)) | 1                    | R   | 3                                   | Não               | N/D      | Sim          |
| Primitivaid de entrada UINT de 32 bits (vPrim)                      | 1                    | R   | 1                                   | Não               | N/D      | Sim          |
| Elemento em um recurso de entrada (t \# )                         | 128                  | R   | 128                                 | Yes              | Nenhum     | Yes          |
| Amostra (s \# )                                              | 16                   | R   | 1                                   | Sim              | Nenhum     | Yes          |
| referência de iConstantBuffer ( \# \[ índice CB \] )                  | 15                   | R   | 4                                   | Sim              | Nenhum     | Yes          |
| referência de ConstantBuffer de iImmediate (índice de ICB \[ \] )         | 1                    | R   | 4                                   | Sim (conteúdo)    | Nenhum     | Yes          |



 

**Observação 1:** O sombreador de domínio vê as saídas do sombreador envoltória em 2 conjuntos de registros separados. Os registros VCP podem ver todos os pontos de controle de saída do sombreador envoltória. Os registros do VPC podem ver todos os dados de saída constante do patch do envoltória Shader.

**Observação 2:** Como o código para o envoltória Shader patch constante Fork ou as fases de junção geram TessFactors usando nomes como a VA \_ TessFactor, o sombreador de domínio deve corresponder a essas declarações na entrada do VPC equivalente se quiser ver esses valores.

## <a name="output-registers"></a>Registros de saída



| Tipo de registro                           | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento de dados de vértice de saída de 32 bits (o \# ) | 32    | W   | 4         | Sim              | Nenhum     | Yes          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




