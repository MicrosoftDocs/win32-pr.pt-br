---
description: Especifica o número de quadros de vídeo codificados pelo codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Propriedade MFPKEY_CODEDFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766931"
---
# <a name="mfpkey_codedframes-property"></a>\_Propriedade MFPKEY CODEDFRAMES

Especifica o número de quadros de vídeo codificados pelo codec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCodedFrames

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Esse valor é igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos quaisquer quadros que foram descartados devido a restrições de taxa de bits. Você pode obter esse valor depois de terminar de passar amostras.

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

 

 




