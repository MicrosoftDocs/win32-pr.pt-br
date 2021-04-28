---
description: Propriedade MFPKEY_RESIZE_INTERLACE-especifica se o fluxo de entrada está entrelaçado.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Propriedade MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092874"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
