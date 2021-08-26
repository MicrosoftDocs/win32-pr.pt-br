---
title: Canais virtuais persistentes de controle remoto
description: Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta para a sessão conectada ao cliente. Os dados continuarão a ser transmitidos e recebidos por meio desse canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71206b8272fb516da9a3c39bed7f7d54edbc5227958d975bf11b114db9c13869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988776"
---
# <a name="remote-control-persistent-virtual-channels"></a>Canais virtuais persistentes de controle remoto

No Windows XP, uma DLL pode especificar um ou mais canais virtuais como *controle remoto persistente.* Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta para a sessão conectada ao cliente. Os dados continuarão a ser transmitidos e recebidos por meio desse canal. Os canais virtuais que a DLL não especifica como controle remoto persistente fecharão nesse cenário.

Os canais virtuais persistentes do controle remoto são especificados durante a chamada para **VirtualChannelInit.** Consulte a página de referência de [**VirtualChannelInit para**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) obter informações específicas sobre isso.

 

 




