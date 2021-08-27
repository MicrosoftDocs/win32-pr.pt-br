---
description: Especifica como o fluxo de vídeo decodificado é entrelaçado.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Propriedade AVDecVideoInputScanType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b86c9499019cdc07f095bf65be5817b828c78d277b02810bc1612cc0365edce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108696"
---
# <a name="avdecvideoinputscantype-property"></a>Propriedade AVDecVideoInputScanType

Especifica como o fluxo de vídeo decodificado é entrelaçado.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoInputScanType**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) .

## <a name="remarks"></a>Comentários

Os 16 bits superiores do valor contêm a largura e os 16 bits inferiores contêm a altura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

