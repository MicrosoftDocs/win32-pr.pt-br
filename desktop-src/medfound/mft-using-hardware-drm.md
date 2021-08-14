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
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ usando \_ atributo de DRM de hardware \_

Especifica se o IMFTransform está usando o DRM de hardware.

## <a name="data-type"></a>Tipo de dados

**UINT32** (Tratado como **bool**)

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Comentários

Se um MFT Decrypter especificar esse atributo definido como 1, ele estará usando o DRM de hardware. Se um MFT Decrypter especificar esse atributo definido como 0, ele não estará usando o DRM de hardware. Se um Decrypter MFT não especificar esse atributo ou especificá-lo com um valor diferente, ele não será (ou não poderá) indicar se está usando o DRM de hardware.


A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 Atualização de abril de 2020   <br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




