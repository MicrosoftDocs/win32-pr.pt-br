---
title: DRM_BaseLicenseAcqURL
description: O atributo BASELicenseAcqURL do DRM contém uma URL parcial e base para a qual um aplicativo player deve navegar para obter uma \_ licença para o conteúdo.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77827068ee8a491cd732b28e5b8d60e1868ec66c04c72156f08358dd7d3751d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658996"
---
# <a name="drm_baselicenseacqurl"></a>DRM \_ BaseLicenseAcqURL

O **atributo \_ BASELicenseAcqURL do DRM** contém uma URL parcial e base para a qual um aplicativo player deve navegar para obter uma licença para o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Essa é uma propriedade de leitura/gravação opcional que é definida e recuperada usando [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Ele é fornecido para permitir que os sistemas de distribuição de licença usem caminhos relativos nas propriedades da URL de aquisição de licença.

Depois de definir essa propriedade, todas as URLs de aquisição de licença parcial em títulos de conteúdo terão a URL base adicionada à frente da URL parcial para formar uma URL completa para o aplicativo player navegar. Chamar **IWMDRMReader::GetDRMProperty** para **DRM \_ BaseLicenseAcqURL** só funcionará na mesma sessão que foi definida. A propriedade não é armazenada no título do conteúdo; ele é dinâmico e apenas a URL relativa é armazenada no conteúdo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




