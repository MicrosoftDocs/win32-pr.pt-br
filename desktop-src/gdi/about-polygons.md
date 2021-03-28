---
description: Um polígono é uma forma preenchida com lados retos.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Sobre polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010741"
---
# <a name="about-polygons"></a>Sobre polígonos

Um *polígono* é uma forma preenchida com lados retos. Os lados de um polígono são desenhados usando a caneta atual. Quando o sistema preenche um polígono, ele usa o pincel atual e o modo de preenchimento do polígono atual. Os dois modos de preenchimento, alternativo (o padrão) e o enrolamento, determinam se as regiões em um polígono complexo são preenchidas ou deixadas como não pintadas. Um aplicativo pode selecionar um dos modos chamando a função [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Para obter mais informações sobre os modos de preenchimento de polígono, consulte [regiões](regions.md).

A ilustração a seguir mostra um polígono desenhado usando o [**polígono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).

![ilustração de um polígono na forma de uma estrela de cinco pontas](images/csfsh-04.png)

Além de desenhar um único polígono usando [**polígono**](/windows/win32/api/wingdi/nf-wingdi-polygon), um aplicativo pode desenhar vários polígonos usando a função [**polipolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .

 

 
