---
title: Serviço de nome
description: Este tópico discute como a biblioteca de gerenciamento de troca dinâmica de dados possibilita que um aplicativo de servidor registre os nomes de serviço aos quais ele dá suporte.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Interface do usuário do Windows, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), serviço de nome
- DDE (troca dinâmica de dados), serviço de nome
- troca de dados, troca dinâmica de dados (DDE)
- Interface do usuário do Windows, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), serviço de nome
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), serviço de nome
- Data Exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- Troca dinâmica de dados (DDE), registro de nome de serviço
- DDE (troca dinâmica de dados), registro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), registro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), registro de nome de serviço
- Troca dinâmica de dados (DDE), filtro de nome de serviço
- DDE (troca dinâmica de dados), filtro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), filtro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), filtro de nome de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292846"
---
# <a name="name-service"></a><span data-ttu-id="7f7be-119">Serviço de nome</span><span class="sxs-lookup"><span data-stu-id="7f7be-119">Name Service</span></span>

<span data-ttu-id="7f7be-120">A biblioteca de gerenciamento de troca dinâmica de dados (DDEML) possibilita que um aplicativo de servidor registre os nomes de serviço aos quais ele dá suporte e impeça que o DDEML envie transações de [**\_ conexão XTYP**](xtyp-connect.md) para nomes de serviço sem suporte na função de retorno de chamada do troca dinâmica de dados (DDE) do servidor.</span><span class="sxs-lookup"><span data-stu-id="7f7be-120">The Dynamic Data Exchange Management Library (DDEML) makes it possible for a server application to register the service names that it supports and to prevent the DDEML from sending [**XTYP\_CONNECT**](xtyp-connect.md) transactions for unsupported service names to the server's Dynamic Data Exchange (DDE) callback function.</span></span>

<span data-ttu-id="7f7be-121">Os tópicos a seguir descrevem o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="7f7be-121">The following topics describe the name service.</span></span>

-   [<span data-ttu-id="7f7be-122">Registro de nome de serviço</span><span class="sxs-lookup"><span data-stu-id="7f7be-122">Service Name Registration</span></span>](#service-name-registration)
-   [<span data-ttu-id="7f7be-123">Filtro de nome de serviço</span><span class="sxs-lookup"><span data-stu-id="7f7be-123">Service Name Filter</span></span>](#service-name-filter)

## <a name="service-name-registration"></a><span data-ttu-id="7f7be-124">Registro de nome de serviço</span><span class="sxs-lookup"><span data-stu-id="7f7be-124">Service Name Registration</span></span>

<span data-ttu-id="7f7be-125">Ao registrar seus nomes de serviço com o DDEML, um servidor informa outros aplicativos DDE no sistema que um novo servidor está disponível.</span><span class="sxs-lookup"><span data-stu-id="7f7be-125">By registering its service names with the DDEML, a server informs other DDE applications in the system that a new server is available.</span></span> <span data-ttu-id="7f7be-126">Um servidor registra um nome de serviço chamando a função [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) e especificando um identificador de cadeia de caracteres que identifica o nome.</span><span class="sxs-lookup"><span data-stu-id="7f7be-126">A server registers a service name by calling the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function and specifying a string handle that identifies the name.</span></span> <span data-ttu-id="7f7be-127">Em resposta, o DDEML envia uma transação de [**\_ registro de XTYP**](xtyp-register.md) para a função de retorno de chamada de cada aplicativo ddeml no sistema (exceto aqueles que especificavam o \_ sinalizador de filtro CBF ignorar \_ registros na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).</span><span class="sxs-lookup"><span data-stu-id="7f7be-127">In response, the DDEML sends an [**XTYP\_REGISTER**](xtyp-register.md) transaction to the callback function of each DDEML application in the system (except those that specified the CBF\_SKIP\_REGISTRATIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span> <span data-ttu-id="7f7be-128">A transação de **\_ registro XTYP** passa dois identificadores de cadeia de caracteres para uma função de retorno de chamada: o primeiro identifica a cadeia de caracteres que especifica o nome do serviço base e o segundo identifica a cadeia de caracteres que especifica o serviço específico da instância.</span><span class="sxs-lookup"><span data-stu-id="7f7be-128">The **XTYP\_REGISTER** transaction passes two string handles to a callback function: the first identifies the string specifying the base service name, and the second identifies the string specifying the instance-specific service.</span></span> <span data-ttu-id="7f7be-129">Um cliente geralmente usa o nome do serviço base em uma lista de servidores disponíveis, para que o usuário possa selecionar um servidor na lista.</span><span class="sxs-lookup"><span data-stu-id="7f7be-129">A client typically uses the base service name in a list of available servers, so the user can select a server from the list.</span></span> <span data-ttu-id="7f7be-130">O cliente usa o nome de serviço específico da instância para estabelecer uma conversa com uma instância específica de um aplicativo de servidor, se mais de uma instância estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="7f7be-130">The client uses the instance-specific service name to establish a conversation with a specific instance of a server application, if more than one instance is running.</span></span>

<span data-ttu-id="7f7be-131">Um servidor pode usar [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para cancelar o registro de um nome de serviço.</span><span class="sxs-lookup"><span data-stu-id="7f7be-131">A server can use [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to unregister a service name.</span></span> <span data-ttu-id="7f7be-132">Essa função faz com que o DDEML envie [**XTYP o \_ registro**](xtyp-unregister.md) de transações para os outros aplicativos DDE no sistema, informando que eles não podem mais usar o nome para estabelecer conversas.</span><span class="sxs-lookup"><span data-stu-id="7f7be-132">This function causes the DDEML to send [**XTYP\_UNREGISTER**](xtyp-unregister.md) transactions to the other DDE applications in the system, informing them that they can no longer use the name to establish conversations.</span></span>

<span data-ttu-id="7f7be-133">Um servidor deve chamar [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar seus nomes de serviço logo após chamar [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span><span class="sxs-lookup"><span data-stu-id="7f7be-133">A server must call [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names soon after calling [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="7f7be-134">Um servidor deve cancelar o registro de seus nomes de serviço usando **DdeNameService** logo antes de chamar a função [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="7f7be-134">A server must unregister its service names by using **DdeNameService** just before calling the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span>

## <a name="service-name-filter"></a><span data-ttu-id="7f7be-135">Filtro de nome de serviço</span><span class="sxs-lookup"><span data-stu-id="7f7be-135">Service Name Filter</span></span>

<span data-ttu-id="7f7be-136">Além de registrar nomes de serviço, o [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) habilita um servidor a ativar ou desativar seu filtro de nome de serviço.</span><span class="sxs-lookup"><span data-stu-id="7f7be-136">In addition to registering service names, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) enables a server to turn its service name filter on or off.</span></span> <span data-ttu-id="7f7be-137">Quando um servidor desativa seu filtro de nome de serviço, o DDEML envia a transação [**XTYP \_ Connect**](xtyp-connect.md) para a função de retorno de chamada DDE do servidor sempre que qualquer cliente chama a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , independentemente do nome do serviço especificado na função.</span><span class="sxs-lookup"><span data-stu-id="7f7be-137">When a server turns off its service name filter, the DDEML sends the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the server's DDE callback function whenever any client calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function, regardless of the service name specified in the function.</span></span> <span data-ttu-id="7f7be-138">Quando um servidor ativa seu filtro de nome de serviço, o DDEML envia a transação **XTYP \_ Connect** para o servidor somente quando **DdeConnect** especifica um nome de serviço que o servidor especificou em uma chamada para **DdeNameService**.</span><span class="sxs-lookup"><span data-stu-id="7f7be-138">When a server turns on its service name filter, the DDEML sends the **XTYP\_CONNECT** transaction to the server only when **DdeConnect** specifies a service name the server has specified in a call to **DdeNameService**.</span></span>

<span data-ttu-id="7f7be-139">Por padrão, o filtro de nome de serviço está ativado quando um aplicativo chama [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span><span class="sxs-lookup"><span data-stu-id="7f7be-139">By default, the service name filter is on when an application calls [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="7f7be-140">Esse padrão impede que o DDEML envie a transação [**XTYP \_ Connect**](xtyp-connect.md) para um servidor antes que o servidor tenha criado a cadeia de caracteres necessária.</span><span class="sxs-lookup"><span data-stu-id="7f7be-140">This default prevents the DDEML from sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to a server before the server has created the string handles it needs.</span></span> <span data-ttu-id="7f7be-141">Um servidor pode desativar seu filtro de nome de serviço especificando o \_ sinalizador DNS FILTEROFF em uma chamada para [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="7f7be-141">A server can turn off its service name filter by specifying the DNS\_FILTEROFF flag in a call to [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="7f7be-142">O \_ sinalizador de filtragem DNS ativa o filtro.</span><span class="sxs-lookup"><span data-stu-id="7f7be-142">The DNS\_FILTERON flag turns on the filter.</span></span>

 

 




