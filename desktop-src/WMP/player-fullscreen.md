---
title: Player. tela inteira
description: A propriedade fullScreen especifica ou recupera um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. tela inteira do Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781356"
---
# <a name="playerfullscreen"></a>Player. tela inteira

A propriedade **fullscreen** especifica ou recupera um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.

## <a name="syntax"></a>Syntax

*Player* . **tela inteira**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** de leitura/gravação.



| Valor | Descrição                                                    |
|-------|----------------------------------------------------------------|
| true  | O conteúdo de vídeo é reproduzido no modo de tela inteira.              |
| false | Padrão. O conteúdo de vídeo não é reproduzido no modo de tela inteira. |



 

## <a name="remarks"></a>Comentários

Para que o modo de tela inteira funcione corretamente ao inserir o controle do Windows Media Player, a área de exibição de vídeo deve ter uma altura e largura de pelo menos um pixel. Se **UIMODE** for definido como "mini" ou "Full", a altura do controle em si deverá ser 65 ou maior para acomodar a área de exibição do vídeo além da interface do usuário.

Se **UIMODE** for definido como "invisível", a configuração dessa propriedade como true gerará um erro e não afetará o comportamento do controle.

Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".

Se **UIMODE** for definido como "Full" ou "mini", o Windows Media Player exibirá controles de transporte no modo de tela inteira quando o cursor do mouse se mover. Após um breve intervalo de sem movimento do mouse, os controles de transporte ficam ocultos. Se **UIMODE** for definido como "None", nenhum controle será exibido no modo de tela inteira.

**Observação**

A exibição de controles de transporte no modo de tela inteira requer o sistema operacional Windows XP.

Se os controles de transporte não forem exibidos no modo de tela inteira, o Windows Media Player sairá automaticamente do modo de tela inteira quando a reprodução for interrompida.

**Observação**

Sempre certifique-se de informar ao usuário como retornar do modo de tela inteira.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um botão de entrada HTML que usa o *Player*. **tela inteira** para alternar um objeto de player incorporado para o modo de tela inteira. O objeto de **jogador** foi criado com ID = "Player".


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





