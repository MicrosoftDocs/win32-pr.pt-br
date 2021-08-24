---
title: Exclusão de licença
description: Exclusão de licença
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows SDK de Formato de Mídia, licenças
- Windows SDK de Formato de Mídia, excluindo licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), excluindo licenças
- DRM (gerenciamento de direitos digitais), excluindo licenças
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs Estendidas do Cliente DRM, excluindo licenças
- APIs estendidas do cliente, excluindo licenças
- licenças, excluindo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd1e20c0e98fd2129b807cf11f27f5975701d851d9301eda894ccb24015360a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808296"
---
# <a name="license-deletion"></a>Exclusão de licença

Todas as licenças de terceiros criadas localmente, por exemplo, por meio da importação de DRM, podem ser excluídas chamando o método [**IWMDRMLicenseManagement::P rocessLicenseDeletionMessage.**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) A cadeia de caracteres que você passar para esse método será uma licença XMR semelhante à seguinte:


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



O campo UID (ID de usuário) específico do proprietário é opcional. Os campos opcionais não deverão ser incluídos na resposta da licença se não houver dados associados a eles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando uma licença XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importação de DRM**](drm-import.md)
</dt> <dt>

[**Guia de programação**](drm-programming-guide.md)
</dt> </dl>

 

 




