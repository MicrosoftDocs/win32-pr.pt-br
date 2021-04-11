---
title: Detalhes da implementação do EAP
description: Pontos de acesso (APs), como o serviço de acesso remoto (RAS), interagem com implementações de EAP por meio do uso de chamadas de função que devem ser exportadas pela DLL EAP de terceiros.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293976"
---
# <a name="eap-implementation-details"></a><span data-ttu-id="fc1e0-103">Detalhes da implementação do EAP</span><span class="sxs-lookup"><span data-stu-id="fc1e0-103">EAP Implementation Details</span></span>

<span data-ttu-id="fc1e0-104">Pontos de acesso (APs), como o serviço de acesso remoto (RAS), interagem com implementações de EAP por meio do uso de chamadas de função que devem ser exportadas pela DLL EAP de terceiros.</span><span class="sxs-lookup"><span data-stu-id="fc1e0-104">Access Points (APs), such as Remote Access Service (RAS), interact with EAP implementations through the use of function calls that must be exported by the third-party EAP DLL.</span></span> <span data-ttu-id="fc1e0-105">Em outras palavras, o EAP é uma API de provedor, o que significa que plug-ins ou DLLs implementam código para se tornar um provedor de EAP, mas não devem chamar as APIs de EAP.</span><span class="sxs-lookup"><span data-stu-id="fc1e0-105">In other words, EAP is a provider API, meaning that plug-ins or DLLs implement code to become an EAP provider, but must not call the EAP APIs themselves.</span></span> <span data-ttu-id="fc1e0-106">Por exemplo, um programador de uma DLL de EAP cria código para uma rotina de inicialização de EAP e coloca esse código na função predefinida do EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc1e0-106">For example, a programmer of an EAP DLL creates code for an EAP initialization routine and places this code in the EAP predefined function [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span></span> <span data-ttu-id="fc1e0-107">Em seguida, em tempo de execução, o Gerenciador de conexões do AP chama a função **RasEapInitialize** , que contém o código, para inicializar a implementação do EAP.</span><span class="sxs-lookup"><span data-stu-id="fc1e0-107">Then at run-time, the AP connection manager calls the **RasEapInitialize** function, which contains the code, to initialize the EAP implementation.</span></span>

<span data-ttu-id="fc1e0-108">Os tópicos a seguir detalham essa interação:</span><span class="sxs-lookup"><span data-stu-id="fc1e0-108">The following topics detail this interaction:</span></span>

-   [<span data-ttu-id="fc1e0-109">Inicialização do ponto de acesso do EAP</span><span class="sxs-lookup"><span data-stu-id="fc1e0-109">Access Point Initialization of EAP</span></span>](ras-initialization-of-eap.md)
-   [<span data-ttu-id="fc1e0-110">Inicialização do protocolo de autenticação</span><span class="sxs-lookup"><span data-stu-id="fc1e0-110">Authentication Protocol Initialization</span></span>](authentication-protocol-initialization.md)
-   [<span data-ttu-id="fc1e0-111">Interação do protocolo de autenticação e ponto de acesso</span><span class="sxs-lookup"><span data-stu-id="fc1e0-111">Access Point and Authentication Protocol Interaction</span></span>](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [<span data-ttu-id="fc1e0-112">Conclusão da sessão de autenticação</span><span class="sxs-lookup"><span data-stu-id="fc1e0-112">Completion of the Authentication Session</span></span>](completion-of-the-authentication-session.md)

 

 