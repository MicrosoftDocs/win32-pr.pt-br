---
description: Se um aplicativo não quiser nenhuma interferência por eventos externos para uma sessão da TAPI ou do provedor de serviços, ele deverá proteger a chamada.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteger uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792614"
---
# <a name="secure-a-session"></a>Proteger uma sessão

Se um aplicativo não quiser nenhuma interferência por eventos externos para uma sessão da TAPI ou do provedor de serviços, ele deverá proteger a chamada. Por exemplo, em uma chamada de ambiente analógico, os tons de espera podem destruir uma sessão de fax ou modem na chamada original.

Um aplicativo pode proteger uma chamada no momento em que a chamada é feita ou após a chamada já existir.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3. x:** Consulte [**ITAddress:: forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
