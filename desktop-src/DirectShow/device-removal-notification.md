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

Se o usuário remover um dispositivo Plug and Play que o grafo estava usando, o gerenciador de grafo de filtro postará um evento [**EC \_ DEVICE \_ LOST.**](ec-device-lost.md) Se o dispositivo ficar disponível novamente, o gerenciador de grafo de filtro postará outro **evento EC \_ DEVICE \_ LOST.** No entanto, o estado anterior do filtro de captura não é mais válido. O aplicativo deve recriar o grafo para usar o dispositivo.

DirectShow não envia nenhum evento quando um novo dispositivo está conectado. Para saber quando um novo dispositivo está disponível, o aplicativo pode monitorar mensagens de janela WM \_ DEVICECHANGE. Para obter mais informações, consulte "Gerenciamento de Dispositivos" na documentação do SDK da plataforma.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



