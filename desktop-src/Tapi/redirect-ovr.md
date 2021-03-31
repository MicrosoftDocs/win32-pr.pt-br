---
description: O redirecionamento de sessão permite que um aplicativo desviar uma sessão oferecida para outro endereço sem responder à chamada.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Redirecionar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663591"
---
# <a name="redirect"></a>Redirecionar

O redirecionamento de sessão permite que um aplicativo desviar uma sessão oferecida para outro endereço sem responder à chamada. O aplicativo pode fazer o redirecionamento em uma base chamada por chamada. Por exemplo, um aplicativo pode permitir que um usuário especifique diferentes redirecionamentos com base nas informações de ID do chamador. Depois que uma chamada for redirecionada com êxito, o estado normalmente será transferido para ocioso e os recursos associados deverão ser liberados.

O redirecionamento difere do [encaminhamento](forward-ovr.md) , uma vez que o encaminhamento foi configurado, a operação é executada pela TAPI, pelo provedor de serviços ou pela opção sem envolvimento adicional do aplicativo. O redirecionamento difere da [transferência](transfer-ovr.md) , pois o redirecionamento não requer a resposta da chamada primeiro.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
