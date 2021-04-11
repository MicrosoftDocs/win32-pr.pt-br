---
title: Especificando formatos de hora
description: Especificando formatos de hora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- Macro MCIWndGetTimeFormat
- Macro MCIWndSetTimeFormat
- Macro MCIWndUseTime
- Macro MCIWndUseFrames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292204"
---
# <a name="specifying-time-formats"></a>Especificando formatos de hora

Os tipos de dados de multimídia normalmente podem usar o tempo para identificar posições significativas em seu conteúdo. Formatos de tempo comuns são milissegundos, faixas e quadros; outros formatos de tempo menos comuns, como SMPTE (sociedade de imagem de movimento e engenheiros de televisão) 24, também existem. A hora é o formato e o sistema de referência para a forma de onda-áudio, MIDI e dados de áudio de CD. O vídeo dá suporte ao tempo, embora seja registrado como uma sequência de quadros (fluxo) que normalmente é reproduzido em uma velocidade específica. Várias macros estão disponíveis para o formato de hora de design.

Você pode recuperar o formato de hora atual para um arquivo ou dispositivo usando a macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) . Você pode alterar o formato de hora atual para qualquer outro formato de hora com suporte de um dispositivo usando a macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) . Ou você pode definir o formato de hora como milissegundos ou quadros usando as macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) ou [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .

> [!Note]  
> Formatos não contínuos, como trilhas e SMPTE, podem fazer com que a barra de ferramentas se comporte incorretamente. Para esses formatos de tempo, talvez você queira desativar a barra de ferramentas especificando o \_ estilo de janela MCIWNDF NOPLAYBAR ao criar uma janela MCIWnd.

 

 

 




