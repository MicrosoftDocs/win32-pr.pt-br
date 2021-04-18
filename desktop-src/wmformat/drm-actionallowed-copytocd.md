---
title: DRM_ActionAllowed_CopyToCD
description: O \_ atributo DRM ActionAllowed \_ CopyToCD indica se o conteúdo pode ser copiado para um CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105768214"
---
# <a name="drm_actionallowed_copytocd"></a>\_CopyToCD ACTIONALLOWED \_ DRM

O atributo **DRM \_ ActionAllowed \_ CopyToCD** indica se o conteúdo pode ser copiado para um CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

As licenças do Windows Media DRM 10 usam a ação de cópia para restringir a cópia em CD. Você deve verificar a propriedade de [**\_ \_ cópia do DRM ActionAllowed**](drm-actionallowed-copy.md) para determinar se a cópia é permitida.

Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




