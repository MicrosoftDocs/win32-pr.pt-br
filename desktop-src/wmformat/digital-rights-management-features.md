---
title: Recursos de Rights Management digital
description: Recursos de Rights Management digital
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- SDK do Windows Media Format, recursos do DRM
- DRM (gerenciamento de direitos digitais), recursos
- DRM (gerenciamento de direitos digitais), recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641277"
---
# <a name="digital-rights-management-features"></a><span data-ttu-id="01c95-106">Recursos de Rights Management digital</span><span class="sxs-lookup"><span data-stu-id="01c95-106">Digital Rights Management Features</span></span>

<span data-ttu-id="01c95-107">\[O recurso DRM do Windows Media foi preterido e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="01c95-107">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="01c95-108">Em vez disso, use [o Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="01c95-108">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="01c95-109">O DRM (gerenciamento de direitos digitais) é uma tecnologia que os proprietários de conteúdo podem usar para proteger arquivos de mídia digital criptografando-os com uma chave (um dado que bloqueia e desbloqueia o conteúdo).</span><span class="sxs-lookup"><span data-stu-id="01c95-109">Digital rights management (DRM) is a technology that content owners can use to protect digital media files by encrypting them with a key (a piece of data that locks and unlocks the content).</span></span> <span data-ttu-id="01c95-110">Para reproduzir um arquivo ASF protegido, um consumidor deve obter uma licença separada que contém a chave.</span><span class="sxs-lookup"><span data-stu-id="01c95-110">To play a protected ASF file, a consumer must obtain a separate license containing the key.</span></span> <span data-ttu-id="01c95-111">Cada licença também contém direitos, determinados pelo proprietário do conteúdo ou pelo emissor da licença, que especificam como o consumidor pode usar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="01c95-111">Each license also contains rights, determined by the content owner or license issuer, which specify how the consumer can use the file.</span></span> <span data-ttu-id="01c95-112">Usando a tecnologia DRM, os proprietários de conteúdo podem entregar músicas, vídeos e outros arquivos de mídia digital pela Internet em um formato de arquivo protegido e controlar o uso de seu conteúdo digital.</span><span class="sxs-lookup"><span data-stu-id="01c95-112">Using DRM technology, content owners can deliver songs, videos, and other digital media files over the Internet in a protected file format and control the use of their digital content.</span></span> <span data-ttu-id="01c95-113">A tecnologia Microsoft DRM também tem suporte do Windows Media Rights Manager, do Windows Media Encoder e do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="01c95-113">Microsoft DRM technology is also supported by the Windows Media Rights Manager, the Windows Media Encoder, and Windows Media Player.</span></span> <span data-ttu-id="01c95-114">Para obter mais informações básicas sobre a tecnologia DRM da Microsoft, consulte o [site do Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).</span><span class="sxs-lookup"><span data-stu-id="01c95-114">For more background information on Microsoft's DRM technology, see the [Microsoft Windows Media Web site](https://support.microsoft.com/help/17946/windows-media).</span></span>

> [!Note]  
> <span data-ttu-id="01c95-115">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="01c95-115">DRM is not supported by the x64-based version of this SDK.</span></span>

 

<span data-ttu-id="01c95-116">As seções a seguir discutem os principais recursos relacionados ao DRM do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="01c95-116">The following sections discuss the main DRM-related features of the Windows Media Format SDK.</span></span>



| <span data-ttu-id="01c95-117">Seção</span><span class="sxs-lookup"><span data-stu-id="01c95-117">Section</span></span>                                                                                            | <span data-ttu-id="01c95-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="01c95-118">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01c95-119">Noções básicas de DRM</span><span class="sxs-lookup"><span data-stu-id="01c95-119">DRM Basics</span></span>](drm-basics.md)                                                                       | <span data-ttu-id="01c95-120">Fornece uma breve visão geral da funcionalidade DRM fornecida pelo Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="01c95-120">Provides a brief overview of the DRM functionality provided by the Windows Media Format SDK.</span></span>                                         |
| [<span data-ttu-id="01c95-121">Versões de DRM</span><span class="sxs-lookup"><span data-stu-id="01c95-121">DRM Versions</span></span>](drm-versions.md)                                                                   | <span data-ttu-id="01c95-122">Descreve as principais diferenças entre as versões de proteção de DRM disponíveis para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="01c95-122">Describes the main differences between the versions of DRM protection available to applications.</span></span>                                     |
| [<span data-ttu-id="01c95-123">DRM ao vivo</span><span class="sxs-lookup"><span data-stu-id="01c95-123">Live DRM</span></span>](live-drm.md)                                                                           | <span data-ttu-id="01c95-124">Descreve os cenários possibilitados pela proteção de DRM "em tempo real".</span><span class="sxs-lookup"><span data-stu-id="01c95-124">Describes the scenarios made possible by "on the fly" DRM protection.</span></span>                                                                |
| [<span data-ttu-id="01c95-125">Individualização de DRM</span><span class="sxs-lookup"><span data-stu-id="01c95-125">DRM Individualization</span></span>](drm-individualization.md)                                                 | <span data-ttu-id="01c95-126">Descreve a atualização de segurança do aplicativo que os proprietários de conteúdo do DRM ou os emissores de licença podem exigir.</span><span class="sxs-lookup"><span data-stu-id="01c95-126">Describes the application security upgrade that DRM content owners or license issuers can require.</span></span>                                   |
| [<span data-ttu-id="01c95-127">Fazendo backup e restaurando licenças DRM</span><span class="sxs-lookup"><span data-stu-id="01c95-127">Backing Up and Restoring of DRM Licenses</span></span>](backing-up-and-restoring-of-drm-licenses.md)           | <span data-ttu-id="01c95-128">Descreve os prós e contras de permitir que os usuários façam backup e restaure suas licenças de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="01c95-128">Describes the pros and cons of permitting users to back up and restore their content licenses.</span></span>                                       |
| [<span data-ttu-id="01c95-129">Exibindo atributos DRM no editor de metadados</span><span class="sxs-lookup"><span data-stu-id="01c95-129">Viewing DRM Attributes in the Metadata Editor</span></span>](viewing-drm-attributes-in-the-metadata-editor.md) | <span data-ttu-id="01c95-130">Descreve os recursos desse objeto auxiliar DRM e os cenários para os quais ele foi projetado para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="01c95-130">Describes the capabilities of this DRM helper object and the scenarios it was designed to support.</span></span>                                   |
| [<span data-ttu-id="01c95-131">Níveis de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="01c95-131">Output Protection Levels</span></span>](output-protection-levels.md)                                           | <span data-ttu-id="01c95-132">Descreve como os níveis de proteção de saída tornam as licenças do DRM versão 10 mais flexíveis.</span><span class="sxs-lookup"><span data-stu-id="01c95-132">Describes how Output Protection Levels make DRM version 10 licenses more flexible.</span></span>                                                   |
| [<span data-ttu-id="01c95-133">Revogação de licença</span><span class="sxs-lookup"><span data-stu-id="01c95-133">License Revocation</span></span>](license-revocation.md)                                                       | <span data-ttu-id="01c95-134">Descreve a revogação de licenças.</span><span class="sxs-lookup"><span data-stu-id="01c95-134">Describes license revocation.</span></span>                                                                                                        |
| [<span data-ttu-id="01c95-135">Windows Media DRM 10 para dispositivos de rede</span><span class="sxs-lookup"><span data-stu-id="01c95-135">Windows Media DRM 10 for Network Devices</span></span>](windows-media-drm-10-for-network-devices.md)           | <span data-ttu-id="01c95-136">Apresenta o Windows Media DRM 10 para dispositivos de rede e sua implementação neste SDK.</span><span class="sxs-lookup"><span data-stu-id="01c95-136">Introduces Windows Media DRM 10 for Network Devices and its implementation in this SDK.</span></span>                                              |
| [<span data-ttu-id="01c95-137">Caminho de áudio seguro da Microsoft</span><span class="sxs-lookup"><span data-stu-id="01c95-137">Microsoft Secure Audio Path</span></span>](microsoft-secure-audio-path--deprecated.md)                         | <span data-ttu-id="01c95-138">Descreve a arquitetura de caminho de áudio seguro da Microsoft, que fornece o nível mais alto de proteção para conteúdo de áudio protegido.</span><span class="sxs-lookup"><span data-stu-id="01c95-138">Describes the Microsoft Secure Audio Path architecture, which provides the highest degree of protection for protected audio content.</span></span> |
| [<span data-ttu-id="01c95-139">Gravação de playlist</span><span class="sxs-lookup"><span data-stu-id="01c95-139">Playlist Burning</span></span>](playlist-burning.md)                                                           | <span data-ttu-id="01c95-140">Descreve o recurso de gravação de playlist do DRM e como ele tem suporte no Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="01c95-140">Describes the playlist-burning feature of DRM and how it is supported in the Windows Media Format SDK.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="01c95-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01c95-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01c95-142">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="01c95-142">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="01c95-143">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="01c95-143">**Features**</span></span>](features.md)
</dt> </dl>

 

 