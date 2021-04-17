---
title: Lista de atributos DRM
description: Lista de atributos DRM
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), atributos
- DRM (gerenciamento de direitos digitais), atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798269"
---
# <a name="drm-attribute-list"></a>Lista de atributos DRM

Para sua conveniência, a tabela a seguir lista todos os atributos de arquivo relacionados ao DRM. (Esses atributos também estão listados na tabela de todos os atributos na [lista de atributos](attribute-list.md).)

Os aplicativos podem definir esses valores ao gravar arquivos DRM e podem recuperá-los durante a leitura.



| Atributo de arquivo DRM                                                                   | Identificador global                             | Tipo de dados             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [**\_ContentId DRM**](drm-contentid.md)                                              | g \_ wszWMDRM \_ ContentId                        | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_ContentDistributor DRMHEADER \_ DRM**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor    | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_ContentId do DRM DRMHeader \_**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ ContentId             | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_IndividualizedVersion DRMHEADER \_ DRM**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_Keyid DRMHEADER \_ DRM**](drm-drmheader-keyid.md)                                 | \_keyid g wszWMDRM \_ DRMHeader \_                 | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_LicenseAcqURL DRMHEADER \_ DRM**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_SubscriptionContentID DRMHEADER \_ DRM**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_DRMHEADER DRM**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_Keyid DRM**](drm-keyid.md)                                                      | \_keyid g wszWMDRM \_                            | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **Cadeia de caracteres do \_ tipo WMT \_** |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos por tipo**](attributes-by-type.md)
</dt> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




