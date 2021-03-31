---
title: API C++ do WinRM
description: As interfaces de Gerenciamento Remoto do Windows podem ser usadas para obter dados ou gerenciar recursos em um computador remoto. Essa API é destinada principalmente para uso interno. É recomendável usar a API do shell do cliente WinRM, em vez disso, sempre que possível.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916430"
---
# <a name="winrm-c-api"></a><span data-ttu-id="b3d8e-105">API C++ do WinRM</span><span class="sxs-lookup"><span data-stu-id="b3d8e-105">WinRM C++ API</span></span>

<span data-ttu-id="b3d8e-106">As interfaces de Gerenciamento Remoto do Windows podem ser usadas para obter dados ou gerenciar [*recursos*](windows-remote-management-glossary.md) em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-106">The Windows Remote Management interfaces can be used to obtain data or manage [*resources*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="b3d8e-107">Essa API é destinada principalmente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-107">This API is intended primarily for internal use.</span></span> <span data-ttu-id="b3d8e-108">É recomendável usar a [API do shell do cliente WinRM](client-shell-api.md) , em vez disso, sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-108">We recommend using the [WinRM Client Shell API](client-shell-api.md) instead whenever possible.</span></span> <span data-ttu-id="b3d8e-109">As interfaces correspondem exatamente à [API de script do WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b3d8e-109">The interfaces closely correspond to the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="b3d8e-110">As interfaces do WinRM que herdam diretamente do **IDispatch** têm um objeto de script correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-110">The WinRM interfaces that inherit directly from **IDispatch** each have a corresponding scripting object.</span></span> <span data-ttu-id="b3d8e-111">Para obter mais informações, consulte a [API de script do WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b3d8e-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="b3d8e-112">Para aplicativos multissegmentados, o WinRM não dá suporte a threads separados que acessam o mesmo objeto [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .</span><span class="sxs-lookup"><span data-stu-id="b3d8e-112">For multithreaded applications, WinRM does not support separate threads accessing the same [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) object.</span></span>

<span data-ttu-id="b3d8e-113">As interfaces a seguir são fornecidas pelo WinRM.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-113">The following interfaces are provided by WinRM.</span></span>

<dl> <dt>

<span data-ttu-id="b3d8e-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="b3d8e-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="b3d8e-115">Fornece métodos e propriedades usados para criar uma nova sessão e gerenciar uma sessão estabelecida.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-115">Provides methods and properties used to create a new session and manage an established session.</span></span> <span data-ttu-id="b3d8e-116">[**WSMan**](wsman.md) é o objeto de script correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-116">[**WSMan**](wsman.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="b3d8e-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="b3d8e-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="b3d8e-118">Fornece métodos e propriedades usados para criar um novo [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="b3d8e-118">Provides methods and properties used to create a new [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span> <span data-ttu-id="b3d8e-119">Esse método está disponível para o objeto de script do [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="b3d8e-119">This method is available for the [**WSMan**](wsman.md) scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="b3d8e-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span><span class="sxs-lookup"><span data-stu-id="b3d8e-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span></span>
</dt> <dd>

<span data-ttu-id="b3d8e-121">Define o nome de usuário e a senha usados para conexões remotas.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-121">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="b3d8e-122">[**ConnectionOptions**](connectionoptions.md) é o objeto de script correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-122">[**ConnectionOptions**](connectionoptions.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="b3d8e-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="b3d8e-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span></span>
</dt> <dd>

<span data-ttu-id="b3d8e-124">Define as operações de rede e as propriedades disponíveis para a sessão.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-124">Defines the network operations and properties available for the session.</span></span> <span data-ttu-id="b3d8e-125">[**Session**](session.md) é o objeto de script correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-125">[**Session**](session.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="b3d8e-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span><span class="sxs-lookup"><span data-stu-id="b3d8e-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span></span>
</dt> <dd>

<span data-ttu-id="b3d8e-127">Representa uma coleção de resultados retornados da enumeração de um recurso.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-127">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="b3d8e-128">O [**enumerador**](enumerator.md) é o objeto de script correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-128">[**Enumerator**](enumerator.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="b3d8e-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="b3d8e-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span></span>
</dt> <dd>

<span data-ttu-id="b3d8e-130">Fornece o caminho para um recurso.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-130">Supplies the path to a resource.</span></span> <span data-ttu-id="b3d8e-131">Você pode usar um objeto [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) em vez de um [*URI de recurso*](windows-remote-management-glossary.md) em operações de objeto de [**sessão**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="b3d8e-131">You can use an [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="b3d8e-132">[**ResourceLocator**](resourcelocator.md) é o objeto de script correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-132">[**ResourceLocator**](resourcelocator.md) is the corresponding scripting object.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b3d8e-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3d8e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3d8e-134">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="b3d8e-134">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




