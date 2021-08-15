---
title: EQUALIZERSETTINGS. Speakers
description: O atributo Speakize especifica ou recupera o número de índice do tamanho atual do alto-falante.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. Speakers Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d289a89a22e8c10cf669e9b55fc304826acb3ce0f72468f725e7d5fae0dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748644"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS. Speakers

O atributo **speakize** especifica ou recupera o número de índice do tamanho atual do alto-falante.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (Long) que contém um dos valores a seguir.



| Valor | Descrição                              |
|-------|------------------------------------------|
| 0     | Os alto-falantes atuais são fones de ouvido.     |
| 1     | Os alto-falantes atuais são do tamanho normal. |
| 2     | Os alto-falantes atuais são grandes.          |



 

## <a name="remarks"></a>Comentários

O nome amigável do tamanho do orador pode ser recuperado usando o atributo **currentSpeakerName** .

Esse atributo será ignorado se **enhancedAudio** estiver definido como false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





