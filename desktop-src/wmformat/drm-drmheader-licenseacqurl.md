---
title: DRM_DRMHeader_LicenseAcqURL
description: O \_ atributo DRM DRMHeader \_ LicenseAcqURL contém a URL de aquisição de licença para uma licença do DRM versão 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007108"
---
# <a name="drm_drmheader_licenseacqurl"></a>\_LicenseAcqURL DRMHEADER \_ DRM

O atributo **DRM \_ DRMHeader \_ LICENSEACQURL** contém a URL de aquisição de licença para uma licença do DRM versão 7.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Esse atributo está presente somente com conteúdo do DRM versão 7. Ele pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para definir a URL de aquisição de licença no arquivo usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , você deve usar a propriedade [**\_ LicenseAcqURL do DRM**](drm-licenseacqurl.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




