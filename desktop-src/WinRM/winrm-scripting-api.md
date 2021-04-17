---
title: API de script do WinRM
description: Gerenciamento Remoto do Windows objetos de script são implementados como uma camada acima do protocolo WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782473"
---
# <a name="winrm-scripting-api"></a><span data-ttu-id="01930-103">API de script do WinRM</span><span class="sxs-lookup"><span data-stu-id="01930-103">WinRM Scripting API</span></span>

<span data-ttu-id="01930-104">Gerenciamento Remoto do Windows objetos de script são implementados como uma camada acima da [protocolo WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="01930-104">Windows Remote Management scripting objects are implemented as a layer above the [WS-Management Protocol](ws-management-protocol.md).</span></span> <span data-ttu-id="01930-105">Os objetos de script permitem que você obtenha dados ou gerencie [*recursos*](windows-remote-management-glossary.md) em computadores locais e remotos.</span><span class="sxs-lookup"><span data-stu-id="01930-105">The scripting objects enable you to obtain data or manage [*resources*](windows-remote-management-glossary.md) on local and remote computers.</span></span>

## <a name="ws-management-objects"></a><span data-ttu-id="01930-106">Objetos WS-Management</span><span class="sxs-lookup"><span data-stu-id="01930-106">WS-Management Objects</span></span>

<span data-ttu-id="01930-107">Cada objeto de script tem uma interface C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="01930-107">Each scripting object has a corresponding C++ interface.</span></span> <span data-ttu-id="01930-108">Para obter mais informações, consulte [API C++ do WinRM](winrm-c---api.md) e [scripts em gerenciamento remoto do Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="01930-108">For more information, see [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="01930-109">Os objetos a seguir são fornecidos pela API de script do WinRM.</span><span class="sxs-lookup"><span data-stu-id="01930-109">The following objects are provided by the WinRM Scripting API.</span></span>

<dl> <dt>

<span data-ttu-id="01930-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span><span class="sxs-lookup"><span data-stu-id="01930-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span></span>
</dt> <dd>

<span data-ttu-id="01930-111">Define o nome de usuário e a senha usados para conexões remotas.</span><span class="sxs-lookup"><span data-stu-id="01930-111">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="01930-112">O nome de usuário e a senha são passados ao chamar o método [**Createconnectoptions**](wsman-createconnectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="01930-112">The user name and password are passed when calling the [**CreateConnectionOptions**](wsman-createconnectionoptions.md) method.</span></span> <span data-ttu-id="01930-113">Para obter mais informações, consulte [obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="01930-113">For more information, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="01930-114">A interface C++ correspondente é [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span><span class="sxs-lookup"><span data-stu-id="01930-114">The corresponding C++ interface is [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span></span>

</dd> <dt>

<span data-ttu-id="01930-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumera**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="01930-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span></span>
</dt> <dd>

<span data-ttu-id="01930-116">Representa uma coleção de resultados retornados da enumeração de um recurso.</span><span class="sxs-lookup"><span data-stu-id="01930-116">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="01930-117">Para obter mais informações, consulte [enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="01930-117">For more information, see [Enumerating or Listing All the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span> <span data-ttu-id="01930-118">A interface C++ correspondente é [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="01930-118">The corresponding C++ interface is [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="01930-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span><span class="sxs-lookup"><span data-stu-id="01930-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span></span>
</dt> <dd>

<span data-ttu-id="01930-120">Fornece o caminho para um recurso.</span><span class="sxs-lookup"><span data-stu-id="01930-120">Supplies the path to a resource.</span></span> <span data-ttu-id="01930-121">Você pode usar um objeto [**ResourceLocator**](resourcelocator.md) em vez de um [*URI de recurso*](windows-remote-management-glossary.md) em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="01930-121">You can use a [**ResourceLocator**](resourcelocator.md) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations, such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="01930-122">A interface C++ correspondente é [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="01930-122">The corresponding C++ interface is [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span>

</dd> <dt>

<span data-ttu-id="01930-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sessão**](session.md)</span><span class="sxs-lookup"><span data-stu-id="01930-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span></span>
</dt> <dd>

<span data-ttu-id="01930-124">Define as operações de rede e as propriedades disponíveis para a sessão, como [**Session. Get**](session-get.md), [**Session. Enumerate**](session-enumerate.md), [**Session. Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="01930-124">Defines the network operations and properties available for the session, such as [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md).</span></span> <span data-ttu-id="01930-125">Para obter mais informações, consulte [obtendo dados do computador local](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="01930-125">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span> <span data-ttu-id="01930-126">A interface C++ correspondente é [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span><span class="sxs-lookup"><span data-stu-id="01930-126">The corresponding C++ interface is [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span></span>

</dd> <dt>

<span data-ttu-id="01930-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span><span class="sxs-lookup"><span data-stu-id="01930-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span></span>
</dt> <dd>

<span data-ttu-id="01930-128">Fornece métodos e propriedades usados para criar uma nova sessão ou gerenciar uma sessão estabelecida.</span><span class="sxs-lookup"><span data-stu-id="01930-128">Provides methods and properties used to create a new session or manage an established session.</span></span> <span data-ttu-id="01930-129">Para obter mais informações, consulte [usando gerenciamento remoto do Windows](using-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="01930-129">For more information see, [Using Windows Remote Management](using-windows-remote-management.md).</span></span> <span data-ttu-id="01930-130">As interfaces C++ correspondentes são [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span><span class="sxs-lookup"><span data-stu-id="01930-130">The corresponding C++ interfaces are [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="01930-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01930-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01930-132">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="01930-132">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01930-133">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="01930-133">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01930-134">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="01930-134">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01930-135">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="01930-135">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




