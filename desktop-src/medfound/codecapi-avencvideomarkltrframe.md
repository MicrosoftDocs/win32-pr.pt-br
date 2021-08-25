---
description: Marca o quadro atual como um quadro LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a62f7bed0fd913dd17e06055ad259f4c8ed7037d90df2ecc53100e14ec4e505a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606426"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>Propriedade CODECAPI \_ AVEncVideoMarkLTRFrame

Marca o quadro atual como um quadro LTR.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Comentários

**Codificadores H.264/AVC:**

O valor desse controle é o valor da sintaxe H.264 *LongTermFramIdx* associada ao quadro atual. Se o quadro atual não estiver na camada base, por exemplo, a *\_ ID temporal* do elemento de sintaxe não for igual a 0, essa propriedade se aplicará ao próximo quadro de camada base na ordem de codificação.

Essa propriedade não deverá ser chamada se uma chamada pendente para marcar um quadro LTR tiver sido emitida usando a propriedade CODECAPI AVEncVideoMarkLTRFrame e o codificador ainda não tiver marcado um quadro como \_ LTR. Em outras palavras, o codificador não deve enfileirar solicitações \_ CODECAPI AVEncVideoMarkLTRFrame. Se uma solicitação CODECAPI AVEncVideoMarkLTRFrame for enviada enquanto outra solicitação \_ CODECAPI AVEncVideoMarkLTRFrame ainda estiver pendente, a solicitação mais antiga deverá \_ ser retirada.

A propriedade CODECAPI AVEncVideoMarkLTRFrame é dinâmica e pode ser definida durante \_ a sessão de codificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




