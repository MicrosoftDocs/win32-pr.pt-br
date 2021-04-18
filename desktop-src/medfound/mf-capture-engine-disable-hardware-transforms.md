---
description: Desabilita o uso de transformações de Media Foundation baseadas em hardware (MFTs) no mecanismo de captura.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Atributo MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798547"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>O \_ mecanismo de captura MF \_ desabilita o atributo de \_ \_ \_ transformações de hardware

Desabilita o uso de transformações de Media Foundation baseadas em hardware (MFTs) no mecanismo de captura.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Por padrão, o mecanismo de captura usa os codificadores de hardware ou codificadores. Para desabilitar o uso de MFTs de hardware, defina esse atributo como **true** ao criar o mecanismo de captura.

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

 

 




