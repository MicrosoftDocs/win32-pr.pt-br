---
description: Especifica o número máximo de passagens com suporte pelo codificador.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: MFPKEY_PASSESRECOMMENDED propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af869c6acca584547083b3de245913a35680306b47feabaf2a602a3c1c15e87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826356"
---
# <a name="mfpkey_passesrecommended-property"></a>Propriedade MFPKEY \_ PASSESRECOMMENDED

Especifica o número máximo de passagens com suporte pelo codificador. Somente leitura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="remarks"></a>Comentários

Você pode obter o valor dessa propriedade chamando [IWMCodecProps::GetCodecProp.](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) Se você usar **IPropertyBag**, deverá primeiro definir o valor FOURCC do formato compactado desejado usando a [propriedade MFPKEY \_ FOURCC.](mfpkey-fourccproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




