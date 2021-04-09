---
description: Especifica a categoria de dispositivo para um dispositivo de captura de vídeo.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090689"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a>\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ atributo category

Especifica a categoria de dispositivo para um dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de dados

**GUID**

O valor a seguir é definido.



| Valor                                                                                                                                                                                                                                                             | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <dt>**\_VIDEOINPUTDEVICECATEGORY CLSID**</dt> </dl> | Dispositivo de captura de vídeo.<br/> |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentários

Use esse atributo como entrada para a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) ao enumerar dispositivos de captura de vídeo.

Além disso, esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

O atributo aplica-se somente a dispositivos de captura de vídeo.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




