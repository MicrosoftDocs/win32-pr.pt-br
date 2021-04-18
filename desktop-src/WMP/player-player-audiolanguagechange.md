---
title: Evento Player. AudioLanguageChange
description: O evento AudioLanguageChange ocorre quando o idioma de áudio atual é alterado. | Evento Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Evento AudioLanguageChange do Windows Media Player
- Evento AudioLanguageChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento AudioLanguageChange
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763059"
---
# <a name="playeraudiolanguagechange-event"></a>Evento Player. AudioLanguageChange

O evento **AudioLanguageChange** ocorre quando o idioma de áudio atual é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LangID* 
</dt> <dd>

**Número** (**longo**) que especifica o novo LCID (identificador de localidade).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou passado para um método em um arquivo Microsoft JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





