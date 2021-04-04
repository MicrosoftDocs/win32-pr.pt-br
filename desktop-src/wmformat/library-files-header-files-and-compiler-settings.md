---
title: Arquivos de biblioteca, arquivos de cabeçalho e configurações do compilador
description: Arquivos de biblioteca, arquivos de cabeçalho e configurações do compilador
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- SDK do Windows Media Format, arquivos de biblioteca DRM
- SDK do Windows Media Format, arquivos de biblioteca
- SDK do Windows Media Format, arquivos de cabeçalho do DRM
- SDK do Windows Media Format, arquivos de cabeçalho
- SDK do Windows Media Format, configurações do compilador do DRM
- SDK do Windows Media Format, configurações do compilador
- DRM (gerenciamento de direitos digitais), arquivos de biblioteca
- DRM (gerenciamento de direitos digitais), arquivos de biblioteca
- DRM (gerenciamento de direitos digitais), arquivos de cabeçalho
- DRM (gerenciamento de direitos digitais), arquivos de cabeçalho
- DRM (gerenciamento de direitos digitais), configurações do compilador
- DRM (gerenciamento de direitos digitais), configurações do compilador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084092"
---
# <a name="library-files-header-files-and-compiler-settings"></a><span data-ttu-id="02357-115">Arquivos de biblioteca, arquivos de cabeçalho e configurações do compilador</span><span class="sxs-lookup"><span data-stu-id="02357-115">Library Files, Header Files, and Compiler Settings</span></span>

<span data-ttu-id="02357-116">Os componentes de programação das APIs estendidas do cliente DRM do Windows Media são definidos no arquivo de cabeçalho wmdrmsdk. h e implementados nas bibliotecas wmdrmsdk. lib e mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="02357-116">The programming components of the Windows Media DRM Client Extended APIs are defined in the wmdrmsdk.h header file, and implemented in the wmdrmsdk.lib and mfuuid.lib libraries.</span></span>

<span data-ttu-id="02357-117">Algumas das funcionalidades das APIs estendidas do cliente DRM do Windows Media exigem que você obtenha uma biblioteca protegida da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="02357-117">Some of the functionality of the Windows Media DRM Client Extended APIs requires that you obtain a protected library from Microsoft.</span></span> <span data-ttu-id="02357-118">Essa biblioteca, chamada de biblioteca de stub nesta documentação, é específica para o destinatário e especifica o nível de segurança do aplicativo para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="02357-118">This library, called the stub library in this documentation, is specific to the recipient and specifies the application security level for your applications.</span></span> <span data-ttu-id="02357-119">A biblioteca de stub substitui wmdrmsdk. lib; Você nunca deve vincular a ambos.</span><span class="sxs-lookup"><span data-stu-id="02357-119">The stub library replaces wmdrmsdk.lib; you should never link to both.</span></span>

<span data-ttu-id="02357-120">**Observação** A biblioteca de stubs de DRM é separada da biblioteca de stub usada pelo restante do Windows Media Format SDK, mas é licenciada usando o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="02357-120">**Note** The DRM stub library is separate from the stub library used by the rest of the Windows Media Format SDK but is licensed using the same method.</span></span>

<span data-ttu-id="02357-121">**Observação** A biblioteca de stub de DRM deve ser vinculada ao seu aplicativo após o arquivo de biblioteca msvcrt. lib para evitar erros de vinculador.</span><span class="sxs-lookup"><span data-stu-id="02357-121">**Note** The DRM stub library must be linked into your application after the library file msvcrt.lib to avoid linker errors.</span></span>

<span data-ttu-id="02357-122">A biblioteca de stub contém um certificado inserido que pode ser revogado pela Microsoft se você não atender aos termos e condições do contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="02357-122">The stub library contains an embedded certificate which can be revoked by Microsoft if you fail to comply with the terms and conditions of the license agreement.</span></span>

<span data-ttu-id="02357-123">Métodos específicos que exigem a biblioteca de stub são rotulados na documentação.</span><span class="sxs-lookup"><span data-stu-id="02357-123">Specific methods that require the stub library are labeled in the documentation.</span></span> <span data-ttu-id="02357-124">Se você tentar usar esse método sem vincular à biblioteca de stub, ele retornará um erro STUBLIB do NS \_ E \_ DRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="02357-124">If you try to use such a method without linking to the stub library, it will return an NS\_E\_DRM\_STUBLIB\_REQUIRED error.</span></span>

<span data-ttu-id="02357-125">O subsistema DRM não pode ser usado em uma compilação de depuração.</span><span class="sxs-lookup"><span data-stu-id="02357-125">The DRM subsystem can not be used in a debug build.</span></span> <span data-ttu-id="02357-126">Se isso for tentado, os métodos da API retornarão o erro de \_ depuração do NS E \_ DRM \_ \_ não \_ permitido.</span><span class="sxs-lookup"><span data-stu-id="02357-126">If this is attempted, methods of the API will return the NS\_E\_DRM\_DEBUGGING\_NOT\_ALLOWED error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02357-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02357-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02357-128">**Introdução**</span><span class="sxs-lookup"><span data-stu-id="02357-128">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="02357-129">**Arquivos de biblioteca e configurações do compilador**</span><span class="sxs-lookup"><span data-stu-id="02357-129">**Library Files and Compiler Settings**</span></span>](library-files-and-compiler-settings.md)
</dt> <dt>

[<span data-ttu-id="02357-130">**Obtendo a biblioteca de DRM necessária**</span><span class="sxs-lookup"><span data-stu-id="02357-130">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




