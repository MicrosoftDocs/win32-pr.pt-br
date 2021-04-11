---
title: O sinalizador de notificação
description: O sinalizador de notificação
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- Sinalizador de MCI_NOTIFY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365973"
---
# <a name="the-notify-flag"></a>O sinalizador de notificação

O sinalizador "notificar" ( \_ notificação MCI) direciona o dispositivo para postar uma mensagem [**mm MCINOTIFY**](mm-mcinotify.md) quando o dispositivo conclui uma ação. Seu aplicativo deve ter um procedimento de janela para processar a \_ mensagem mm MCINOTIFY para que a notificação tenha qualquer efeito. Uma \_ mensagem mm MCINOTIFY indica que o processamento de um comando foi concluído, mas não indica se o comando foi concluído com êxito, se falhou ou foi substituído ou anulado.

O aplicativo especifica o identificador para a janela de destino da mensagem quando emite um comando. Na interface de cadeia de caracteres de comando, esse identificador é o último parâmetro da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Na interface de mensagem de comando, o identificador é especificado na palavra de ordem inferior do membro **dwCallBack** da estrutura enviada com a mensagem de comando. (Cada estrutura associada a uma mensagem de comando contém esse membro.)

 

 