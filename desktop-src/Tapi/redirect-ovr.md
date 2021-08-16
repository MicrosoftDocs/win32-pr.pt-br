---
description: O redirecionamento de sessão permite que um aplicativo desvie uma sessão oferecida para outro endereço sem responder à chamada.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Redirecionar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea44aaa10bc174784822032359d68d24ba01b6f7f1dcdf0fb211554107b8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761200"
---
# <a name="redirect"></a>Redirecionar

O redirecionamento de sessão permite que um aplicativo desvie uma sessão oferecida para outro endereço sem responder à chamada. O aplicativo pode fazer o redirecionamento em uma base de chamada por chamada. Por exemplo, um aplicativo pode permitir que um usuário especifique redirecionamentos diferentes com base nas informações de ID do chamador. Depois que uma chamada for redirecionada com êxito, o estado normalmente faz a transição para recursos ociosos e associados devem ser liberados.

O redirecionamento [](forward-ovr.md) é diferente do futuro, já que, depois que o encaminhamento tiver sido definido, a operação será executada pela TAPI, pelo provedor de serviços ou pela opção sem mais envolvimento do aplicativo. O redirecionamento é [diferente da transferência,](transfer-ovr.md) já que o redirecionamento não exige a resposta da chamada primeiro.

Nem todos os provedores de serviços suportam o uso dessa operação.

**TAPI 2.x:** Consulte [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
