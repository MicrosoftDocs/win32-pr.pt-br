---
description: Especifica o aumento Delta entre a imagem quantizador do quadro âncora e a quantizador da imagem do quadro B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: Propriedade MFPKEY_BDELTAQP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810759"
---
# <a name="mfpkey_bdeltaqp-property"></a>\_Propriedade MFPKEY BDELTAQP

Especifica o aumento Delta entre a imagem quantizador do quadro âncora e a quantizador da imagem do quadro B.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBDeltaQP

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

O Picture quantizador (QP) é uma medida de como o quadro é compactado. Valores mais altos representam taxas de compactação maiores. A QP pode ser definida em incrementos de meio ponto. Normalmente, um quadro B é compactado em um QP igual a ou 0,5 maior do que o QP do quadro âncora. Ao especificar um Delta de QP de B superior a 0, é possível compactar quadros B a uma taxa de compactação ainda maior.

O Delta QP de quadro B só pode ser definido em incrementos de ponto inteiro. Essa propriedade deve ser definida como um valor inteiro de 0 a 31. O valor recomendado é 1.

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

 

 




