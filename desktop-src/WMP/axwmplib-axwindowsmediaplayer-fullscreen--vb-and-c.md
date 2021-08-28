---
title: Propriedade AxWindowsMediaPlayer. fullScreen
description: A propriedade fullScreen Obtém ou define um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Windows Media Player da propriedade fullScreen
- propriedade fullScreen Windows Media Player, classe AxWindowsMediaPlayer
- classe AxWindowsMediaPlayer Windows Media Player, propriedade fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e128d8c7e0cf49d3feaae723a7fb5a51740cda47e5016df6290b4852c20ec27b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902616"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>Propriedade AxWindowsMediaPlayer. fullScreen

A propriedade fullScreen Obtém ou define um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um valor System. Boolean que indica se o conteúdo é reproduzido no modo de tela inteira. O valor padrão é false.

## <a name="remarks"></a>Comentários

para que o modo de tela inteira funcione corretamente ao inserir o controle de Windows Media Player, a área de exibição de vídeo deve ter uma altura e largura de pelo menos um pixel. Se **UIMODE** for definido como "mini" ou "Full", a altura do controle em si deverá ser 65 ou maior para acomodar a área de exibição do vídeo além da interface do usuário.

Se **UIMODE** for definido como "invisível", a configuração dessa propriedade como true gerará um erro e não afetará o comportamento do controle.

durante a reprodução de tela inteira, Windows Media Player oculta o cursor do mouse quando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) é igual a false e **uiMode** é igual a "none".

se **uiMode** for definido como "full" ou "mini", Windows Media Player exibirá controles de transporte no modo de tela inteira quando o cursor do mouse se mover. Após um breve intervalo de sem movimento do mouse, os controles de transporte ficam ocultos. Se **UIMODE** for definido como "None", nenhum controle será exibido no modo de tela inteira.

> [!Note]  
> a exibição de controles de transporte no modo de tela inteira requer o sistema operacional Windows XP.

 

se os controles de transporte não forem exibidos no modo de tela inteira, Windows Media Player sairá automaticamente no modo de tela inteira quando a reprodução for interrompida.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um botão que usa a propriedade fullScreen para alternar um objeto de player incorporado para o modo de tela inteira. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                  |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                            |
| Assembly<br/>  | <dl> <dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. uiMode (VB e C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





