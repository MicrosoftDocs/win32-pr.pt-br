---
title: Criando uma licença XMR
description: Criando uma licença XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows SDK de formato de mídia, importação de DRM
- Windows SDK de Formato de Mídia, importar
- Windows SDK de Formato de Mídia, licenças XMR
- Windows SDK de Formato de Mídia, licenças
- Windows SDK de formato de mídia, direitos de mídia extensíveis (XMR)
- DRM (gerenciamento de direitos digitais), importação
- DRM (gerenciamento de direitos digitais), importação
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças XMR
- DRM (gerenciamento de direitos digitais), licenças XMR
- DRM (gerenciamento de direitos digitais), XMR (Direitos de Mídia Extensíveis)
- DRM (gerenciamento de direitos digitais), XMR (Direitos de Mídia Extensíveis)
- APIs estendidas do cliente DRM, importação
- APIs estendidas do cliente, importação
- APIs estendidas do cliente DRM, licenças XMR
- APIs estendidas do cliente, licenças XMR
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, XMR (Direitos de Mídia Extensíveis)
- APIs estendidas do cliente, direitos de mídia extensíveis (XMR)
- licenças, XMR
- XMR (Extensible Media Rights)
- XMR (direitos de mídia extensíveis)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73406d36c6ec7903ee7966f162811336aaecccaac5093e6d467e02c1a56ec71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881396"
---
# <a name="building-an-xmr-license"></a>Criando uma licença XMR

Para gerar uma licença para Windows DRM de Mídia para processar, você deve usar o esquema binário XMR (Extensible Media Rights). XMR é um esquema para transmitir direitos e restrições de uso de mídia e precisa ser licenciado separadamente.

O material importante em uma licença é criptografado usando a chave pública na coleção de certificados drm de mídia Windows, portanto, ele fica visível somente para o subsistema de API estendida do cliente drm de Windows mídia. .

É sua responsabilidade garantir que a estrutura de licenças e as configurações de política sejam válidas e consistentes com a intenção do emissor da licença e que elas estão em conformidade com as regras de conformidade.

Você deve ler as Windows de conformidade de importação de DRM de mídia para aprender o conjunto completo de objetos XMR que devem estar presentes na licença.

Para passar a licença XMR para o subsistema DRM, chame o [**método IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md) Use o seguinte formato para passar a licença no *parâmetro bstrLicenseResponse:*


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

 

 




