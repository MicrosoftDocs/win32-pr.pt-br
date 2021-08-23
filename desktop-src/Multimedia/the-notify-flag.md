---
title: O sinalizador Notify
description: O sinalizador Notify
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY sinalizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbec671a9810d31078eedf9b8557bcdc4fa7c3e82f688b7fd005f85cb4127476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688266"
---
# <a name="the-notify-flag"></a>O sinalizador Notify

O sinalizador "notify" (MCI NOTIFY) direciona o dispositivo para postar uma mensagem \_ [**MM MCINOTIFY**](mm-mcinotify.md) quando o dispositivo conclui uma ação. Seu aplicativo deve ter um procedimento de janela para processar a mensagem MM \_ MCINOTIFY para que a notificação tenha qualquer efeito. Uma mensagem MM MCINOTIFY indica que o processamento de um comando foi concluído, mas não indica se o comando foi concluído com êxito, falhou ou foi \_ anulado ou anulado.

O aplicativo especifica o handle para a janela de destino para a mensagem quando ele emite um comando. Na interface de cadeia de caracteres de comando, esse handle é o último parâmetro da [**função mciSendString.**](/previous-versions//dd757161(v=vs.85)) Na interface de mensagem de comando, o handle é especificado na palavra de ordem baixa do membro **dwCallBack** da estrutura enviada com a mensagem de comando. (Cada estrutura associada a uma mensagem de comando contém esse membro.)

 

 