---
description: Especifica o número máximo de passagens aceitas pelo codificador.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Propriedade MFPKEY_PASSESRECOMMENDED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165382"
---
# <a name="mfpkey_passesrecommended-property"></a>\_Propriedade MFPKEY PASSESRECOMMENDED

Especifica o número máximo de passagens aceitas pelo codificador. Somente leitura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Você pode obter o valor dessa propriedade chamando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Se você usar **IPropertyBag**, deverá primeiro definir o valor FOURCC do formato compactado desejado usando a propriedade [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md) .

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

 

 




