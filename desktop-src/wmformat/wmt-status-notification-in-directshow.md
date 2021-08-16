---
title: WMT_STATUS notificação de eventos no DirectShow
description: '\_Notificação de eventos de status WMT no DirectShow'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows SDK do formato de mídia, WMT_STATUS notificações de eventos no DirectShow
- Windows SDK de formato de mídia, notificações de eventos
- Windows SDK do formato de mídia, DirectShow
- ASF (Advanced Systems Format), WMT_STATUS notificações de eventos no DirectShow
- ASF (formato de sistemas avançados), WMT_STATUS notificações de eventos no DirectShow
- ASF (Advanced Systems Format), notificações de eventos
- ASF (formato de sistemas avançados), notificações de eventos
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, notificações de eventos
- DirectShow, WMT_STATUS notificações de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4bbe430f16872baf94a0d47417381bc8bcd23d5c9fbbdb69ff2496cd873908
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089626"
---
# <a name="wmt_status-event-notification-in-directshow"></a>\_Notificação de eventos de status WMT no DirectShow

O leitor de ASF e o gravador ASF encaminham eventos de [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) para aplicativos. O gravador encaminha todos esses eventos, e o leitor encaminha apenas aqueles que pertencem à aquisição de licença do DRM. Para receber essas notificações de eventos em seu aplicativo, adicione um caso para **o \_ \_ evento WMT do EC** em sua função de manipulação de eventos. O parâmetro *lParam1* associado ao evento contém o código **de \_ status WMT** (que pode ser **WMT \_ erro**) e lParam2 contém os [**\_ dados de \_ evento \_ am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que incluem o **HRESULT**.

 

 