---
description: Especifica o FOURCC que identifica o codificador que você deseja usar.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Propriedade MFPKEY_FOURCC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921399"
---
# <a name="mfpkey_fourcc-property"></a>\_Propriedade FOURCC MFPKEY

Especifica o FOURCC que identifica o codificador que você deseja usar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCFOURCC

## <a name="data-type"></a>Tipo de Dados

VT \_ i4 (valor FourCC)

## <a name="remarks"></a>Comentários

Você deve definir esse valor antes de recuperar os valores para as seguintes propriedades usando **IPropertyBag** ou **IPropertyStore**:

-   [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)

Você deve usar [**IWMCodecProps:: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar os valores das propriedades dependentes de FOURCC listadas anteriormente. Ao usar **GetCodecProp**, você não precisa definir **MFPKEY \_ FOURCC**.

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

 

 




