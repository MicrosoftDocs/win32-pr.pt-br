---
description: Especifica se o fluxo de entrada está entrelaçado.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Propriedade MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661880"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
