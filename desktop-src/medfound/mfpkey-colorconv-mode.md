---
description: Propriedade MFPKEY_COLORCONV_MODE-especifica se o fluxo de entrada está entrelaçado.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Propriedade MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087574"
---
# <a name="mfpkey_colorconv_mode-property"></a>\_Propriedade do \_ modo MFPKEY COLORCONV

Especifica se o fluxo de entrada está entrelaçado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

Computado pelo DSP do vídeo de origem.

## <a name="applies-to"></a>Aplica-se A

-   [DSP de conversor de cores](colorconverter.md)

## <a name="remarks"></a>Comentários

Use um dos valores a seguir.



| Valor | Descrição |
|-------|-------------|
| 0     | Progressivo |
| 2     | Interlaced  |



 

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

 

 
