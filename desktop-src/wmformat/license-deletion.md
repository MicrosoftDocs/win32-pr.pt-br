---
title: Exclusão de licenças
description: Exclusão de licenças
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- SDK do Windows Media Format, licenças
- SDK do Windows Media Format, excluindo licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), excluindo licenças
- DRM (gerenciamento de direitos digitais), excluindo licenças
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, excluindo licenças
- APIs estendidas do cliente, excluindo licenças
- licenças, excluindo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105749384"
---
# <a name="license-deletion"></a><span data-ttu-id="79128-114">Exclusão de licenças</span><span class="sxs-lookup"><span data-stu-id="79128-114">License Deletion</span></span>

<span data-ttu-id="79128-115">Qualquer licença de terceiros criada localmente, por exemplo, por meio de importação de DRM, pode ser excluída chamando o método [**IWMDRMLicenseManagement::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="79128-115">Any third-party licenses created locally, for example through DRM import, can be deleted by calling the [**IWMDRMLicenseManagement::ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) method.</span></span> <span data-ttu-id="79128-116">A cadeia de caracteres que você passa para esse método será uma licença XMR que se assemelha ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="79128-116">The string you pass to this method will be an XMR license that resembles the following:</span></span>


```C++
<response type="LRB">
  <DATA>
    <LICENSEDATA>
      <DATA>
        <KID>include Key ID here to revoke certain keys</KID>
        <LID>rights ID</LID
        <META>
          <LGPUBKEY>
            <PublicKey>
              <Modulus>base64 encoded public key</Modulus>
              <Exponent>Exponent in network byte order</Exponent>
            </PublicKey>
          </LGPUBKEY>
          <UID>content-owner-specific user ID</UID>
        </META>
      </DATA>
    </LICENSEDATA>
  </DATA>
</response>
```



<span data-ttu-id="79128-117">O campo UID (ID de usuário específico) do proprietário é opcional.</span><span class="sxs-lookup"><span data-stu-id="79128-117">The owner specific user ID (UID) field is optional.</span></span> <span data-ttu-id="79128-118">Os campos opcionais não devem ser incluídos na resposta da licença se não houver dados associados a eles.</span><span class="sxs-lookup"><span data-stu-id="79128-118">Optional fields must not be included in the license response if there is not any data associated with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79128-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79128-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79128-120">**Criando uma licença do XMR**</span><span class="sxs-lookup"><span data-stu-id="79128-120">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="79128-121">**Importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="79128-121">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="79128-122">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="79128-122">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




