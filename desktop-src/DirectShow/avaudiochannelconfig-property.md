---
description: Obtém a configuração do alto-falante para os canais de áudio no fluxo de bits de áudio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propriedade AVAudioChannelConfig (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba9c497305292abeb34b86a7989fb05fbb872c898d10743ebd93b3982089e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983786"
---
# <a name="avaudiochannelconfig-property"></a>Propriedade AVAudioChannelConfig

Obtém a configuração do alto-falante para os canais de áudio no fluxo de bits de áudio.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVAudioChannelConfig**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é uma operação OR dos membros da enumeração [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .

## <a name="remarks"></a>Comentários

O número de canais inclui o canal de baixo efeito de frequência (LFE), se presente.

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

 

 




