---
title: DRM_DRMHeader_SubscriptionContentID
description: O \_ atributo DRM DRMHeader \_ SubscriptionContentID contém a ID de conteúdo da assinatura.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916988"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>\_SubscriptionContentID DRMHEADER \_ DRM

O atributo **DRM \_ DRMHeader \_ SUBSCRIPTIONCONTENTID** contém a ID de conteúdo da assinatura.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Esse atributo está presente somente com conteúdo do DRM versão 7. A ID do conteúdo da assinatura é opcional e é determinada exclusivamente pelo criador do conteúdo. O objeto gravador não faz nada com esse atributo. Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




