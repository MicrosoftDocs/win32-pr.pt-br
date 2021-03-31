---
title: Proteção de DRM e distribuição de licença de conteúdo
description: Proteção de DRM e distribuição de licença de conteúdo
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- SDK do Windows Media Format, proteção de conteúdo do DRM
- SDK do Windows Media Format, licenças DRM
- ASF (Advanced Systems Format), proteção de conteúdo de DRM
- ASF (formato de sistemas avançados), proteção de conteúdo de DRM
- ASF (Advanced Systems Format), distribuição de licença do DRM
- ASF (formato de sistemas avançados), distribuição de licença do DRM
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), distribuição de licenças
- DRM (gerenciamento de direitos digitais), distribuição de licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292830"
---
# <a name="drm-protection-and-content-license-distribution"></a><span data-ttu-id="3d185-113">Proteção de DRM e distribuição de licença de conteúdo</span><span class="sxs-lookup"><span data-stu-id="3d185-113">DRM Protection and Content License Distribution</span></span>

<span data-ttu-id="3d185-114">No lado da criação, a tecnologia de gerenciamento de direitos digitais envolve dois processos principais: (1) proteger o conteúdo e (2) fornecer licenças para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3d185-114">On the creation side, digital rights management technology involves two main processes: (1) protecting the content and (2) providing licenses for the content.</span></span> <span data-ttu-id="3d185-115">A proteção de um arquivo envolve basicamente a criptografia do conteúdo e a inclusão de uma URL no cabeçalho do arquivo que especifica onde uma licença para o conteúdo pode ser obtida.</span><span class="sxs-lookup"><span data-stu-id="3d185-115">Protecting a file basically involves encrypting the content, and including a URL in the file header that specifies where a license for the content may be obtained.</span></span> <span data-ttu-id="3d185-116">Se você quiser proteger arquivos com o e, em seguida, distribuir os arquivos para outros computadores ou dispositivos, poderá usar o SDK do Windows Media Format ou o SDK do Windows Media Rights Manager para proteger o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3d185-116">If you want to protect files with and then distribute the files to other computers or devices, you can use either the Windows Media Format SDK or the Windows Media Rights Manager SDK to protect the file.</span></span> <span data-ttu-id="3d185-117">Para cenários de DRM ao vivo, você deve usar o Windows Media Format SDK para proteger o conteúdo conforme ele está sendo codificado.</span><span class="sxs-lookup"><span data-stu-id="3d185-117">For live-DRM scenarios, you must use the Windows Media Format SDK to protect the content as it is being encoded.</span></span>

<span data-ttu-id="3d185-118">Para criar e emitir licenças para conteúdo protegido, você pode criar sua própria solução personalizada usando os objetos do SDK do Windows Media Rights Manager ou pode usar um serviço executado por terceiros.</span><span class="sxs-lookup"><span data-stu-id="3d185-118">To create and issue licenses for protected content, you can create your own custom solution using the objects of the Windows Media Rights Manager SDK, or you can use a service run by a third party.</span></span>

<span data-ttu-id="3d185-119">Seja qual for o método usado, os arquivos protegidos que você criar conterão, no objeto de cabeçalho DRM, uma URL que informa aos aplicativos cliente onde obter uma licença para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3d185-119">Whichever method you use, the protected files that you create will contain, in the DRM header object, a URL that tells client applications where to obtain a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="3d185-120">O Windows Media Format SDK não oferece suporte para a criação ou a emissão de licenças.</span><span class="sxs-lookup"><span data-stu-id="3d185-120">The Windows Media Format SDK does not provide support for creating or issuing licenses.</span></span>

 

<span data-ttu-id="3d185-121">No lado da reprodução, um aplicativo habilitado para DRM deve ser capaz de obter licenças para conteúdo protegido, descriptografar o conteúdo usando a chave contida na licença e impor as restrições de licença, como o número de vezes que um arquivo pode ser reproduzido ou se o arquivo pode ser copiado para outro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d185-121">On the playback side, a DRM-enabled application must be able to obtain licenses for protected content, to decrypt that content using the key contained in the license, and to enforce the license restrictions, such as the number of times a file may be played, or whether the file can be copied to another device.</span></span> <span data-ttu-id="3d185-122">O SDK do Windows Media Format fornece todo o suporte necessário para criar um aplicativo de reprodução de DRM totalmente habilitado.</span><span class="sxs-lookup"><span data-stu-id="3d185-122">The Windows Media Format SDK provides all the support required to create a fully enabled DRM playback application.</span></span>

> [!Note]  
> <span data-ttu-id="3d185-123">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="3d185-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3d185-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d185-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d185-125">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="3d185-125">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="3d185-126">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="3d185-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




