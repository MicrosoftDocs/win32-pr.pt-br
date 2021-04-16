---
description: O acompanhamento de CallHub é um novo recurso da TAPI versão 3,0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Suporte do CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758415"
---
# <a name="callhub-support"></a>Suporte do CallHub

O acompanhamento de CallHub é um novo recurso da TAPI versão 3,0. A funcionalidade CallHub foi adicionada aos elementos de programação TAPI 2,1 com a entrega do Windows 2000. Um *CallHub* representa uma exibição de terceiros de uma chamada, e os identificadores de chamada da TAPI representam a exibição de primeira parte de uma chamada. Com o acompanhamento de CallHub, o provedor de serviços é solicitado a seguir CallHubs e fornecer informações sobre a chamada durante o tempo de vida de um CallHub. À medida que novas partes ingressam e deixam o CallHub, o provedor de serviços deve informar a TAPI.

Um provedor de serviços não precisa implementar nenhuma função nova para dar suporte a CallHub. Ele simplesmente precisa preencher o membro **dwCallID** da estrutura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) . Na TAPI 3, a TAPI coleta todas as chamadas com o mesmo **dwCallID** e cria um identificador CallHub que o aplicativo pode usar para rastrear a chamada.

 

 
