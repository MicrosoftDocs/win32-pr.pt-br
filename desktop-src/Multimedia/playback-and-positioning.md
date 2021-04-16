---
title: Reprodução e posicionamento
description: Reprodução e posicionamento
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105751173"
---
# <a name="playback-and-positioning"></a><span data-ttu-id="b37a2-103">Reprodução e posicionamento</span><span class="sxs-lookup"><span data-stu-id="b37a2-103">Playback and Positioning</span></span>

<span data-ttu-id="b37a2-104">Vários comandos MCI, como [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)), [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)), [**Pause**](pause.md) ([**MCI \_ Pause**](mci-pause.md)), [**retomar**](resume.md) ([**MCI \_ resume**](mci-resume.md)) e [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), afetam a reprodução ou o posicionamento de um arquivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="b37a2-104">A number of MCI commands, such as [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)), and [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)), affect the playback or positioning of a multimedia file.</span></span> <span data-ttu-id="b37a2-105">Se um dispositivo MCI receber um comando de reprodução enquanto outro comando de reprodução estiver em andamento, ele aceitará o comando e interromperá ou substituirá o comando anterior.</span><span class="sxs-lookup"><span data-stu-id="b37a2-105">If an MCI device receives a playback command while another playback command is in progress, it accepts the command and either stops or supersedes the previous command.</span></span>

<span data-ttu-id="b37a2-106">Muitos comandos MCI, como [**set**](set.md) ([**MCI \_ set**](mci-set.md)), não afetam a reprodução.</span><span class="sxs-lookup"><span data-stu-id="b37a2-106">Many MCI commands, such as [**set**](set.md) ([**MCI\_SET**](mci-set.md)), do not affect playback.</span></span> <span data-ttu-id="b37a2-107">Uma notificação de um desses comandos não interfere nos comandos de reprodução ou de posição pendentes, desde que as notificações não sejam executadas da mesma instância do driver.</span><span class="sxs-lookup"><span data-stu-id="b37a2-107">A notification from one of these commands does not interfere with pending playback or position commands as long as the notifications are not performed from the same instance of the driver.</span></span> <span data-ttu-id="b37a2-108">Por exemplo, você pode emitir um comando **set** ou [**status**](status.md) ([**\_ status MCI**](mci-status.md)) enquanto um dispositivo estiver executando um comando de **busca** sem interromper ou substituir o comando de **busca** .</span><span class="sxs-lookup"><span data-stu-id="b37a2-108">For example, you can issue a **set** or [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command while a device is performing a **seek** command without stopping or superseding the **seek** command.</span></span>

<span data-ttu-id="b37a2-109">No entanto, pode haver apenas uma notificação pendente.</span><span class="sxs-lookup"><span data-stu-id="b37a2-109">However, there can be only one pending notification.</span></span> <span data-ttu-id="b37a2-110">Por exemplo, se um aplicativo solicitar uma notificação para **reproduzir** e seguir essa solicitação com o **status** "Iniciar notificação de posição", a notificação de **reprodução** retornará "substituída" e a notificação para o comando de status retornará quando for concluída.</span><span class="sxs-lookup"><span data-stu-id="b37a2-110">For example, if an application requests a notification for **play** and follows that request with **status** "start position notify," the **play** notification will return "superseded" and the notification for the status command will return when it is finished.</span></span> <span data-ttu-id="b37a2-111">Nesse caso, no entanto, o comando **Play** ainda terá sucesso, embora o aplicativo não tenha recebido a notificação.</span><span class="sxs-lookup"><span data-stu-id="b37a2-111">In this case, however, the **play** command will still succeed, even though the application did not receive the notification.</span></span>

 

 




