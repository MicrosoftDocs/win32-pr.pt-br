---
title: Settings. AutoStart
description: A propriedade AutoStart especifica ou recupera um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Settings. AutoStart Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747699"
---
# <a name="settingsautostart"></a>Settings. AutoStart

A propriedade **AutoStart** especifica ou recupera um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.

## <a name="syntax"></a>Syntax

Player. Settings. AutoStart

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** de leitura/gravação.



| Valor | Descrição                                                         |
|-------|---------------------------------------------------------------------|
| true  | Padrão. O item de mídia começa a ser reproduzido automaticamente (consulte comentários). |
| false | O item de mídia não começa a ser reproduzido automaticamente.                |



 

## <a name="remarks"></a>Comentários

Se **AutoStart** for definido como true, o item de mídia começará a ser reproduzido quando o *Player*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** está definido. Caso contrário, ele não começará a ser reproduzido até os *controles*. o método **Play** é chamado.

Como a propriedade **AutoStart** para o modo completo do Windows Media Player pode ser definida globalmente por eventos externos (como carregar um CD), não há nenhum valor padrão confiável para capas e controles de Player remotos. Isso ocorre porque o mecanismo de reprodução do player de modo completo é usado em ambos os casos.

Você deve definir **AutoStart** como false imediatamente antes de definir o *Player*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** em capas e controles remotos do Windows Media Player se você quiser garantir que o item de mídia não comece a ser reproduzido imediatamente. Além disso, a menos que você defina **AutoStart** como true imediatamente antes de especificar um item de mídia, você não deve confiar nessa configuração como um substituto para usar os *controles*. método **Play** .

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de caixa de seleção HTML que permite ao usuário especificar se o controle de jogador reproduz o item de mídia atual automaticamente. O objeto de **jogador** foi criado com ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> </dl>

 

 





