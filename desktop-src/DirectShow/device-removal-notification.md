---
description: Notificação de remoção de dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notificação de remoção de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920096"
---
# <a name="device-removal-notification"></a>Notificação de remoção de dispositivo

Se o usuário remover um dispositivo Plug and Play que o grafo estava usando, o Gerenciador de grafo de filtro posta um evento de [**\_ \_ perda de dispositivo EC**](ec-device-lost.md) . Se o dispositivo ficar disponível novamente, o Gerenciador de grafo de filtro publicará outro evento de **\_ \_ perda de dispositivo EC** . No entanto, o estado anterior do filtro de captura não é mais válido. O aplicativo deve recriar o grafo para usar o dispositivo.

O DirectShow não envia nenhum evento quando um novo dispositivo é conectado. Para saber quando um novo dispositivo está disponível, o aplicativo pode monitorar \_ as mensagens da janela do WM DEVICECHANGE. Para obter mais informações, consulte "gerenciamento de dispositivo" na documentação do Platform SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



