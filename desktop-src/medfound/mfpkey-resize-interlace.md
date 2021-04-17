---
description: Especifica se o fluxo de entrada está entrelaçado.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Propriedade MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754914"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
