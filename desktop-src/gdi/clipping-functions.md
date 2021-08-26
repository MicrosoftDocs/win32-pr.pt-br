---
description: As funções a seguir são usadas com recorte.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Funções de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7e3ec1c57713a87e5367ed28427caaab663e0bcd1abfe83c4040e04a7e6d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115326"
---
# <a name="clipping-functions"></a>Funções de recorte

As funções a seguir são usadas com recorte.



| Função                                       | Descrição                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Cria uma nova região de recorte que consiste na região de recorte existente menos o retângulo especificado.                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Combina a região especificada com a região de recorte atual usando o modo especificado.                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Recupera as dimensões do retângulo delimitado mais rígido que pode ser desenhado em torno da área visível atual no dispositivo.                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Recupera um identificador que identifica a região de recorte definida pelo aplicativo atual para o contexto do dispositivo especificado.                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Recupera a metaregião atual para o contexto do dispositivo especificado.                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Copia a região de recorte do sistema de um contexto de dispositivo especificado para uma região específica.                                                                                                     |
| [**Intersectcliprect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Cria uma nova região de recorte da interseção da região de recorte atual e do retângulo especificado.                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Move a região de recorte de um contexto de dispositivo pelos deslocamentos especificados.                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Determina se o ponto especificado está dentro da região de recorte de um contexto de dispositivo.                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Determina se qualquer parte do retângulo especificado está dentro da região de recorte de um contexto de dispositivo.                                                                               |
| [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Seleciona o caminho atual como uma região de recorte para um contexto de dispositivo, combinando a nova região com qualquer região de recorte existente usando o modo especificado.                               |
| [**Selectcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Seleciona uma região como a região de recorte atual para o contexto do dispositivo especificado.                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Intersecções da região de recorte atual para o contexto do dispositivo especificado com a metaregião atual e salva a região combinada como a nova metaregião para o contexto do dispositivo especificado. |



 

 

 



