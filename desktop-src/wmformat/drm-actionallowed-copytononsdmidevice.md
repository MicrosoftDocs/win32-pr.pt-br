---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: O \_ atributo DRM ActionAllowed \_ CopyToNonSDMIDevice indica se o conteúdo pode ser copiado para um dispositivo não SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007140"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM

O atributo **DRM \_ ActionAllowed \_ CopyToNonSDMIDevice** indica se o conteúdo pode ser copiado para um dispositivo não SDMI

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

As licenças do Windows Media DRM 10 usam a ação de cópia para restringir a cópia em dispositivos. Você deve verificar a propriedade de [**\_ \_ cópia do DRM ActionAllowed**](drm-actionallowed-copy.md) para determinar se a cópia é permitida.

Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




