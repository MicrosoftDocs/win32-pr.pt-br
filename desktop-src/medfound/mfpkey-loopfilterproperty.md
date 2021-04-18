---
description: Especifica se o codec deve usar o filtro de desbloqueio no loop durante a codificação.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: Propriedade MFPKEY_LOOPFILTER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810720"
---
# <a name="mfpkey_loopfilter-property"></a>\_Propriedade MFPKEY LOOPFILTER

Especifica se o codec deve usar o filtro de desbloqueio no loop durante a codificação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCLoopFilter

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="remarks"></a>Comentários

O filtro em loop é um método de debloqueio que é aplicado durante a codificação e decodificação, para reduzir os artefatos de bloqueio no tempo de codificação ("no loop") para que os quadros P e B futuros não os carreguem.

O efeito de aplicar o filtro em loop é que as bordas dos blocos de macro nos quadros de vídeo de saída são menos perceptíveis. Ao mesmo tempo, a imagem pode se tornar mais suave na aparência.

Embora o filtro em loop possa levar a uma redução nos detalhes da imagem em alguns quadros, a qualidade geral do vídeo terá um benefício perceptível. A maior desvantagem de usar a filtragem no loop é o custo adicional de decodificação de desempenho.

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

 

 




