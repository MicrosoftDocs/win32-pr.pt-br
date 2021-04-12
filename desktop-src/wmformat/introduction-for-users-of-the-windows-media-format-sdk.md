---
title: Introdução para usuários do Windows Media Format SDK
description: Introdução para usuários do Windows Media Format SDK
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- APIs estendidas do cliente DRM, sobre
- APIs estendidas do cliente, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364045"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a><span data-ttu-id="4a5fc-116">Introdução para usuários do Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="4a5fc-116">Introduction for Users of the Windows Media Format SDK</span></span>

<span data-ttu-id="4a5fc-117">Grande parte da funcionalidade fornecida pelas APIs estendidas do cliente DRM do Windows Media é a mesma que a funcionalidade fornecida pelos objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-117">Much of the functionality provided by the Windows Media DRM Client Extended APIs is the same as the functionality provided by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="4a5fc-118">O Windows Media Format SDK fornece aos desenvolvedores os objetos necessários para criar, acessar e manipular arquivos de mídia que usam a estrutura de arquivos ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="4a5fc-118">The Windows Media Format SDK provides developers with the objects needed to create, access, and manipulate media files that use the Advanced Systems Format (ASF) file structure.</span></span> <span data-ttu-id="4a5fc-119">Como o DRM do Windows Media destina-se a proteger arquivos ASF, a funcionalidade DRM do lado do cliente foi incluída no Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-119">Because Windows Media DRM is intended to protect ASF files, client-side DRM functionality was included in the Windows Media Format SDK.</span></span>

<span data-ttu-id="4a5fc-120">As APIs estendidas do cliente DRM do Windows Media estão sendo lançadas em conjunto com a plataforma de mídia digital de última geração da Microsoft, o SDK do Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-120">The Windows Media DRM Client Extended APIs are being released in conjunction with Microsoft's next-generation digital media platform, the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="4a5fc-121">Media Foundation incluirá a funcionalidade do ASF que sobrepõe alguns dos recursos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-121">Media Foundation will include ASF functionality that overlaps some of the features of the Windows Media Format SDK.</span></span> <span data-ttu-id="4a5fc-122">Como agora há dois SDKs da Microsoft que manipulam arquivos ASF, a funcionalidade DRM do lado do cliente está sendo separada do SDK do Windows Media Format para as APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-122">Because there are now two Microsoft SDKs that manipulate ASF files, the client-side DRM functionality is being separated from the Windows Media Format SDK into the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="4a5fc-123">Essas APIs podem ser acessadas por usuários do Windows Media Format SDK e do SDK do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-123">These APIs can be accessed by users of both the Windows Media Format SDK and the Media Foundation SDK.</span></span> <span data-ttu-id="4a5fc-124">No momento, essas APIs são incluídas como parte do pacote de instalação do Windows Media Format SDK e são documentadas como parte do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-124">At present, these APIs are included as part of the Windows Media Format SDK installation package and are documented as part of the Windows Media Format SDK.</span></span> <span data-ttu-id="4a5fc-125">No entanto, as APIs estendidas do cliente Windows Media DRM são implementadas em sua própria biblioteca e têm seu próprio arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-125">However, the Windows Media DRM Client Extended APIs are implemented in their own library and have their own header file.</span></span> <span data-ttu-id="4a5fc-126">Depois de instalar o SDK do Windows Media Format, essas APIs podem ser usadas por conta própria, sem incluir cabeçalhos ou bibliotecas do Windows Media Format SDK em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-126">After installing the Windows Media Format SDK, these APIs can be used one their own, without including any Windows Media Format SDK headers or libraries in your application.</span></span>

<span data-ttu-id="4a5fc-127">Se você desenvolver aplicativos que usam o SDK do Windows Media Format, deverá decidir se usará a funcionalidade DRM fornecida pelo SDK ou usará as APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-127">If you develop applications that use the Windows Media Format SDK you must decide whether to use the DRM functionality that SDK provides, or to use the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="4a5fc-128">Embora muitos dos recursos desses dois SDKs sejam muito semelhantes, as APIs estendidas do cliente Windows Media DRM oferecem os seguintes recursos não disponíveis para os usuários das rotinas de DRM mais antigas:</span><span class="sxs-lookup"><span data-stu-id="4a5fc-128">While many of the features of these two SDKs are very similar, the Windows Media DRM Client Extended APIs offer the following features not available to users of the older DRM routines:</span></span>

-   <span data-ttu-id="4a5fc-129">Capacidade de importar conteúdo protegido por um sistema de gerenciamento de direitos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-129">Ability to import content protected by a third-party rights management system.</span></span>
-   <span data-ttu-id="4a5fc-130">Capacidade de exportar conteúdo protegido pelo Windows Media DRM para um sistema de gerenciamento de direitos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-130">Ability to export content protected by Windows Media DRM to a third-party rights management system.</span></span>
-   <span data-ttu-id="4a5fc-131">Enumeração direta de licenças no repositório de licenças.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-131">Direct enumeration of licenses in the license store.</span></span>
-   <span data-ttu-id="4a5fc-132">Direitos simples e agregados consultam com base na ID da chave (sem necessidade de carregar o arquivo de mídia).</span><span class="sxs-lookup"><span data-stu-id="4a5fc-132">Simple, aggregated rights querying based on key ID (no need to load the media file).</span></span>
-   <span data-ttu-id="4a5fc-133">Capacidade de renovar componentes revogados usando a interface de Media Foundation padrão, **IMFContentEnabler**.</span><span class="sxs-lookup"><span data-stu-id="4a5fc-133">Ability to renew revoked components by using the standard Media Foundation interface, **IMFContentEnabler**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a5fc-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a5fc-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a5fc-135">**Sobre as APIs estendidas do cliente DRM do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4a5fc-135">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




