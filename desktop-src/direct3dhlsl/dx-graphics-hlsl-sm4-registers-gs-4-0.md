---
title: Registros – gs_4_0
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de geometria versão 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a27cbd13cba06ebb05fe1155bc97d13debe3154da48c05cf97a31d889ba88fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513618"
---
# <a name="registers---gs_4_0"></a>Registros – gs \_ 4 \_ 0

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de geometria versão 4 \_ 0.

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

 

 




