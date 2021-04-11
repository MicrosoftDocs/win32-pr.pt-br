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
# <a name="the-notify-flag"></a><span data-ttu-id="27d3d-104">O sinalizador de notificação</span><span class="sxs-lookup"><span data-stu-id="27d3d-104">The Notify Flag</span></span>

<span data-ttu-id="27d3d-105">O sinalizador "notificar" ( \_ notificação MCI) direciona o dispositivo para postar uma mensagem [**mm MCINOTIFY**](mm-mcinotify.md) quando o dispositivo conclui uma ação.</span><span class="sxs-lookup"><span data-stu-id="27d3d-105">The "notify" (MCI\_NOTIFY) flag directs the device to post an [**MM MCINOTIFY**](mm-mcinotify.md) message when the device completes an action.</span></span> <span data-ttu-id="27d3d-106">Seu aplicativo deve ter um procedimento de janela para processar a \_ mensagem mm MCINOTIFY para que a notificação tenha qualquer efeito.</span><span class="sxs-lookup"><span data-stu-id="27d3d-106">Your application must have a window procedure to process the MM\_MCINOTIFY message for notification to have any effect.</span></span> <span data-ttu-id="27d3d-107">Uma \_ mensagem mm MCINOTIFY indica que o processamento de um comando foi concluído, mas não indica se o comando foi concluído com êxito, se falhou ou foi substituído ou anulado.</span><span class="sxs-lookup"><span data-stu-id="27d3d-107">An MM\_MCINOTIFY message indicates that the processing of a command has completed, but it does not indicate whether the command was completed successfully, failed, or was superseded or aborted.</span></span>

<span data-ttu-id="27d3d-108">O aplicativo especifica o identificador para a janela de destino da mensagem quando emite um comando.</span><span class="sxs-lookup"><span data-stu-id="27d3d-108">The application specifies the handle to the destination window for the message when it issues a command.</span></span> <span data-ttu-id="27d3d-109">Na interface de cadeia de caracteres de comando, esse identificador é o último parâmetro da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="27d3d-109">In the command-string interface, this handle is the last parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="27d3d-110">Na interface de mensagem de comando, o identificador é especificado na palavra de ordem inferior do membro **dwCallBack** da estrutura enviada com a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="27d3d-110">In the command-message interface, the handle is specified in the low-order word of the **dwCallBack** member of the structure sent with the command message.</span></span> <span data-ttu-id="27d3d-111">(Cada estrutura associada a uma mensagem de comando contém esse membro.)</span><span class="sxs-lookup"><span data-stu-id="27d3d-111">(Every structure associated with a command message contains this member.)</span></span>

 

 