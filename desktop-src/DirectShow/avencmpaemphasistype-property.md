---
description: Especifica o tipo de filtro de des ênfase que deve ser usado durante a decodificação. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Propriedade AVEncMPAEmphasisType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3da73e2708acde7a5b388d229a3a82c50a2dff04c4f2873551a992fe738189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824226"
---
# <a name="avencmpaemphasistype-property"></a>Propriedade AVEncMPAEmphasisType

Especifica o tipo de filtro de des ênfase que deve ser usado durante a decodificação. Essa propriedade se aplica a codificadores de áudio MPEG.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPAEmphasisType**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVEncMPAEmphasisType.**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)

## <a name="remarks"></a>Comentários

Essa propriedade define os bits de ênfase no header do quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

