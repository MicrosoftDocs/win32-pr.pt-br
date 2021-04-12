---
title: Fechando um dispositivo
description: Fechando um dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363700"
---
# <a name="closing-a-device"></a><span data-ttu-id="91d48-104">Fechando um dispositivo</span><span class="sxs-lookup"><span data-stu-id="91d48-104">Closing a Device</span></span>

<span data-ttu-id="91d48-105">O comando [**fechar**](close.md) ([**MCI \_ Close**](mci-close.md)) libera o acesso a um dispositivo ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="91d48-105">The [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) command releases access to a device or file.</span></span> <span data-ttu-id="91d48-106">O MCI libera um dispositivo quando todas as tarefas que usam um dispositivo o fecham.</span><span class="sxs-lookup"><span data-stu-id="91d48-106">MCI frees a device when all tasks using a device have closed it.</span></span> <span data-ttu-id="91d48-107">Para ajudar o MCI a gerenciar os dispositivos, seu aplicativo deve fechar cada dispositivo ou arquivo quando terminar de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="91d48-107">To help MCI manage the devices, your application must close each device or file when it is finished using it.</span></span>

<span data-ttu-id="91d48-108">Quando você fecha um dispositivo MCI externo que usa sua própria mídia em vez de arquivos (como áudio de CD), o driver deixa o dispositivo em seu modo atual de operação.</span><span class="sxs-lookup"><span data-stu-id="91d48-108">When you close an external MCI device that uses its own media instead of files (such as CD audio), the driver leaves the device in its current mode of operation.</span></span> <span data-ttu-id="91d48-109">Portanto, se você fechar um dispositivo de áudio de CD que está sendo executado, mesmo que o driver de dispositivo seja liberado da memória, o dispositivo de áudio de CD continuará a ser reproduzido até atingir o final de seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="91d48-109">Thus, if you close a CD audio device that is playing, even though the device driver is released from memory, the CD audio device will continue to play until it reaches the end of its content.</span></span>

> [!Note]  
> <span data-ttu-id="91d48-110">Fechar um aplicativo com dispositivos MCI abertos pode impedir que outros aplicativos usem esses dispositivos até que o Windows seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="91d48-110">Closing an application with open MCI devices can prevent other applications from using those devices until Windows is restarted.</span></span>

 

 

 




