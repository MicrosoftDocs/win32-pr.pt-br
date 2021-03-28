---
title: Registros-ps_4_1
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 4 \_ 1.
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1cf70a24ad2fa7e77f7a5a90f6ec247179464f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916270"
---
# <a name="registers---ps_4_1"></a>Registros-PS \_ 4 \_ 1

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 4 \_ 1.

## <a name="input-registers"></a>Registros de entrada



| Registre-se      | Name | Contagem              | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| d\#           |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Não               | Nenhum     | Yes          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Sim              | Nenhum     | Yes          |
| l\#           |      | 32                 | R   | 4         | Sim              | Nenhum     | Yes          |
| t\#           |      | 128                | R   | 1         | Não               | Nenhum     | Yes          |
| s\#           |      | 16                 | R   | 1         | Não               | Nenhum     | Yes          |
| \# \[ índice CB\] |      | 15                 | R   | 4         | Sim (conteúdo)    | Nenhum     | Yes          |
| índice de ICB \[\]  |      | 1                  | R   | 4         | Sim (conteúdo)    | Nenhum     | Yes          |



 

## <a name="output-registers"></a>Registros de saída



| Registre-se | Name             | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULO     | Descartar resultado   | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| minúscula\#      | Registro de saída  | 8     | W   | N/D       | N/D              | 4        | Não           |
| oDepth   | Profundidade de saída     | 1     | W   | N/D       | N/D              | 1        | N/D          |
| oMask    | Máscara de MSAA de saída | 1     | W   | N/D       | N/D              | 1        | N/D          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




