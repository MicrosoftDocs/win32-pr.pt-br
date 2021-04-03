---
title: O que há de novo (SDK do Windows Media Format 11)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- SDK do Windows Media Format, o que há de novo
- SDK do Windows Media Format, recursos
- SDK do Windows Media Format, novos recursos
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, atualizações de DRM
- SDK do Windows Media Format, atualizações de codec
- SDK do Windows Media Format, imagens em miniatura
- DRM (gerenciamento de direitos digitais), novos recursos
- DRM (gerenciamento de direitos digitais), novos recursos
- imagens em miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644150"
---
# <a name="whats-new-windows-media-format-11-sdk"></a><span data-ttu-id="dd20a-113">O que há de novo (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="dd20a-113">What's New (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="dd20a-114">O SDK do Windows Media Format 11 introduz novos recursos de DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="dd20a-114">The Windows Media Format 11 SDK introduces new digital rights management (DRM) features.</span></span> <span data-ttu-id="dd20a-115">As alterações a seguir foram feitas no SDK desde a versão 9,5.</span><span class="sxs-lookup"><span data-stu-id="dd20a-115">The following changes have been made to the SDK since the 9.5 release.</span></span>

## <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="dd20a-116">APIs estendidas do cliente DRM do Windows Media</span><span class="sxs-lookup"><span data-stu-id="dd20a-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="dd20a-117">O SDK do Windows Media Format 11 é fornecido com um novo conjunto de APIs DRM.</span><span class="sxs-lookup"><span data-stu-id="dd20a-117">The Windows Media Format 11 SDK ships with a new set of DRM APIs.</span></span> <span data-ttu-id="dd20a-118">Essas APIs são implementadas em sua própria biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dd20a-118">These APIs are implemented in their own library.</span></span> <span data-ttu-id="dd20a-119">Muitos dos recursos DRM com suporte dos objetos do Windows Media Format SDK também são suportados pelas APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dd20a-119">Many of the DRM features supported by the objects of the Windows Media Format SDK are also supported by the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="dd20a-120">A principal diferença nas novas APIs é que elas não dependem de ter um arquivo ASF para funcionar.</span><span class="sxs-lookup"><span data-stu-id="dd20a-120">The primary difference in the new APIs is that they do not rely on having an ASF file to work.</span></span> <span data-ttu-id="dd20a-121">Em vez disso, as novas APIs lidam com o armazenamento de licença local diretamente, geralmente usando a ID de chave para identificar licenças.</span><span class="sxs-lookup"><span data-stu-id="dd20a-121">Instead, the new APIs deal with the local license store directly, often using the key ID to identify licenses.</span></span>

<span data-ttu-id="dd20a-122">Para obter mais informações, consulte a documentação de [APIs estendidas do cliente DRM do Windows Media](windows-media-drm-client-extended-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="dd20a-122">For more information, see the [Windows Media DRM Client Extended APIs](windows-media-drm-client-extended-apis.md) documentation.</span></span>

## <a name="updated-codecs"></a><span data-ttu-id="dd20a-123">Codecs atualizados</span><span class="sxs-lookup"><span data-stu-id="dd20a-123">Updated Codecs</span></span>

<span data-ttu-id="dd20a-124">O codec de perfil avançado do Windows Media Video 9 foi atualizado para produzir um fluxo de bits compactado compatível com o padrão SMPTE VC-1 publicado.</span><span class="sxs-lookup"><span data-stu-id="dd20a-124">The Windows Media Video 9 Advanced Profile codec has been updated to produce a compressed bit stream that is compliant with the published SMPTE VC-1 standard.</span></span>

<span data-ttu-id="dd20a-125">O codec Windows Media Audio 10 Professional também está incluído nesta versão do SDK.</span><span class="sxs-lookup"><span data-stu-id="dd20a-125">The Windows Media Audio 10 Professional codec is also included in this release of the SDK.</span></span> <span data-ttu-id="dd20a-126">O novo codec de áudio apresenta qualidade aprimorada a taxas de bits mais baixas.</span><span class="sxs-lookup"><span data-stu-id="dd20a-126">The new audio codec features improved quality at lower bit rates.</span></span>

## <a name="thumbnail-right"></a><span data-ttu-id="dd20a-127">Miniatura à direita</span><span class="sxs-lookup"><span data-stu-id="dd20a-127">Thumbnail Right</span></span>

<span data-ttu-id="dd20a-128">Os aplicativos podem solicitar uma nova ação de DRM para ler do vídeo para criar uma imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="dd20a-128">Applications can request a new DRM action to read from video to create a thumbnail image.</span></span> <span data-ttu-id="dd20a-129">Isso permite que os aplicativos criem e exibam imagens em miniatura para arquivos de vídeo sem abrir o arquivo para reprodução.</span><span class="sxs-lookup"><span data-stu-id="dd20a-129">This enables applications to create and display thumbnail images for video files without opening the file for playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd20a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd20a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd20a-131">**Sobre o SDK do Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="dd20a-131">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




