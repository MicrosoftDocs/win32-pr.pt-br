---
title: Registrando para notificação de alteração
description: Um cliente pode se registrar para receber notificações de alterações nas informações de roteamento armazenadas no Gerenciador de tabela de roteamento. Essa solicitação só pode ser feita depois que um cliente é registrado com o Gerenciador de tabela de roteamento.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7049478a5be834b08b7bb17ad9ebfb0fdf70736837f27d53e7900bf7bfdc88dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788615"
---
# <a name="registering-for-change-notification"></a>Registrando para notificação de alteração

Um cliente pode se registrar para receber notificações de alterações nas informações de roteamento armazenadas no Gerenciador de tabela de roteamento. Essa solicitação só pode ser feita depois que um cliente é registrado com o Gerenciador de tabela de roteamento.

Para se registrar para notificação de alteração, um cliente deve chamar [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), especificando os tipos de alterações para as quais o cliente deve receber a notificação. Se o cliente precisar ser notificado sobre alteração em destinos específicos, o cliente chamará [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) uma vez para cada destino.

O cliente pode parar de receber notificações de alteração chamando [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).

Para obter um exemplo de código que mostra como usar essas funções, consulte [registrar para notificação de alteração](register-for-change-notification.md).

 

 




