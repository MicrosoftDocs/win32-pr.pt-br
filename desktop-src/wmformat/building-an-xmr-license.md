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
# <a name="building-an-xmr-license"></a>Criando uma licença do XMR

Para gerar uma licença para o Windows Media DRM processar, você deve usar o esquema binário XMR (direitos de mídia extensível). XMR é um esquema para transmitir direitos e restrições de uso de mídia e precisa ser licenciado separadamente.

O material importante em uma licença é criptografado usando a chave pública na coleção de certificados do Windows Media DRM, portanto, ele é visível apenas para o subsistema de API estendida do cliente DRM do Windows Media. .

É sua responsabilidade garantir que a estrutura de licença e as configurações de política sejam válidas e consistentes com a intenção do emissor da licença e que elas estejam em conformidade com as regras de conformidade.

Você deve ler as regras de conformidade de importação do DRM do Windows Media para saber o conjunto completo de objetos XMR que devem estar presentes na licença.

Para passar a licença XMR para o subsistema DRM, chame o método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) . Use o seguinte formato para passar a licença no parâmetro *bstrLicenseResponse* :


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



Essa cadeia de caracteres deve estar no formato Unicode (UTF-16).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Importação de DRM**](drm-import.md)
</dt> </dl>

 

 




