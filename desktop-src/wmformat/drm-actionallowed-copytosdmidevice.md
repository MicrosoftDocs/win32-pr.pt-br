---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: O atributo \_ ActionAllowed CopyToSDMIDevice do DRM indica se o conteúdo tem permissão para ser \_ copiado para um dispositivo SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a868eab52d354672802ef1f736bbc2754af605371708247415cbe78a42442e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809416"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>Ação do \_ DRMProm \_ permitido CopyToSDMIDevice

O **atributo \_ ActionAllowed \_ CopyToSDMIDevice** do DRM indica se o conteúdo tem permissão para ser copiado para um dispositivo SDMI.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentários

Windows As licenças de DRM de mídia 10 usam a ação Copiar para restringir a cópia para dispositivos. Você deve verificar a [**propriedade \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) do DRM para determinar se a cópia é permitida.

Essa é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




