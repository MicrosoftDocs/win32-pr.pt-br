---
description: Notificação de remoção de dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notificação de remoção de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3cc73aba6ad02eb1dfba095b6f45b9fa6c067c51dbe165f4ded86141dae1c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052016"
---
# <a name="device-removal-notification"></a>Notificação de remoção de dispositivo

Se o usuário remover um dispositivo Plug and Play que o grafo estava usando, o Gerenciador de grafo de filtro posta um evento de [**\_ \_ perda de dispositivo EC**](ec-device-lost.md) . Se o dispositivo ficar disponível novamente, o Gerenciador de grafo de filtro publicará outro evento de **\_ \_ perda de dispositivo EC** . No entanto, o estado anterior do filtro de captura não é mais válido. O aplicativo deve recriar o grafo para usar o dispositivo.

DirectShow não envia nenhum evento quando um novo dispositivo é conectado. Para saber quando um novo dispositivo está disponível, o aplicativo pode monitorar \_ as mensagens da janela do WM DEVICECHANGE. Para obter mais informações, consulte "gerenciamento de dispositivo" na documentação do Platform SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



