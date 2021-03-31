---
description: Especifica o número de quadros de vídeo que são ignorados porque eles eram duplicatas de quadros anteriores.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Propriedade MFPKEY_ZEROBYTEFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827546"
---
# <a name="mfpkey_zerobyteframes-property"></a>\_Propriedade MFPKEY ZEROBYTEFRAMES

Especifica o número de quadros de vídeo que são ignorados porque eles eram duplicatas de quadros anteriores.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCZeroByteFrames

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Esse valor não é subtraído do número total de quadros passados ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) ao calcular o número de quadros codificados ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).

Você pode parar o codec de ignorar quadros duplicados definindo [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) como Variant \_ true.

Você pode obter esse valor depois de terminar de passar amostras.

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

 

 




