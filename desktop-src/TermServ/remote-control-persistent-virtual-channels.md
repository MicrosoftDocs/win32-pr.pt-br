---
title: Canais virtuais persistentes de controle remoto
description: Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta da sessão conectada ao cliente. Os dados continuarão a ser transmitidos e recebidos por meio desse canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364385"
---
# <a name="remote-control-persistent-virtual-channels"></a><span data-ttu-id="155a1-104">Canais virtuais persistentes de controle remoto</span><span class="sxs-lookup"><span data-stu-id="155a1-104">Remote Control Persistent Virtual Channels</span></span>

<span data-ttu-id="155a1-105">No Windows XP, uma DLL pode especificar um ou mais canais virtuais como *persistentes de controle remoto*.</span><span class="sxs-lookup"><span data-stu-id="155a1-105">On Windows XP, a DLL can specify one or more virtual channels as *remote control persistent*.</span></span> <span data-ttu-id="155a1-106">Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta da sessão conectada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="155a1-106">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="155a1-107">Os dados continuarão a ser transmitidos e recebidos por meio desse canal.</span><span class="sxs-lookup"><span data-stu-id="155a1-107">Data will continue to be transmitted and received through this channel.</span></span> <span data-ttu-id="155a1-108">Os canais virtuais que a DLL não especificar como controle remoto persistentes serão fechados nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="155a1-108">Virtual channels that the DLL does not specify as remote control persistent will close in this scenario.</span></span>

<span data-ttu-id="155a1-109">Os canais virtuais persistentes de controle remoto são especificados durante a chamada para **VirtualChannelInit**.</span><span class="sxs-lookup"><span data-stu-id="155a1-109">Remote control persistent virtual channels are specified during the call to **VirtualChannelInit**.</span></span> <span data-ttu-id="155a1-110">Consulte a página de referência de [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) para obter informações específicas sobre isso.</span><span class="sxs-lookup"><span data-stu-id="155a1-110">Refer to the reference page for [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) for specific information about this.</span></span>

 

 




