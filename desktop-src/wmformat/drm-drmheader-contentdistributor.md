---
title: DRM_DRMHeader_ContentDistributor
description: O \_ atributo DRM DRMHeader \_ ContentDistributor contém uma cadeia de caracteres identifiying o distribuidor de conteúdo.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105772638"
---
# <a name="drm_drmheader_contentdistributor"></a>\_ContentDistributor DRMHEADER \_ DRM

O atributo **DRM \_ DRMHeader \_ ContentDistributor** contém uma cadeia de caracteres identifiying o distribuidor de conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

A ID de conteúdo é opcional e é determinada exclusivamente pelo criador de conteúdo. O objeto gravador não faz nada com esse atributo. Esse atributo está presente somente com conteúdo do DRM versão 7. Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




