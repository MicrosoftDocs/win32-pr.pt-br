---
title: Propriedades de DRM
description: Propriedades de DRM
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- SDK do Windows Media Format, propriedades de DRM
- Formato de sistema avançado (ASF), propriedades de DRM
- ASF (formato de sistemas avançados), propriedades de DRM
- DRM (gerenciamento de direitos digitais), propriedades
- DRM (gerenciamento de direitos digitais), propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8542d360c38ab3f12406462cefc0454e7eae33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006180"
---
# <a name="drm-properties"></a>Propriedades de DRM

A tabela a seguir lista as propriedades de DRM que os aplicativos podem obter ou definir ao gravar ou ler arquivos protegidos. Essas propriedades não são atributos de arquivo; Eles não são gravados no cabeçalho do arquivo ASF.



| Propriedade DRM                                                                             | Identificador global                               | Tipo de Dados             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**\_ACTIONALLOWED DRM**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **WMT \_ tipo \_ bool**   |
| [**\_Backup ACTIONALLOWED \_ DRM**](drm-actionallowed-backup.md)                           | Backup do g \_ wszWMDRM \_ ActionAllowed \_              | **WMT \_ tipo \_ bool**   |
| [**\_CollaborativePlay ACTIONALLOWED \_ DRM**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **WMT \_ tipo \_ bool**   |
| [**\_Cópia ACTIONALLOWED \_ DRM**](drm-actionallowed-copy.md)                               | cópia do g \_ wszWMDRM \_ ActionAllowed \_                | **WMT \_ tipo \_ bool**   |
| [**\_CopyToCD ACTIONALLOWED \_ DRM**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **WMT \_ tipo \_ bool**   |
| [**\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **WMT \_ tipo \_ bool**   |
| [**\_CopyToSDMIDevice ACTIONALLOWED \_ DRM**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **WMT \_ tipo \_ bool**   |
| [**\_Reprodução de ACTIONALLOWED DRM \_**](drm-actionallowed-playback.md)                       | reprodução do g \_ wszWMDRM \_ ActionAllowed \_            | **WMT \_ tipo \_ bool**   |
| [**\_PlaylistBurn ACTIONALLOWED \_ DRM**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn        | **WMT \_ tipo \_ bool**   |
| [**\_BASELICENSEACQURL DRM**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**Sinalizadores de DRM \_**](drm-flags.md)                                                          | \_sinalizadores g wszWMDRM \_                              | **WMT \_ tipo \_ DWORD**  |
| [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_ISDRM DRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **WMT \_ tipo \_ bool**   |
| [**\_ISDRMCACHED DRM**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **WMT \_ tipo \_ bool**   |
| [**Keysemente DRM \_**](drm-keyseed.md)                                                      | \_wszWMDRM \_ keysemente                            | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**Nível de DRM \_**](drm-level.md)                                                          | \_nível g wszWMDRM \_                              | **WMT \_ tipo \_ DWORD**  |
| [**\_Licenseid DRM**](drm-licenseid.md)                                                  | \_licença de wszWMDRM g \_                          | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**Licença do DRM \_**](drm-licensestate.md)                                            | \_licença g wszWMDRM \_                       | **WMT \_ tipo \_ DWORD**  |
| [**CollaborativePlay de licença do DRM \_ \_**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ licensestate \_ CollaborativePlay    | **WMT \_ tipo \_ binário** |
| [**\_Cópia do licensestate do DRM \_**](drm-licensestate-copy.md)                                 | \_cópia de \_ licença g \_ wszWMDRM                 | **WMT \_ tipo \_ binário** |
| [**CopyToCD de licença do DRM \_ \_**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ licensestate \_ CopyToCD             | **WMT \_ tipo \_ binário** |
| [**CopyToSDMIDevice de licença do DRM \_ \_**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ licensestate \_ CopyToSDMIDevice     | **WMT \_ tipo \_ binário** |
| [**CopyToNonSDMIDevice de licença do DRM \_ \_**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ licensestate \_ CopyToNonSDMIDevice  | **WMT \_ tipo \_ binário** |
| [**\_Reprodução de licensestate DRM \_**](drm-licensestate-playback.md)                         | wszWMDRM de licença do g para \_ \_ \_ reprodução             | **WMT \_ tipo \_ binário** |
| [**PlaylistBurn de licença do DRM \_ \_**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM \_ licensestate \_ PlaylistBurn         | **WMT \_ tipo \_ binário** |
| [**Direitos de DRM \_**](drm-rights.md)                                                        | \_direitos g wszWMDRM \_                             | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**\_SAPLEVEL DRM**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **Cadeia de caracteres do \_ tipo WMT \_** |
| [**Usar \_ \_ DRM avançado**](use-advanced-drm.md)                                           | \_wszWMUse \_ Advanced \_ DRM                      | **WMT \_ tipo \_ bool**   |
| [**Usar \_ DRM**](use-drm.md)                                                              | \_wszWMUse \_ DRM                                | **WMT \_ tipo \_ bool**   |
| [**\_Revogação de WMDRMNET**](wmdrmnet-revocation.md)                                      | \_wszWMDRMNET \_ revogação de g                      | **Cadeia de caracteres do \_ tipo WMT \_** |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> </dl>

 

 




