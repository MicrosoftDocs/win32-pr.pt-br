---
description: Indica se o \_ atributo MFSampleExtension ROIRectangle definido no exemplo de entrada será respeitado ou não.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: Propriedade CODECAPI_AVEncVideoROIEnabled (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345e6ba27a983be910f0dc0ea5d3db34191bdcb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296160"
---
# <a name="codecapi_avencvideoroienabled-property"></a>\_Propriedade CODECAPI AVEncVideoROIEnabled

Indica se o atributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) definido no exemplo de entrada será respeitado ou não.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Comentários

O valor padrão é 0.

Se um MFT do codificador aceitar um valor diferente de zero, espera-se que o codificador obedeça o atributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) definido no exemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




