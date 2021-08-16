---
title: DRM_LicenseAcqURL
description: O atributo DrM LicenseAcqURL contém o endereço de uma página da Web para a que o aplicativo cliente pode navegar para obter uma licença de conteúdo para o conteúdo da versão 7 do \_ DRM.
ms.assetid: bee29e39-ded8-439d-9164-fc318cb535c0
keywords:
- DRM_LicenseAcqURL formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82edc09cf28ab5b46f4dc6df91f266927294209c69ff11289324d01cedbd23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848475"
---
# <a name="drm_licenseacqurl"></a>Licença \_ DRMAcqURL

O **atributo \_ DrM LicenseAcqURL** contém o endereço de uma página da Web para a que o aplicativo cliente pode navegar para obter uma licença de conteúdo para o conteúdo da versão 7 do DRM.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseAcqURL

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). O mesmo atributo de arquivo pode ser recuperado usando [**\_ DRM DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




