---
title: Monitorando conexões de sessão e desconexões
description: Para registrar um aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007652"
---
# <a name="monitoring-session-connections-and-disconnections"></a><span data-ttu-id="5b57c-103">Monitorando conexões de sessão e desconexões</span><span class="sxs-lookup"><span data-stu-id="5b57c-103">Monitoring session connections and disconnections</span></span>

<span data-ttu-id="5b57c-104">Para um aplicativo de serviço, como um aplicativo de servidor de canal virtual, para monitorar conexões de sessão e desconexões, você deve registrá-lo com Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="5b57c-104">For a service application, such as a virtual channel server application, to monitor session connections and disconnections, you must register it with Remote Desktop Services.</span></span> <span data-ttu-id="5b57c-105">Para registrar o aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="5b57c-105">To register the application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="5b57c-106">**HKEY \_ O sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **AddIns**</span><span class="sxs-lookup"><span data-stu-id="5b57c-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**</span></span>

<span data-ttu-id="5b57c-107">A subchave pode ter qualquer nome.</span><span class="sxs-lookup"><span data-stu-id="5b57c-107">The subkey can have any name.</span></span> <span data-ttu-id="5b57c-108">Ele deve ter um valor de **reg \_ sz** , **nome**, que contenha o nome simbólico do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b57c-108">It must have a **REG\_SZ** value, **Name**, that contains the symbolic name of the application.</span></span>

``` syntax
Name = AddinName
```

<span data-ttu-id="5b57c-109">O comprimento máximo da subchave e do valor do **nome** é de 99 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5b57c-109">The maximum length of both the subkey and the value of **Name** is 99 characters.</span></span>

<span data-ttu-id="5b57c-110">A subchave também deve ter um valor **reg \_ DWORD** que indica o tipo de aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="5b57c-110">The subkey must also have a **REG\_DWORD** value that indicates the type of server application.</span></span>

``` syntax
Type = AddinType
```

<span data-ttu-id="5b57c-111">*Addintype* deve ser o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b57c-111">*AddinType* must be the following value.</span></span>



| <span data-ttu-id="5b57c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5b57c-112">Value</span></span> | <span data-ttu-id="5b57c-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5b57c-113">Meaning</span></span>                               |
|-------|---------------------------------------|
| <span data-ttu-id="5b57c-114">3</span><span class="sxs-lookup"><span data-stu-id="5b57c-114">3</span></span>     | <span data-ttu-id="5b57c-115">Aplicativo de modo de usuário, espaço de sessão.</span><span class="sxs-lookup"><span data-stu-id="5b57c-115">User-mode application, session space.</span></span> |



 

<span data-ttu-id="5b57c-116">O registro do aplicativo de serviço entra em vigor somente em sessões criadas após a execução do registro.</span><span class="sxs-lookup"><span data-stu-id="5b57c-116">Registration of the service application takes effect only in sessions created after the registration was performed.</span></span>

<span data-ttu-id="5b57c-117">Para cada aplicativo de serviço registrado, Serviços de Área de Trabalho Remota sinalizará um conjunto de objetos de evento quando um cliente se conectar ou se desconectar da sessão.</span><span class="sxs-lookup"><span data-stu-id="5b57c-117">For each registered service application, Remote Desktop Services will signal a set of event objects when a client connects or disconnects from the session.</span></span> <span data-ttu-id="5b57c-118">Cada plug-in de canal virtual deve se registrar e criar os eventos de notificação chamando [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span><span class="sxs-lookup"><span data-stu-id="5b57c-118">Each virtual channel plug-in must register itself and create the notification events by calling [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span></span> <span data-ttu-id="5b57c-119">Os nomes desses objetos de evento aderem ao formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b57c-119">The names of these event objects adhere to the following format.</span></span>

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

<span data-ttu-id="5b57c-120">*AddInName* é a cadeia de caracteres especificada no valor de **nome** da subchave do registro sob a qual o aplicativo do servidor está registrado.</span><span class="sxs-lookup"><span data-stu-id="5b57c-120">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="5b57c-121">A criação desses eventos em uma sessão faz com que eles sejam criados em um diretório de eventos por sessão especial.</span><span class="sxs-lookup"><span data-stu-id="5b57c-121">Creating these events under a session causes them to be created in a special per-session event directory.</span></span> <span data-ttu-id="5b57c-122">O diretório de eventos fornece segurança adicional, impedindo que aplicativos em outras sessões modifiquem o estado desses eventos.</span><span class="sxs-lookup"><span data-stu-id="5b57c-122">The event directory provides added security by preventing applications in other sessions from modifying the state of these events.</span></span>

<span data-ttu-id="5b57c-123">Para controlar se os eventos reconectar e desconectar são recebidos no servidor, você pode posicionar o sinalizador **RemoteControlPersistent** no registro na seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="5b57c-123">To control whether RECONNECT and DISCONNECT events are received on the server, you can place the **RemoteControlPersistent** flag in the registry under the following key:</span></span>

<span data-ttu-id="5b57c-124">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **controle** \\ **TerminalServer** \\ **AddIns** \\ *AddInName*</span><span class="sxs-lookup"><span data-stu-id="5b57c-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**\\*addinname*</span></span>

<span data-ttu-id="5b57c-125">O sinalizador habilita ou desabilita a reconexão e a desconexão de eventos de serem sinalizados quando uma sessão de cliente é iniciada ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="5b57c-125">The flag enables or disables RECONNECT and DISCONNECT events from being signaled when a client session starts or stops.</span></span> <span data-ttu-id="5b57c-126">A sintaxe do valor de **reg \_ DWORD** é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="5b57c-126">The syntax of the **REG\_DWORD** value is the following.</span></span>

``` syntax
RemoteControlPersistent = flag
```

<span data-ttu-id="5b57c-127">O valor do *sinalizador* pode ser um ou zero.</span><span class="sxs-lookup"><span data-stu-id="5b57c-127">The value of *flag* can be one or zero.</span></span> <span data-ttu-id="5b57c-128">Zero é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="5b57c-128">Zero is the default value.</span></span> <span data-ttu-id="5b57c-129">Se definido como um, o aplicativo de serviço não será notificado se a sessão do cliente for iniciada ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="5b57c-129">If set to one, the service application will not be notified if the client session is started or stopped.</span></span> <span data-ttu-id="5b57c-130">Se definido como zero, um evento reconnect será sinalizado quando a sessão do cliente for iniciada e um evento de desconexão será sinalizado quando a sessão do cliente for interrompida.</span><span class="sxs-lookup"><span data-stu-id="5b57c-130">If set to zero, a RECONNECT event is signaled when the client session starts, and a DISCONNECT event is signaled when the client session stops.</span></span>

<span data-ttu-id="5b57c-131">O formato de nome de objeto de evento anterior ainda tem suporte no Windows Server 2008 para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="5b57c-131">The previous event-object name format is still supported in Windows Server 2008 for backward compatibility.</span></span> <span data-ttu-id="5b57c-132">É recomendável que você use o formato mais recente do Windows Server 2008, pois ele é mais seguro.</span><span class="sxs-lookup"><span data-stu-id="5b57c-132">It is recommended that you use the newer Windows Server 2008 format because it is more secure.</span></span>

<span data-ttu-id="5b57c-133">O formato de evento anterior é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="5b57c-133">The previous event format is as follows.</span></span>

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

<span data-ttu-id="5b57c-134">*AddInName* é a cadeia de caracteres especificada no valor de **nome** da subchave do registro sob a qual o aplicativo do servidor está registrado.</span><span class="sxs-lookup"><span data-stu-id="5b57c-134">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="5b57c-135">*SessionID* é o identificador de sessão de uma sessão de cliente.</span><span class="sxs-lookup"><span data-stu-id="5b57c-135">*SessionId* is the session identifier of a client session.</span></span>

 

 