---
title: Acessando e controlando dados do quadro DWM
description: Este tópico discute as APIs do Gerenciador de Janelas da Área de Trabalho (DWM) que são usadas para agendamento e apresentação de mídia.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), agendamento e APIs de apresentação de mídia
- DWM (Gerenciador de Janelas da Área de Trabalho), agendamento e APIs de apresentação de mídia
- agendamento e APIs de apresentação de mídia
- Gerenciador de Janelas da Área de Trabalho (DWM), acessando dados de quadro
- DWM (Gerenciador de Janelas da Área de Trabalho), acessando dados de quadro
- Acessando dados de quadro
- Gerenciador de Janelas da Área de Trabalho (DWM), controlando dados de quadro
- DWM (Gerenciador de Janelas da Área de Trabalho), controlando dados de quadro
- controlando dados de quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292259"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a>Acessando e controlando dados do quadro DWM

Este tópico discute as APIs do Gerenciador de Janelas da Área de Trabalho (DWM) que são usadas para agendamento e apresentação de mídia.

## <a name="dwm-frame-timing-api"></a>API de temporização de quadro DWM

As APIs de apresentação de agendamento e mídia permitem um controle mais detalhado de quando a imagem da área de trabalho é composta e apresentada. Normalmente, isso é necessário para aplicativos de reprodução de mídia e vídeo para os quais o DWM está sendo executado de forma assíncrona com sua própria agenda de apresentação, o que pode levar a artefatos de amostragem se não estiver rigidamente controlado.

As funções agendamento e apresentação de mídia incluem o seguinte. Os detalhes de seu uso são encontrados nessas páginas.

-   [**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss). Notifica o DWM para habilitar o agendamento do serviço de agendamento de classe de multimídia (MMCSS) enquanto o processo de chamada está ativo.
-   [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo). Recupera as informações de tempo de composição atuais.
-   [**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration). Altera o número de atualizações durante as quais o quadro anterior será exibido.
-   [**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration). Define o número de atualizações para exibir o quadro apresentado.
-   [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters). Define os parâmetros atuais para composição de quadros.

 

 




