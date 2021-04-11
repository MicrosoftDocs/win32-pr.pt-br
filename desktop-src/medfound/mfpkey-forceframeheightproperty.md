---
description: Especifica uma altura intermediária de quadro para vídeo codificado.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: Propriedade MFPKEY_FORCEFRAMEHEIGHT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165392"
---
# <a name="mfpkey_forceframeheight-property"></a>\_Propriedade MFPKEY FORCEFRAMEHEIGHT

Especifica uma altura intermediária de quadro para vídeo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceFrameHeight

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Você pode definir esse valor e a propriedade [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) para forçar o codificador a codificar o fluxo de vídeo com um tamanho de quadro menor do que os tamanhos de quadro de entrada ou de saída. Quando decodificado, o vídeo será redimensionado para sua resolução de entrada original.

As dimensões de quadro válidas em qualquer eixo são de 2 a 8192 pixels. As dimensões do quadro devem ser divisíveis por 2.

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

 

 




