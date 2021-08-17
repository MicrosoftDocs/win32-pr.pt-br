---
description: Propriedade MFPKEY_RESIZE_INTERLACE-especifica se o fluxo de entrada está entrelaçado.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Propriedade MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c614865d0c8a49238b9c8d6f7714787bb22aaadaa317a8a3a0405a7f51c87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873030"
---
# <a name="mfpkey_resize_interlace-property"></a>MFPKEY \_ redimensionar \_ Propriedade entrelaçar

Especifica se o fluxo de entrada está entrelaçado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="applies-to"></a>Aplica-se A

-   [DSP de redimensionador de vídeo](videoresizer.md)

## <a name="remarks"></a>Comentários

Use um dos seguintes valores:



| Valor     | Descrição |
|-----------|-------------|
| VT \_ falso | Progressivo |
| VT \_ verdadeiro  | Interlaced  |



 

Se essa propriedade não for definida, o DSP usará o tipo de mídia de entrada para determinar se o vídeo está entrelaçado. Você pode definir essa propriedade para substituir a configuração do tipo de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
