---
title: Detalhes da implementação do EAP
description: Pontos de acesso (APs), como o serviço de acesso remoto (RAS), interagem com implementações de EAP por meio do uso de chamadas de função que devem ser exportadas pela DLL EAP de terceiros.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8772d839e6d6fb748f56de0329a958057400d37afeb92a2f3ec89b3ab462e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852406"
---
# <a name="eap-implementation-details"></a>Detalhes da implementação do EAP

Pontos de acesso (APs), como o serviço de acesso remoto (RAS), interagem com implementações de EAP por meio do uso de chamadas de função que devem ser exportadas pela DLL EAP de terceiros. Em outras palavras, o EAP é uma API de provedor, o que significa que plug-ins ou DLLs implementam código para se tornar um provedor de EAP, mas não devem chamar as APIs de EAP. Por exemplo, um programador de uma DLL de EAP cria código para uma rotina de inicialização de EAP e coloca esse código na função predefinida do EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)). Em seguida, em tempo de execução, o Gerenciador de conexões do AP chama a função **RasEapInitialize** , que contém o código, para inicializar a implementação do EAP.

Os tópicos a seguir detalham essa interação:

-   [Inicialização do ponto de acesso do EAP](ras-initialization-of-eap.md)
-   [Inicialização do protocolo de autenticação](authentication-protocol-initialization.md)
-   [Interação do protocolo de autenticação e ponto de acesso](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Conclusão da sessão de autenticação](completion-of-the-authentication-session.md)

 

 