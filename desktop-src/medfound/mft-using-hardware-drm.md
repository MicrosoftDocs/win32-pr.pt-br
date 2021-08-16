---
description: Especifica se o IMFTransform está usando o DRM de hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b46760fd5759abdd601269f5905f0649145649713839de5fe6424bc36219c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473546"
---
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ USANDO o atributo \_ \_ DRM DE HARDWARE

Especifica se o IMFTransform está usando o DRM de hardware.

## <a name="data-type"></a>Tipo de dados

**UINT32** (tratado como **BOOL**)

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Comentários

Se um descriptografador MFT especificar esse atributo definido como 1, ele está usando o DRM de hardware. Se um descriptografador MFT especificar esse atributo definido como 0, ele não está usando o DRM de hardware. Se um descriptografador MFT não especificar esse atributo ou especificá-lo com um valor diferente, ele não indicará (ou não) se está usando o DRM de hardware.


A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 Atualização de abril de 2020   <br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




