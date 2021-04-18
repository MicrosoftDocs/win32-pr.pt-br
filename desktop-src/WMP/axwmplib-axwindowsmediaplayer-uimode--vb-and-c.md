---
title: Propriedade AxWindowsMediaPlayer. uiMode
description: A propriedade uiMode Obtém ou define um valor que indica quais controles são mostrados na interface do usuário.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- Propriedade uiMode Windows Media Player
- Propriedade uiMode Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781057"
---
# <a name="axwindowsmediaplayeruimode-property"></a>Propriedade AxWindowsMediaPlayer. uiMode

A propriedade uiMode Obtém ou define um valor que indica quais controles são mostrados na interface do usuário.

## <a name="syntax"></a>Syntax


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um System. String que é um dos valores a seguir.



| Valor     | Descrição                                                                                                                                                                                                     | Exemplo de áudio                                                   | Exemplo de vídeo                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| invisível | O Windows Media Player é incorporado sem nenhuma interface do usuário visível (janela controles, vídeo ou visualização).                                                                                                  | (Nada é exibido.)                                         | (Nada é exibido.)                                         |
| none      | O Windows Media Player é inserido sem controles e apenas com a janela de vídeo ou visualização exibida.                                                                                                   | ![UIMode = ' none ' com áudio](images/uimode-none-audio-v11.png) | ![UIMode = ' none ' com vídeo](images/uimode-none-video-v11.png) |
| mini-aba      | O Windows Media Player é inserido com os controles janela de status, reproduzir/pausar, parar, desativar mudo e volume mostrados além da janela vídeo ou visualização.                                                    | ![UIMode = ' Mini ' com áudio](images/uimode-mini-audio-v11.png) | ![UIMode = ' Mini ' com vídeo](images/uimode-mini-video-v11.png) |
| completa      | Padrão. O Windows Media Player é inserido com os controles janela de status, barra de busca, reproduzir/pausar, parar, desativar mudo, avançar, anterior, avançar, retroceder e volume, além da janela vídeo ou visualização. | ![UIMode = ' full ' com áudio](images/uimode-full-audio-v11.png) | ![UIMode = ' full ' com vídeo](images/uimode-full-video-v11.png) |
| custom    | O Windows Media Player é inserido com uma interface de usuário personalizada. Só pode ser usado em programas C++.                                                                                                                | (A interface do usuário personalizada é exibida.)                           | (A interface do usuário personalizada é exibida.)                           |



 

## <a name="remarks&quot;></a>Comentários

Esta propriedade especifica a aparência do Windows Media Player inserido. Quando **UIMODE** é definido como &quot;None&quot;, &quot;mini&quot; ou &quot;Full&quot;, uma janela está presente para a exibição de clipes de vídeo e visualizações de áudio. Essa janela pode ser ocultada no modo mini ou Full, definindo o atributo **Height** da marca **Object** como 40, que é medido a partir da parte inferior e deixa a parte dos controles da interface do usuário visível. Se nenhuma interface inserida for desejada, defina os atributos **Width** e **Height** como zero.

Se **UIMODE** for definido como &quot;invisível&quot;, nenhuma interface do usuário será exibida, mas o espaço ainda será reservado na página, conforme especificado por **largura** e **altura**. Isso é útil para reter o layout da página quando **UIMODE** pode mudar. Além disso, o espaço reservado é transparente, portanto, todos os elementos em camadas por trás do controle ficarão visíveis.

Se **UIMODE** for definido como &quot;Full&quot; ou &quot;mini&quot;, o Windows Media Player exibirá os controles de transporte no modo de tela inteira. Se **UIMODE** for definido como &quot;None&quot;, nenhum controle será exibido no modo de tela inteira.

Se a janela estiver visível e o conteúdo de áudio estiver sendo reproduzido, a visualização exibida será aquela usada mais recentemente no Windows Media Player.

Se **UIMODE** for definido como &quot;Custom&quot; em um programa C++ que implementa **IWMPRemoteMediaServices**, o arquivo de capa indicado por **IWMPRemoteMediaServices. GetCustomUIMode** será exibido.

Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a &quot;None&quot;.

## <a name=&quot;examples&quot;></a>Exemplos

O exemplo a seguir cria uma caixa de listagem que permite ao usuário alterar o modo de interface do usuário para um objeto incorporado do Windows Media Player. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player versão 7,0 ou posterior. Windows Media Player 9 Series ou posterior para "invisível" ou "personalizado"<br/>   |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. enableContextMenu (VB e C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





