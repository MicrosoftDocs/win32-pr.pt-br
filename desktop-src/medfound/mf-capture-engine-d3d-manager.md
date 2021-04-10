---
description: Define um ponteiro para o Gerenciador de Dispositivos DXGI no mecanismo de captura.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Atributo MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090696"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>\_Atributo do \_ Gerenciador de D3D do mecanismo de captura MF \_ \_

Define um ponteiro para o Gerenciador de Dispositivos DXGI no mecanismo de captura.

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Esse atributo permite que o mecanismo de captura aloque quadros de vídeo usando superfícies DXGI e use aceleração de hardware para decodificação e processamento de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




