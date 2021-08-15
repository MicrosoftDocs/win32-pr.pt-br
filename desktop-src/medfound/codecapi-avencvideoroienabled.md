---
description: Indica se o atributo ROIRectangle de MFSampleExtension definido no exemplo de entrada \_ será ou não acatado.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: CODECAPI_AVEncVideoROIEnabled propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86185f6dbb9dfe16a84e7e85c3faddc8da3a7c1ead91dee2b1086e6fafa456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346976"
---
# <a name="codecapi_avencvideoroienabled-property"></a>Propriedade CODECAPI \_ AVEncVideoROIEnabled

Indica se o [atributo \_ ROIRectangle de MFSampleExtension](mfsampleextension-roirectangle.md) definido no exemplo de entrada será ou não acatado.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Comentários

O valor padrão é 0.

Se um codificador MFT aceitar um valor não zero, espera-se que o codificador aceite o atributo [ \_ ROIRectangle MFSampleExtension](mfsampleextension-roirectangle.md) definido no exemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




