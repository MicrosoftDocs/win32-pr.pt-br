---
description: Mensagens de dispositivo são mensagens do sistema que notificam aplicativos e outros recursos de eventos de alteração do dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Mensagens do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a26666ab0f7675da02e70d53ffd8aec5040a0482a0a2cdc71279fcaeca8ca92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053502"
---
# <a name="device-messages"></a>Mensagens do dispositivo

Mensagens de dispositivo são mensagens do sistema que notificam aplicativos e outros recursos de eventos de alteração do dispositivo. Esses eventos ocorrem sempre que o sistema detecta uma alteração no hardware do sistema, como quando o usuário encaixa e desencaixa um computador laptop, ou insere ou remove um dispositivo, como uma placa PCMCIA. Os eventos de dispositivo podem ocorrer enquanto o sistema está em execução ou quando o sistema retoma a operação depois de ser suspenso temporariamente.

Para ajudar a garantir que os aplicativos não percam dados quando os dispositivos ficarem indisponíveis, o sistema monitora a configuração de hardware e envia mensagens de dispositivo aos aplicativos para notificá-las das alterações e dar a ela a oportunidade de se preparar para as alterações antes que elas ocorram.

Para cada evento de dispositivo, o sistema transmite uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) para todos os aplicativos. Nessa mensagem, o parâmetro *wParam* identifica o [tipo de evento do dispositivo](device-event-types.md) e o parâmetro *lParam* é um ponteiro para dados específicos do evento.

 

 



