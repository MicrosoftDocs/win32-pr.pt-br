---
description: Se um aplicativo não quiser nenhuma interferência por eventos externos para uma sessão da TAPI ou do provedor de serviços, ele deverá proteger a chamada.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteger uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ee16dc0854c6502f1347a3aa676e709920555ad91a02190db001bd80b34824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080456"
---
# <a name="secure-a-session"></a>Proteger uma sessão

Se um aplicativo não quiser nenhuma interferência por eventos externos para uma sessão da TAPI ou do provedor de serviços, ele deverá proteger a chamada. Por exemplo, em uma chamada de ambiente analógico, os tons de espera podem destruir uma sessão de fax ou modem na chamada original.

Um aplicativo pode proteger uma chamada no momento em que a chamada é feita ou após a chamada já existir.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3. x:** Consulte [**ITAddress:: forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
