---
description: Especifica uma largura de quadro intermediária para vídeo codificado.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: MFPKEY_FORCEFRAMEWIDTH propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d04e30f5fd5d2ecc7055553e17eaf86199b62be8d3dd861b9f82246947212f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939827"
---
# <a name="mfpkey_forceframewidth-property"></a>Propriedade MFPKEY \_ FORCEFRAMEWIDTH

Especifica uma largura de quadro intermediária para vídeo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceFrameWidth

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="remarks"></a>Comentários

Você pode definir esse valor e a propriedade [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) para forçar o codificador a codificar o fluxo de vídeo com um tamanho de quadro menor do que os tamanhos de quadro de entrada ou saída. Quando decodificado, o vídeo será reessado para sua resolução de entrada original.

As dimensões de quadro válidas em qualquer eixo são de 2 a 8192 pixels. As dimensões do quadro devem ser divisíveis por 2.

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

 

 




