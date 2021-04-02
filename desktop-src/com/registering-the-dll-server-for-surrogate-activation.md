---
title: Registrando o servidor DLL para ativação alternativa
description: Registrando o servidor DLL para ativação alternativa
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641891"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a><span data-ttu-id="22262-103">Registrando o servidor DLL para ativação alternativa</span><span class="sxs-lookup"><span data-stu-id="22262-103">Registering the DLL Server for Surrogate Activation</span></span>

<span data-ttu-id="22262-104">Um servidor DLL será carregado em um processo substituto sob as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="22262-104">A DLL server will be loaded into a surrogate process under the following conditions:</span></span>

-   <span data-ttu-id="22262-105">Deve haver um valor AppID especificado na chave CLSID no registro e uma chave [AppID](appid-key.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="22262-105">There must be an AppID value specified under the CLSID key in the registry, and a corresponding [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="22262-106">Em uma chamada de ativação, o bit do [**\_ \_ servidor local CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) é definido e a chave CLSID não especifica [LocalServer32](localserver32.md), [LocalServer](localserver.md)ou [LocalService](localservice.md).</span><span class="sxs-lookup"><span data-stu-id="22262-106">In an activation call, the [**CLSCTX\_LOCAL\_SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) bit is set and the CLSID key does not specify [LocalServer32](localserver32.md), [LocalServer](localserver.md), or [LocalService](localservice.md).</span></span> <span data-ttu-id="22262-107">Se outros bits **CLSCTX** estiverem definidos, o [**algoritmo de processamento**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)para os sinalizadores de execução em processo, local ou remoto será seguido.</span><span class="sxs-lookup"><span data-stu-id="22262-107">If other **CLSCTX** bits are set, the [**processing algorithm**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)for the in-process, local, or remote execution flags is followed.</span></span>
-   <span data-ttu-id="22262-108">A chave CLSID contém a subchave [InprocServer32](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="22262-108">The CLSID key contains the [InprocServer32](inprocserver32.md) subkey.</span></span>
-   <span data-ttu-id="22262-109">A DLL de proxy/stub especificada na chave **InprocServer32** existe.</span><span class="sxs-lookup"><span data-stu-id="22262-109">The proxy/stub DLL specified in the **InprocServer32** key exists.</span></span>
-   <span data-ttu-id="22262-110">O valor de [DllSurrogate](dllsurrogate.md) existe na chave **AppID** .</span><span class="sxs-lookup"><span data-stu-id="22262-110">The [DllSurrogate](dllsurrogate.md) value exists under the **AppID** key.</span></span>

<span data-ttu-id="22262-111">Se houver um **LocalServer**, **LocalServer32** ou **LocalService**, indicando a existência de um exe, o servidor exe ou o serviço sempre será iniciado em preferência ao carregamento de um servidor dll em um processo substituto.</span><span class="sxs-lookup"><span data-stu-id="22262-111">If there is a **LocalServer**, **LocalServer32**, or **LocalService**, indicating the existence of an EXE, the EXE server or service will always be launched in preference to loading a DLL server into a surrogate process.</span></span>

<span data-ttu-id="22262-112">O valor nomeado **DllSurrogate** deve ser especificado para que a ativação substituta ocorra.</span><span class="sxs-lookup"><span data-stu-id="22262-112">The **DllSurrogate** named-value must be specified for surrogate activation to occur.</span></span> <span data-ttu-id="22262-113">A ativação refere-se a chamadas para qualquer uma das seguintes funções de ativação:</span><span class="sxs-lookup"><span data-stu-id="22262-113">Activation refers to calls to any of the following activation functions:</span></span>

-   [<span data-ttu-id="22262-114">**CoGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="22262-114">**CoGetClassObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [<span data-ttu-id="22262-115">**CoCreateInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="22262-115">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="22262-116">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="22262-116">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="22262-117">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="22262-117">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [<span data-ttu-id="22262-118">**IMoniker::BindToObject**</span><span class="sxs-lookup"><span data-stu-id="22262-118">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

<span data-ttu-id="22262-119">Para iniciar uma instância do substituto fornecido pelo sistema, defina o valor de **DllSurrogate** como uma cadeia de caracteres vazia ou como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="22262-119">To launch an instance of the system-supplied surrogate, set the value of **DllSurrogate** either to an empty string or to **NULL**.</span></span> <span data-ttu-id="22262-120">Para especificar o início de um substituto personalizado, defina o valor para o caminho do substituto.</span><span class="sxs-lookup"><span data-stu-id="22262-120">To specify the launch of a custom surrogate, set the value to the path of the surrogate.</span></span>

<span data-ttu-id="22262-121">Se [RemoteServerName](remoteservername.md) e **DllSurrogate** forem especificados para a mesma AppID, o valor de **RemoteServerName** será ignorado e o valor **DllSurrogate** causará uma ativação no computador local.</span><span class="sxs-lookup"><span data-stu-id="22262-121">If both [RemoteServerName](remoteservername.md) and **DllSurrogate** are specified for the same AppID, the **RemoteServerName** value is ignored and the **DllSurrogate** value causes an activation on the local computer.</span></span> <span data-ttu-id="22262-122">Para ativação alternativa remota, especifique **RemoteServerName** , mas não **DllSurrogate** no cliente, e especifique **DllSurrogate** no servidor.</span><span class="sxs-lookup"><span data-stu-id="22262-122">For remote surrogate activation, specify **RemoteServerName** but not **DllSurrogate** on the client, and specify **DllSurrogate** on the server.</span></span>

<span data-ttu-id="22262-123">Um servidor DLL que é projetado para ser sempre executado sozinho em seu próprio processo substituto é melhor configurado com um AppID igual a seu CLSID.</span><span class="sxs-lookup"><span data-stu-id="22262-123">A DLL server that is designed to always run alone in its own surrogate process is best configured with an AppID equal its CLSID.</span></span> <span data-ttu-id="22262-124">Em **AppID**, basta especificar um valor nomeado **DllSurrogate** com um valor de cadeia de caracteres vazio.</span><span class="sxs-lookup"><span data-stu-id="22262-124">Under **AppID**, simply specify a **DllSurrogate** named-value with an empty string value.</span></span>

<span data-ttu-id="22262-125">É melhor configurar um servidor DLL que foi projetado para ser executado sozinho em seu próprio processo substituto e para atender a vários clientes em uma rede com um valor [runas](runas.md) especificado na chave do registro **AppID** .</span><span class="sxs-lookup"><span data-stu-id="22262-125">It is best to configure a DLL server that is designed to run alone in its own surrogate process and to service multiple clients across a network with a [RunAs](runas.md) value specified under the **AppID** registry key.</span></span> <span data-ttu-id="22262-126">Se o **runas** especifica "usuário interativo" ou uma identidade de usuário específica depende da interface do usuário, da segurança e de outros requisitos do servidor.</span><span class="sxs-lookup"><span data-stu-id="22262-126">Whether the **RunAs** specifies "Interactive User" or a specific user identity depends upon the user interface, security, and other server requirements.</span></span> <span data-ttu-id="22262-127">Quando um valor **runas** é especificado, apenas uma instância do servidor é carregada para atender a todos os clientes, independentemente da identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="22262-127">When a **RunAs** value is specified, only one instance of the server is loaded to service all of the clients, regardless of the identity of the client.</span></span> <span data-ttu-id="22262-128">Por outro lado, não configure o servidor com **runas** se a intenção for ter uma instância do servidor dll em execução em substituto para atender a cada identidade de cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="22262-128">On the other hand, do not configure the server with **RunAs** if the intention is to have one instance of the DLL server running in surrogate to service each remote client identity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22262-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22262-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22262-130">Requisitos do servidor DLL</span><span class="sxs-lookup"><span data-stu-id="22262-130">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="22262-131">Compartilhamento substituto</span><span class="sxs-lookup"><span data-stu-id="22262-131">Surrogate Sharing</span></span>](surrogate-sharing.md)
</dt> </dl>

 

 