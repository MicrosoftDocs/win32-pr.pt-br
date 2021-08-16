---
description: A TAPI atribui identificadores de sessão que são exclusivos para cada sessão e aplicativo.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificador de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527706159328b3919e47c39bc5fb160615ed2c202d33c1ce39c711b6921235a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760778"
---
# <a name="session-identifier"></a>Identificador de sessão

A TAPI atribui identificadores de sessão que são exclusivos para cada sessão e aplicativo. Um aplicativo usa um identificador de sessão para se comunicar com a TAPI em relação a uma sessão específica. Um aplicativo normalmente Obtém um identificador criando uma nova sessão de comunicações ou quando a TAPI oferece uma sessão.

Um identificador de sessão não pode ser usado para passar informações para outro aplicativo. Para essa finalidade, use a [ID de chamada](call-id-ovr.md), que pode ser atribuída por um provedor de serviços.

Consulte [iniciar uma sessão](initiate-a-session-ovr.md) para obter informações sobre operações que criam sessões e retornam um identificador de sessão. Consulte [responder à sessão iniciada em outro lugar](respond-to-session-initiated-elsewhere-ovr.md) para operações que adquirem identificadores de sessão da TAPI. Consulte [encerrar uma sessão](terminate-a-session-ovr.md) para obter informações sobre como liberar recursos de sessão.

Todos os provedores de serviço devem oferecer suporte a alguma forma de identificação de sessão.

**TAPI 2. x:** O identificador principal de uma sessão de comunicações é o identificador de chamada.

**TAPI 3. x:** Uma sessão é representada por um [objeto de chamada](call-object.md) e o identificador primário é um ponteiro para a interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

 

 



