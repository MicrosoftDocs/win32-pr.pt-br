---
title: Noções básicas de DRM
description: Noções básicas de DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- SDK do Windows Media Format, noções básicas de DRM
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), protegendo o conteúdo
- DRM (gerenciamento de direitos digitais), conteúdo de empacotamento
- DRM (gerenciamento de direitos digitais), conteúdo de empacotamento
- DRM (gerenciamento de direitos digitais), lendo conteúdo protegido
- DRM (gerenciamento de direitos digitais), lendo conteúdo protegido
- protegendo o conteúdo
- empacotando conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364435"
---
# <a name="drm-basics"></a><span data-ttu-id="66800-114">Noções básicas de DRM</span><span class="sxs-lookup"><span data-stu-id="66800-114">DRM Basics</span></span>

<span data-ttu-id="66800-115">As tecnologias DRM do Windows Media são bem simples da perspectiva do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="66800-115">The Windows Media DRM technologies are fairly simple from the perspective of the Windows Media Format SDK.</span></span> <span data-ttu-id="66800-116">Os componentes do SDK podem ser usados para proteger o conteúdo e para reproduzir conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="66800-116">Components of the SDK can be used to protect content and to play protected content.</span></span>

## <a name="protecting-content"></a><span data-ttu-id="66800-117">Protegendo conteúdo</span><span class="sxs-lookup"><span data-stu-id="66800-117">Protecting Content</span></span>

<span data-ttu-id="66800-118">Proteger o conteúdo (também chamado de conteúdo de empacotamento) envolve criptografar a seção de dados do arquivo e incluir algumas informações no cabeçalho do arquivo que permite que os jogadores descriptografem o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="66800-118">Protecting content (also called packaging content) involves encrypting the data section of the file and including some information in the file header that enables players to decrypt the content.</span></span>

<span data-ttu-id="66800-119">Para criptografar o conteúdo, você precisa de uma chave, que é um valor usado para propagar os algoritmos de criptografia.</span><span class="sxs-lookup"><span data-stu-id="66800-119">To encrypt the content, you need a key, which is a value used to seed the encryption algorithms.</span></span> <span data-ttu-id="66800-120">Uma chave é composta de duas partes: uma semente de chave (ou chave privada) e um identificador de chave (ou chave pública).</span><span class="sxs-lookup"><span data-stu-id="66800-120">A key is made up of two pieces: a key seed (or private key), and a key identifier (or public key).</span></span> <span data-ttu-id="66800-121">A semente de chave é o valor secreto com o qual você codifica o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="66800-121">The key seed is the secret value with which you encode content.</span></span> <span data-ttu-id="66800-122">O identificador de chave é um valor público que é incluído no cabeçalho de um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="66800-122">The key identifier is a public value that is included in the header of a protected file.</span></span>

<span data-ttu-id="66800-123">Quando um arquivo é protegido, ele não pode ser descriptografado sem uma licença.</span><span class="sxs-lookup"><span data-stu-id="66800-123">When a file is protected, it cannot be decrypted without a license.</span></span> <span data-ttu-id="66800-124">Uma licença inclui informações que especificam os termos de uso do conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="66800-124">A license includes information that specifies the terms of use for the protected content.</span></span> <span data-ttu-id="66800-125">Os termos de uma licença são decididos pelo proprietário do conteúdo e podem ser personalizados para atender a uma variedade de necessidades.</span><span class="sxs-lookup"><span data-stu-id="66800-125">The terms of a license are decided by the content owner and can be customized to meet a variety of needs.</span></span> <span data-ttu-id="66800-126">Parte do processo de empacotamento de um arquivo é incluir a URL de uma página da Web em que os usuários podem adquirir uma licença para acessar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="66800-126">Part of the process of packaging a file is to include the URL of a Web page where users can acquire a license to access the content.</span></span>

## <a name="reading-protected-content"></a><span data-ttu-id="66800-127">Lendo conteúdo protegido</span><span class="sxs-lookup"><span data-stu-id="66800-127">Reading Protected Content</span></span>

<span data-ttu-id="66800-128">Para ler o conteúdo protegido, uma licença para o conteúdo deve residir no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="66800-128">To read protected content, a license for the content must reside on the client computer.</span></span> <span data-ttu-id="66800-129">Algumas restrições de licença são verificadas internamente pelos componentes DRM do SDK do Windows Media Format, enquanto outras devem ser impostas pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="66800-129">Some license restrictions are checked internally by the DRM components of the Windows Media Format SDK, while others must be enforced by your application.</span></span>

<span data-ttu-id="66800-130">Você pode usar os objetos do Windows Media Format SDK para ajudar o usuário a adquirir licenças para conteúdo e executar outras tarefas administrativas, como atualizar componentes DRM e fazer backup de licenças.</span><span class="sxs-lookup"><span data-stu-id="66800-130">You can use the objects of the Windows Media Format SDK to assist the user in acquiring licenses for content and to perform other administrative tasks, such as updating DRM components and backing up licenses.</span></span>

> [!Note]  
> <span data-ttu-id="66800-131">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="66800-131">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="66800-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="66800-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66800-133">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="66800-133">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="66800-134">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="66800-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




