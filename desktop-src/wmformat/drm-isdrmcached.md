---
title: DRM_IsDRMCached
description: A \_ Propriedade DRM IsDRMCached indica se as informações de licença do DRM versão 1 foram armazenadas no computador local.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105778450"
---
# <a name="drm_isdrmcached"></a>\_ISDRMCACHED DRM

A propriedade **DRM \_ IsDRMCached** indica se as informações de licença do DRM versão 1 foram armazenadas no computador local.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). É **verdade** quando a URL de aquisição de licença corresponde a uma das duas URLs conhecidas usadas para aquisição de licença local no DRM versão 1.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




