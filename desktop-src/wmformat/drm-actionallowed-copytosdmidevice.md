---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: O \_ atributo DRM ActionAllowed \_ CopyToSDMIDevice indica se o conteúdo pode ser copiado para um dispositivo SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365516"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>\_CopyToSDMIDevice ACTIONALLOWED \_ DRM

O atributo **DRM \_ ActionAllowed \_ CopyToSDMIDevice** indica se o conteúdo pode ser copiado para um dispositivo SDMI.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

As licenças do Windows Media DRM 10 usam a ação de cópia para restringir a cópia em dispositivos. Você deve verificar a propriedade de [**\_ \_ cópia do DRM ActionAllowed**](drm-actionallowed-copy.md) para determinar se a cópia é permitida.

Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




