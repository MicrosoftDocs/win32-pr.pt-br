---
title: Criando uma licença do XMR
description: Criando uma licença do XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, licenças do XMR
- SDK do Windows Media Format, licenças
- Windows Media Format SDK, XMR (direitos de mídia extensível)
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças do XMR
- DRM (gerenciamento de direitos digitais), licenças do XMR
- DRM (gerenciamento de direitos digitais), XMR (direitos de mídia extensível)
- DRM (gerenciamento de direitos digitais), direitos de mídia extensível (XMR)
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, licenças do XMR
- APIs estendidas do cliente, licenças do XMR
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, direitos de mídia extensível (XMR)
- APIs estendidas do cliente, direitos de mídia extensível (XMR)
- licenças, XMR
- Direitos de mídia extensível (XMR)
- XMR (direitos de mídia extensível)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363670"
---
# <a name="building-an-xmr-license"></a><span data-ttu-id="177ef-127">Criando uma licença do XMR</span><span class="sxs-lookup"><span data-stu-id="177ef-127">Building an XMR License</span></span>

<span data-ttu-id="177ef-128">Para gerar uma licença para o Windows Media DRM processar, você deve usar o esquema binário XMR (direitos de mídia extensível).</span><span class="sxs-lookup"><span data-stu-id="177ef-128">To generate a license for Windows Media DRM to process, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="177ef-129">XMR é um esquema para transmitir direitos e restrições de uso de mídia e precisa ser licenciado separadamente.</span><span class="sxs-lookup"><span data-stu-id="177ef-129">XMR is a schema for conveying media usage rights and restrictions and needs to be licensed separately.</span></span>

<span data-ttu-id="177ef-130">O material importante em uma licença é criptografado usando a chave pública na coleção de certificados do Windows Media DRM, portanto, ele é visível apenas para o subsistema de API estendida do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="177ef-130">The important material in a license is encrypted using the public key in the Windows Media DRM certificate collection, so it is visible only to the Windows Media DRM Client Extended API subsystem.</span></span> <span data-ttu-id="177ef-131">.</span><span class="sxs-lookup"><span data-stu-id="177ef-131">.</span></span>

<span data-ttu-id="177ef-132">É sua responsabilidade garantir que a estrutura de licença e as configurações de política sejam válidas e consistentes com a intenção do emissor da licença e que elas estejam em conformidade com as regras de conformidade.</span><span class="sxs-lookup"><span data-stu-id="177ef-132">It is your responsibility to ensure that the license structure and policy settings are valid and consistent with the license issuer's intent, and that they conform to the compliance rules.</span></span>

<span data-ttu-id="177ef-133">Você deve ler as regras de conformidade de importação do DRM do Windows Media para saber o conjunto completo de objetos XMR que devem estar presentes na licença.</span><span class="sxs-lookup"><span data-stu-id="177ef-133">You should read the Windows Media DRM import compliance rules to learn the complete set of XMR objects that must be present in the license.</span></span>

<span data-ttu-id="177ef-134">Para passar a licença XMR para o subsistema DRM, chame o método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="177ef-134">To pass the XMR license to the DRM subsystem, call the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span> <span data-ttu-id="177ef-135">Use o seguinte formato para passar a licença no parâmetro *bstrLicenseResponse* :</span><span class="sxs-lookup"><span data-stu-id="177ef-135">Use the following format to pass the license in the *bstrLicenseResponse* parameter:</span></span>


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



<span data-ttu-id="177ef-136">Essa cadeia de caracteres deve estar no formato Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="177ef-136">This string must be in Unicode format (UTF-16).</span></span>

## <a name="related-topics"></a><span data-ttu-id="177ef-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="177ef-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="177ef-138">**Importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="177ef-138">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




