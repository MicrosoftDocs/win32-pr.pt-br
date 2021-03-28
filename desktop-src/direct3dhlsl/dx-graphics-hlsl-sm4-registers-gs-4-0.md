---
title: Registros-gs_4_0
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo Geometry shader versão 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498718"
---
# <a name="registers---gs_4_0"></a>Registros-GS \_ 4 \_ 0

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo Geometry shader versão 4 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Registre-se                 | Name | Contagem              | R/W | Dimensão        | Indexável por r\# | Padrões | Requer DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| d\#                      |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4                | Não               | Nenhum     | Yes          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4                | Sim              | Nenhum     | Yes          |
| \# \[ elemento de vértice \] \[ v\] |      | 32                 | R   | 4 (comp.) \* 6 (Vert) | Yes              | Nenhum     | Yes          |
| vprim                    |      | 1                  | R   | 1                | Não               | Nenhum     | Yes          |
| t\#                      |      | 128                | R   | 1                | Não               | Nenhum     | Yes          |
| s\#                      |      | 16                 | R   | 1                | Não               | Nenhum     | Yes          |
| \# \[ índice CB\]            |      | 15                 | R   | 4                | Sim (conteúdo)    | Nenhum     | Yes          |
| índice de ICB \[\]             |      | 1                  | R   | 4                | Sim (conteúdo)    | Nenhum     | Yes          |



 

## <a name="output-registers"></a>Registros de saída



| Registre-se | Name            | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULO     | Descartar resultado  | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| minúscula\#      | Registro de saída | 32    | W   | N/D       | N/D              | 4        | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




