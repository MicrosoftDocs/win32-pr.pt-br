---
description: Indica se um flash foi disparado para o quadro capturado.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a885786674c524b382912100171502dba78a010b2169738233b5aaad88ed701a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973915"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>Atributo FLASH MF \_ CAPTURE \_ \_ METADATA PHOTO \_ FRAME \_

Indica se um flash foi disparado para o quadro capturado.

## <a name="data-type"></a>Tipo de dados

**UINT32**



| Valor                                                                               | Significado                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | Um flash não foi disparado nesse quadro.<br/>                                                                                                   |
| <dl> <dt>diferente de zero</dt> </dl> | Um flash foi disparado nesse quadro.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Reservado<br/> Não verifique explicitamente se há um valor de 1. Os aplicativos só devem verificar !=0 para indicar se um flash foi disparado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




