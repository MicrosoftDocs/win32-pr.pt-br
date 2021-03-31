---
title: DRM_DRMHeader_ContentID
description: O \_ atributo DRM DRMHeader \_ ContentId contém o ContentId gerado pelo proprietário do conteúdo.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66edd858451e5d1a58b2a91f9f2362d4cabe9da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916989"
---
# <a name="drm_drmheader_contentid"></a>\_ContentId do DRM DRMHeader \_

O atributo **DRM \_ DRMHeader \_ ContentId** contém o ContentId gerado pelo proprietário do conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ ContentId

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Esse atributo está presente somente com conteúdo do DRM versão 7. Ele pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para definir a ID do conteúdo no arquivo usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , você deve usar a propriedade [**\_ ContentId do DRM**](drm-contentid.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




