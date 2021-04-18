---
title: Player. uiMode
description: A propriedade uiMode especifica ou recupera um valor que indica quais controles são mostrados na interface do usuário.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player. uiMode Windows Media Player
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784545"
---
# <a name="playeruimode"></a>Player. uiMode

A propriedade **UIMODE** especifica ou recupera um valor que indica quais controles são mostrados na interface do usuário.

## <a name="syntax"></a>Syntax

*Player* . **UIMODE**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.



| Valor     | Descrição                                                                                                                                                                                                           | Exemplo de áudio                                          | Exemplo de vídeo                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| invisível | O Windows Media Player é incorporado sem nenhuma interface do usuário visível (janela controles, vídeo ou visualização).                                                                                                        | (Nada é exibido.)                                | (Nada é exibido.)                                |
| none      | O Windows Media Player é inserido sem controles e apenas com a janela de vídeo ou visualização exibida.                                                                                                         | !["nenhum" com áudio](images/uimode-none-audio-v11.png) | !["nenhum" com vídeo](images/uimode-none-video-v11.png) |
| mini-aba      | O Windows Media Player é inserido com os controles janela de status, reproduzir/pausar, parar, desativar mudo e volume mostrados além da janela vídeo ou visualização.                                                          | !["mini" com áudio](images/uimode-mini-audio-v11.png) | !["mini" com vídeo](images/uimode-mini-video-v11.png) |
| completa      | Padrão. O Windows Media Player é inserido com os controles janela de status, barra de busca, reproduzir/pausar, parar, desativar mudo, avançar, anterior, avançar, reverter e volume, além da janela de vídeo ou visualização. | !["completo" com áudio](images/uimode-full-audio-v11.png) | !["completo" com vídeo](images/uimode-full-video-v11.png) |
| custom    | O Windows Media Player é inserido com uma interface de usuário personalizada. Só pode ser usado em programas C++.                                                                                                                      | (A interface do usuário personalizada é exibida.)                  | (A interface do usuário personalizada é exibida.)                  |



 

## <a name="remarks"></a>Comentários

Esta propriedade especifica a aparência do Windows Media Player inserido. Quando **UIMODE** é definido como "None", "mini" ou "Full", uma janela está presente para a exibição de clipes de vídeo e visualizações de áudio. Essa janela pode ser ocultada no modo mini ou Full, definindo o atributo **Height** da marca **Object** como 40, que é medido a partir da parte inferior e deixa a parte dos controles da interface do usuário visível. Se nenhuma interface inserida for desejada, defina os atributos **Width** e **Height** como zero.

Se **UIMODE** for definido como "invisível", nenhuma interface do usuário será exibida, mas o espaço ainda será reservado na página, conforme especificado por **largura** e **altura**. Isso é útil para reter o layout da página quando **UIMODE** pode mudar. Além disso, o espaço reservado é transparente, portanto, todos os elementos em camadas por trás do controle ficarão visíveis.

Se **UIMODE** for definido como "Full" ou "mini", o Windows Media Player exibirá os controles de transporte no modo de tela inteira. Se **UIMODE** for definido como "None", nenhum controle será exibido no modo de tela inteira.

Se a janela estiver visível e o conteúdo de áudio estiver sendo reproduzido, a visualização exibida será aquela usada mais recentemente no Windows Media Player.

Se **UIMODE** for definido como "Custom" em um programa C++ que implementa **IWMPRemoteMediaServices**, o arquivo de capa indicado por **IWMPRemoteMediaServices:: GetCustomUIMode** será exibido.

Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML SELECT que permite ao usuário alterar a interface do usuário para um objeto de **Player** incorporado. O objeto de **jogador** foi criado com ID = "Player".


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



Windows Media Player 10 Mobile: essa propriedade só aceita ou retorna valores de "nenhum" ou "completo". Em dispositivos Smartphone, somente o status de reprodução e um contador são exibidos quando *UIMODE* é definido como "Full".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior. Windows Media Player 9 Series ou posterior para "invisível" ou "personalizado".<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





