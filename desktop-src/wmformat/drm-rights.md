---
title: DRM_Rights
description: A \_ Propriedade direitos de DRM especifica os direitos que o aplicativo precisará na próxima tentativa de abrir um arquivo protegido.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d655ea3f4a0a5dccc8b5e1380296948c9a55dce1d86336f824b30189f6557d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930896"
---
# <a name="drm_rights"></a>Direitos de DRM \_

A **propriedade \_ direitos de DRM** especifica os direitos que o aplicativo precisará na próxima tentativa de abrir um arquivo protegido.

## <a name="global-constant"></a>Constante global

\_direitos g wszWMDRM \_

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Essa é uma propriedade de leitura/gravação que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) e definida usando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) ou [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

A tabela a seguir lista os direitos com suporte.



| Direita                                           | Cadeia de caracteres literal      | Descrição                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ backup do g wszWMDRM direito \_                      | "Backup"            | Direito de fazer backup da licença.                                                                                                                                                                                        |
| g \_ wszWMDRM \_ de \_ colaboração à \_ direita         | "CollaborativePlay" | Direito de reproduzir o arquivo como parte de uma lista de reprodução colaborativa.                                                                                                                                                          |
| \_ \_ copiar à direita do g wszWMDRM \_                        | CopiarObjeto              | Direito de copiar o arquivo para um dispositivo. Esse direito substitui os direitos de cópia mais antigos (g \_ wszWMDRM \_ à direita \_ copiar \_ para \_ CD, g \_ wszWMDRM \_ à direita \_ copiar \_ para \_ \_ dispositivo não SDMI \_ e g \_ wszWMDRM \_ a cópia à direita \_ para o \_ \_ dispositivo SDMI \_ ). |
| \_ \_ \_ copiar \_ para o \_ CD do g wszWMDRM                | "Print. Redbook"     | Direito de copiar o arquivo em um CD (formato de livro vermelho). no Windows Media DRM 10, esse direito é substituído pela \_ \_ cópia right g wszWMDRM \_ .<br/>                                                                             |
| \_ \_ copiar à direita do g wszWMDRM \_ para um \_ \_ \_ dispositivo não SDMI \_ | "Transfer. NONSDMI"  | Direito de copiar o arquivo para um dispositivo não SDMI. no Windows Media DRM 10, esse direito é substituído pela \_ \_ cópia right g wszWMDRM \_ .<br/>                                                                                  |
| \_ \_ copiar à direita do g wszWMDRM \_ para o \_ \_ \_ dispositivo SDMI      | "Transfer. SDMI"     | Direito de copiar o arquivo para um dispositivo compatível com SDMI. no Windows Media DRM 10, esse direito é substituído pela \_ \_ cópia right g wszWMDRM \_ .<br/>                                                                           |
| \_ \_ reprodução à direita g wszWMDRM \_                    | Reproduzir              | Direito de reproduzir o arquivo de mídia.                                                                                                                                                                                        |



 

Essa propriedade contém uma cadeia de caracteres largos de um ou mais direitos separados por ponto-e-vírgula, por exemplo: L "reprodução; CopiarObjeto CollaborativePlay".

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 





