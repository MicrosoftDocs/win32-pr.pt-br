---
description: Especifica o tipo de sala para um fluxo de áudio Dolby Digital. Essa propriedade se aplica aos codificadores Dolby Digital Audio.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propriedade AVEncDDProductionRoomType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087832"
---
# <a name="avencddproductionroomtype-property"></a>Propriedade AVEncDDProductionRoomType

Especifica o tipo de sala para um fluxo de áudio Dolby Digital. Essa propriedade se aplica aos codificadores Dolby Digital Audio.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncDDProductionRoomType**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .

## <a name="remarks"></a>Comentários

*Tipo de sala* refere-se ao tamanho da sala usada durante a produção. Se você definir essa propriedade, defina a propriedade [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) como **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

