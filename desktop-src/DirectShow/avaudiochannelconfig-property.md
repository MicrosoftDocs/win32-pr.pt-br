---
description: Obtém a configuração do alto-falante para os canais de áudio no fluxo de bits de áudio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propriedade AVAudioChannelConfig (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009948"
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
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




