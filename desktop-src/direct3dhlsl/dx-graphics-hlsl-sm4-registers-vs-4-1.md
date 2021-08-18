---
title: Registros – vs_4_1
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de vértice versão 4 \_ 1.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0164b1d82a9d371e735177f381e2a1a97aa062aaca8c65a00d4959a32279ed11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119920"
---
# <a name="registers---vs_4_1"></a>Registros – vs \_ 4 \_ 1

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de vértice versão 4 \_ 1.

## <a name="input-registers"></a>Registros de entrada



| Registre-se      | Nome | Contagem              | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| R\#           |      | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Não               | Nenhum     | Sim          |
| x \# \[ n\]      |      | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Sim              | Nenhum     | Sim          |
| v\#           |      | 32                 | R   | 4         | Sim              | Nenhum     | Sim          |
| T\#           |      | 128                | R   | 1         | Não               | Nenhum     | Sim          |
| s\#           |      | 16                 | R   | 1         | Não               | Nenhum     | Sim          |
| cb \# \[ index\] |      | 15                 | R   | 4         | Sim(Conteúdo)    | Nenhum     | Sim          |
| índice \[ icb\]  |      | 1                  | R   | 4         | Sim(Conteúdo)    | Nenhum     | Sim          |



 

## <a name="output-registers"></a>Registros de saída



| Registre-se | Nome            | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULO     | Descartar Resultado  | N/D   | W   | N/D       | N/D              | N/D      | Não           |
| o\#      | Registro de Saída | 32    | W   | N/D       | N/D              | 4        | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




