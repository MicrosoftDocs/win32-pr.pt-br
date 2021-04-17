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
# <a name="license-deletion"></a>Exclusão de licenças

Qualquer licença de terceiros criada localmente, por exemplo, por meio de importação de DRM, pode ser excluída chamando o método [**IWMDRMLicenseManagement::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) . A cadeia de caracteres que você passa para esse método será uma licença XMR que se assemelha ao seguinte:


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



O campo UID (ID de usuário específico) do proprietário é opcional. Os campos opcionais não devem ser incluídos na resposta da licença se não houver dados associados a eles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando uma licença do XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importação de DRM**](drm-import.md)
</dt> <dt>

[**Guia de programação**](drm-programming-guide.md)
</dt> </dl>

 

 




