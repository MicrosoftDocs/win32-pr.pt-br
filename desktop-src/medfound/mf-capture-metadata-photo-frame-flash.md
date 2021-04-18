---
description: Indica se um flash foi disparado para o quadro capturado.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: Atributo MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810767"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>\_ \_ \_ \_ Atributo flash do quadro de fotos de metadados do MF Capture \_

Indica se um flash foi disparado para o quadro capturado.

## <a name="data-type"></a>Tipo de dados

**UINT32**



| Valor                                                                               | Significado                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | Um flash não foi disparado neste quadro.<br/>                                                                                                   |
| <dl> <dt>diferente de zero</dt> </dl> | Um flash foi disparado neste quadro.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Reservado<br/> Não verifique explicitamente um valor de 1. Os aplicativos só devem verificar! = 0 para indicar se um flash foi disparado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




