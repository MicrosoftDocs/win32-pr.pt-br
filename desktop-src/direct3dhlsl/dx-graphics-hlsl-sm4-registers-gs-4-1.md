---
title: Registros – gs_4_1
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelas \_ versões 4 0 e 4 1 do sombreador \_ de geometria.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 262f86490e95684f0db8ce972f8fc93528cb33ed26b09989399c15ccab766205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119940"
---
# <a name="registers---gs_4_1"></a>Registros – gs \_ 4 \_ 1

Esta seção contém informações de referência para os registros de entrada e saída implementados pelas \_ versões 4 0 e 4 1 do sombreador \_ de geometria.

## <a name="input-registers"></a>Registros de entrada



| Registre-se                 | Nome | Contagem              | R/W | Dimensão        | Indexável por r\# | Padrões | Requer DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| R\#                      |      | 4096(r \# +x \# \[ n \] ) | R/W | 4                | Não               | Nenhum     | Sim          |
| x \# \[ n\]                 |      | 4096(r \# +x \# \[ n \] ) | R/W | 4                | Sim              | Nenhum     | Sim          |
| Elemento \# \[ v vtex \] \[\] |      | 32                 | R   | 4(comp) \* 6(vert) | Sim              | Nenhum     | Sim          |
| vprim                    |      | 1                  | R   | 1                | Não               | Nenhum     | Sim          |
| T\#                      |      | 128                | R   | 1                | Não               | Nenhum     | Sim          |
| s\#                      |      | 16                 | R   | 1                | Não               | Nenhum     | Sim          |
| cb \# \[ index\]            |      | 15                 | R   | 4                | Sim(Conteúdo)    | Nenhum     | Sim          |
| índice \[ icb\]             |      | 1                  | R   | 4                | Sim(Conteúdo)    | Nenhum     | Sim          |



 

## <a name="output-registers"></a>Registros de saída



| Registre-se | Nome            | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULO     | Descartar Resultado  | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| o\#      | Registro de Saída | 32    | W   | N/D       | N/D              | 4        | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




