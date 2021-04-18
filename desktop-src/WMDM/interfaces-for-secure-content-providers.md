---
title: Interfaces para provedores de conteúdo seguro
description: Interfaces para provedores de conteúdo seguro
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- referência de programação, conteúdo protegido por DRM
- referência para Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Conteúdo protegido por DRM
- Windows Media Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- referência de programação, provedor de conteúdo seguro (SCP)
- referência para Windows Media Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- provedor de conteúdo seguro (SCP)
- SCP (provedor de conteúdo seguro)
- Windows Media Gerenciador de Dispositivos, interfaces SCP
- Gerenciador de Dispositivos, interfaces SCP
- referência de programação, interfaces SCP
- referência para Windows Media Gerenciador de Dispositivos, interfaces SCP
- Interfaces SCP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788810"
---
# <a name="interfaces-for-secure-content-providers"></a><span data-ttu-id="b5547-119">Interfaces para provedores de conteúdo seguro</span><span class="sxs-lookup"><span data-stu-id="b5547-119">Interfaces for Secure Content Providers</span></span>

<span data-ttu-id="b5547-120">Um SCP (provedor de conteúdo seguro) é um componente de plug-in que permite que o Windows Media Gerenciador de Dispositivos transfira e solicite informações de direitos do conteúdo protegido por DRM.</span><span class="sxs-lookup"><span data-stu-id="b5547-120">A secure content provider (SCP) is a plug-in component that enables Windows Media Device Manager to transfer and request rights information from DRM-protected content.</span></span> <span data-ttu-id="b5547-121">A Microsoft fornece um componente SCP que pode manipular arquivos WMA e WMV protegidos por DRM.</span><span class="sxs-lookup"><span data-stu-id="b5547-121">Microsoft provides an SCP component that can handle DRM-protected WMA and WMV files.</span></span> <span data-ttu-id="b5547-122">Se seu dispositivo ou aplicativo usar o conteúdo protegido por DRM de outros formatos, ele deverá criar um componente SCP implementando todas essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="b5547-122">If your device or application will use DRM-protected content of other formats, it should create an SCP component by implementing all of these interfaces.</span></span> <span data-ttu-id="b5547-123">Caso contrário, não será necessário usar essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="b5547-123">Otherwise, you will not need to use these interfaces.</span></span>



| <span data-ttu-id="b5547-124">Interface</span><span class="sxs-lookup"><span data-stu-id="b5547-124">Interface</span></span>                                                  | <span data-ttu-id="b5547-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5547-125">Description</span></span>                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5547-126">**ISCPSecureAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="b5547-126">**ISCPSecureAuthenticate**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | <span data-ttu-id="b5547-127">A principal interface do provedor de conteúdo seguro.</span><span class="sxs-lookup"><span data-stu-id="b5547-127">The primary interface of the secure content provider.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="b5547-128">**ISCPSecureAuthenticate2**</span><span class="sxs-lookup"><span data-stu-id="b5547-128">**ISCPSecureAuthenticate2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | <span data-ttu-id="b5547-129">Estende o **ISCPSecureAuthenticate** fornecendo uma maneira de obter um objeto de sessão.</span><span class="sxs-lookup"><span data-stu-id="b5547-129">Extends **ISCPSecureAuthenticate** by providing a way to get a session object.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="b5547-130">**ISCPSecureExchange**</span><span class="sxs-lookup"><span data-stu-id="b5547-130">**ISCPSecureExchange**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | <span data-ttu-id="b5547-131">Usado para trocar conteúdo protegido e direitos associados ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b5547-131">Used to exchange secured content and rights associated with content.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="b5547-132">**ISCPSecureExchange2**</span><span class="sxs-lookup"><span data-stu-id="b5547-132">**ISCPSecureExchange2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | <span data-ttu-id="b5547-133">Estende o **ISCPSecureExchange** fornecendo uma nova versão do método **TransferContainerData** .</span><span class="sxs-lookup"><span data-stu-id="b5547-133">Extends **ISCPSecureExchange** by providing a new version of the **TransferContainerData** method.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="b5547-134">**ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="b5547-134">**ISCPSecureExchange3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | <span data-ttu-id="b5547-135">Estende o **ISCPSecureExchange2** fornecendo um desempenho de troca de dados aprimorado e um método de retorno de chamada de transferência completa.</span><span class="sxs-lookup"><span data-stu-id="b5547-135">Extends **ISCPSecureExchange2** by providing improved data exchange performance, and a transfer complete callback method.</span></span>                                                                                                                            |
| [<span data-ttu-id="b5547-136">**ISCPSecureQuery**</span><span class="sxs-lookup"><span data-stu-id="b5547-136">**ISCPSecureQuery**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | <span data-ttu-id="b5547-137">Consultado pelo Windows Media Gerenciador de Dispositivos para determinar a propriedade do conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="b5547-137">Queried by Windows Media Device Manager to determine ownership of secured content.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="b5547-138">**ISCPSecureQuery2**</span><span class="sxs-lookup"><span data-stu-id="b5547-138">**ISCPSecureQuery2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | <span data-ttu-id="b5547-139">Estende o **ISCPSecureQuery** por meio de funcionalidade que determina se o provedor de conteúdo seguro é responsável pelo conteúdo e, nesse caso, fornece uma URL para atualizar os componentes revogados e determinar quais componentes foram revogados.</span><span class="sxs-lookup"><span data-stu-id="b5547-139">Extends **ISCPSecureQuery** through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.</span></span> |
| [<span data-ttu-id="b5547-140">**ISCPSecureQuery3**</span><span class="sxs-lookup"><span data-stu-id="b5547-140">**ISCPSecureQuery3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | <span data-ttu-id="b5547-141">Estende o **ISCPSecureQuery2** fornecendo um conjunto de novos métodos para recuperar os direitos e tomar decisão em um canal claro.</span><span class="sxs-lookup"><span data-stu-id="b5547-141">Extends **ISCPSecureQuery2** by providing a set of new methods for retrieving the rights and making decision on a clear channel.</span></span>                                                                                                                     |
| [<span data-ttu-id="b5547-142">**ISCPSession**</span><span class="sxs-lookup"><span data-stu-id="b5547-142">**ISCPSession**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | <span data-ttu-id="b5547-143">Fornece gerenciamento de Estado comum eficiente para várias operações.</span><span class="sxs-lookup"><span data-stu-id="b5547-143">Provides efficient common state management for multiple operations.</span></span>                                                                                                                                                                                  |



 

 

 




