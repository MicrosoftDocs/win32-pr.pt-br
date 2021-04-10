---
title: Importando a licença e o material da chave
description: Importando a licença e o material da chave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), material da chave
- DRM (gerenciamento de direitos digitais), material da chave
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, material da chave
- APIs estendidas do cliente, material da chave
- licenças, importando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160358"
---
# <a name="importing-license-and-key-material"></a><span data-ttu-id="c046d-119">Importando a licença e o material da chave</span><span class="sxs-lookup"><span data-stu-id="c046d-119">Importing License and Key Material</span></span>

<span data-ttu-id="c046d-120">Se você tiver conteúdo de mídia que foi criptografado usando um sistema de proteção de conteúdo de terceiros e desejar importar a licença e o material da chave no Windows Media DRM, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="c046d-120">If you have media content that was encrypted using a third-party content protection system and you want to import the license and key material into Windows Media DRM, follow these steps:</span></span>

1.  <span data-ttu-id="c046d-121">Recupere a coleção de certificados do computador DRM do Windows Media chamando o método [**IWMDRMSecurity:: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="c046d-121">Retrieve the Windows Media DRM machine certificate collection by calling the [**IWMDRMSecurity::GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) method.</span></span>
2.  <span data-ttu-id="c046d-122">Analise a coleção de certificados, garantindo que ela esteja assinada corretamente e seja validada para uma chave pública Microsoft raiz conhecida.</span><span class="sxs-lookup"><span data-stu-id="c046d-122">Parse the certificate collection, ensuring that it is signed correctly and is validated to a known Microsoft root public key.</span></span> <span data-ttu-id="c046d-123">A coleção de certificados está de acordo com o esquema XMR.</span><span class="sxs-lookup"><span data-stu-id="c046d-123">The certificate collection conforms to the XMR schema.</span></span> <span data-ttu-id="c046d-124">Para obter mais informações, consulte [criando uma licença do XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="c046d-124">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>
3.  <span data-ttu-id="c046d-125">Opcional: Extraia a lista de revogação chamando o método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c046d-125">Optional: Extract the revocation list by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
4.  <span data-ttu-id="c046d-126">Opcional: Certifique-se de que nenhum certificado na coleção seja revogado.</span><span class="sxs-lookup"><span data-stu-id="c046d-126">Optional: Insure that no certificate in the collection is revoked.</span></span> <span data-ttu-id="c046d-127">Para obter mais informações, consulte [verificando revogação de certificado](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="c046d-127">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
5.  <span data-ttu-id="c046d-128">Gere uma licença no formato XMR que represente os requisitos de política para o conteúdo de importação e contenha o material de chave DRM do Windows Media apropriado.</span><span class="sxs-lookup"><span data-stu-id="c046d-128">Generate a license in the XMR format that represents the policy requirements for the import content and contains the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="c046d-129">Para obter mais informações, consulte o tópico [criando uma licença do XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="c046d-129">For more information, see the topic [Building an XMR License](building-an-xmr-license.md).</span></span>
6.  <span data-ttu-id="c046d-130">Passe a licença XMR para o sistema DRM do Windows Media para processamento, usando o método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="c046d-130">Pass the XMR license to the Windows Media DRM system for processing, by using the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="c046d-131">Os detalhes sobre o esquema XMR serão fornecidos a você quando você licenciar o DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c046d-131">Details about the XMR schema will be provided to you when you license Windows Media DRM.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c046d-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c046d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c046d-133">**Verificando revogação de certificado**</span><span class="sxs-lookup"><span data-stu-id="c046d-133">**Checking Certificate Revocation**</span></span>](checking-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="c046d-134">**Criando uma licença do XMR**</span><span class="sxs-lookup"><span data-stu-id="c046d-134">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="c046d-135">**Importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="c046d-135">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




