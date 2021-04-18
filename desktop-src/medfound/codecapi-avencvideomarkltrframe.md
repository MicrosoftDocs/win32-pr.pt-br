---
description: Marca o quadro atual como um quadro EPD.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: Propriedade CODECAPI_AVEncVideoMarkLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501194"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>\_Propriedade CODECAPI AVEncVideoMarkLTRFrame

Marca o quadro atual como um quadro EPD.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Comentários

**Codificadores H. 264/AVC:**

O valor desse controle é o valor da sintaxe H. 264 *LongTermFramIdx* associada ao quadro atual. Se o quadro atual não estiver na camada base, por exemplo, a *\_ ID temporal* do elemento de sintaxe não for igual a 0, essa propriedade se aplicará ao próximo quadro de camada base na ordem de codificação.

Essa propriedade não deverá ser chamada se uma chamada pendente para marcar um quadro EPD tiver sido emitida usando a \_ Propriedade CODECAPI AVEncVideoMarkLTRFrame e o codificador ainda não tiver marcado um quadro como LTR. Em outras palavras, o codificador não deve enfileirar \_ as solicitações CODECAPI AVEncVideoMarkLTRFrame. Se uma \_ solicitação CODECAPI AVEncVideoMarkLTRFrame for enviada enquanto outra \_ solicitação AVEncVideoMarkLTRFrame CODECAPI ainda estiver pendente, a solicitação mais antiga deverá ser descartada.

A \_ Propriedade CODECAPI AVEncVideoMarkLTRFrame é dinâmica e pode ser definida durante a sessão de codificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




