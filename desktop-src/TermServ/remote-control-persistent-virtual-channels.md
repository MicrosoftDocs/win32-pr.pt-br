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
# <a name="remote-control-persistent-virtual-channels"></a>Canais virtuais persistentes de controle remoto

No Windows XP, uma DLL pode especificar um ou mais canais virtuais como *persistentes de controle remoto*. Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta da sessão conectada ao cliente. Os dados continuarão a ser transmitidos e recebidos por meio desse canal. Os canais virtuais que a DLL não especificar como controle remoto persistentes serão fechados nesse cenário.

Os canais virtuais persistentes de controle remoto são especificados durante a chamada para **VirtualChannelInit**. Consulte a página de referência de [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) para obter informações específicas sobre isso.

 

 




