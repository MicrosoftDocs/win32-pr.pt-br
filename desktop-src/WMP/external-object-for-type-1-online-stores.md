---
title: Objeto externo para lojas online do tipo 1
description: Objeto externo para lojas online do tipo 1
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player online, objetos externos
- lojas online, objetos externos
- tipo 1 lojas online, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7d95d2ca332b88edea73da2238374aeffc52e520d7bc0346eab9f4eb7a05f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648996"
---
# <a name="external-object-for-type-1-online-stores"></a>Objeto externo para lojas online do tipo 1

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **objeto** Externo fornece funcionalidade para páginas da Web, fornecidas por uma loja online, hospedadas em Windows Media Player.

O **objeto** Externo expõe as propriedades a seguir para lojas online do tipo 1.



| Propriedade                                                                                  | Descrição                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Accounttype](external-accounttype.md)                                                   | Recupera o tipo de conta do usuário atual.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Recupera a cor de realçada do botão atual para a Windows Media Player do usuário.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Recupera a cor de foco do botão atual para a Windows Media Player do usuário.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Recupera a cor de sombra do botão atual para a Windows Media Player do usuário.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Recupera a cor sombreada escura atual da interface Windows Media Player usuário.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Recupera a cor sombreada à luz atual da interface Windows Media Player usuário.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Recupera a cor sombreada média atual da interface Windows Media Player usuário.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Recupera o título do botão no painel de lista (também chamado de cesta) no Windows Media Player.                                     |
| [filter](external-filter.md)                                                             | Recupera o filtro de pesquisa atualmente em uso por Windows Media Player.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Especifica se Windows Media Player deve ignorar Internet Explorer histórico.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Recupera o identificador de um item de mídia específico que é exibido atualmente na exibição do Player.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Recupera uma constante [de local de](library-location-constants.md) biblioteca que indica o tipo da exibição atual no Windows Media Player. |
| [pluginRunning](external-pluginrunning.md)                                               | Recupera um valor que indica se o plug-in da loja online está em execução.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | Recupera o identificador do item de mídia selecionado no momento Windows Media Player.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | Recupera o tipo do item de mídia selecionado atualmente no Windows Media Player.                                                 |
| [Tarefa](external-task.md)                                                                 | Recupera o nome do painel de tarefas atual.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indica se o feed representado pela página de descoberta atual está sendo exibido no controle de exibição de árvore da biblioteca local.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Recupera um valor que indica se o usuário está conectado à loja online.                                                          |
| [version](external-version.md)                                                           | Recupera a versão atual do Windows Media Player.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | Recupera parâmetros associados à exibição atual no Windows Media Player.                                                           |



 

O **objeto** Externo expõe os métodos a seguir para lojas online do tipo 1.



| Método                                                            | Descrição                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Adiciona itens de mídia ao painel de lista (também chamado de cesta) no Windows Media Player.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Exibe uma caixa de diálogo para que o usuário possa tentar fazer logoff na loja online.                                                 |
| [authenticate](external-authenticate.md)                         | Inicia uma tentativa de autenticar o usuário.                                                                               |
| [comprar](external-buy.md)                                           | Inicia a compra de um conjunto de itens de mídia.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informa Windows Media Player que ela não deve exibir uma nova página de descoberta, mesmo que a exibição tenha sido alterada no Player. |
| [changeView](external-changeview.md)                             | Altera a exibição em Windows Media Player.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Altera a exibição Windows Media Player para exibir uma lista gerada dinamicamente pela loja online.                        |
| [download](external-download.md)                                 | Inicia o download de um conjunto de itens de mídia.                                                                              |
| [Jogar](external-play.md)                                         | Instrui Windows Media Player reproduzir um conjunto de itens de mídia.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Cria uma playlist dos itens de mídia na exibição atual e salva a playlist na biblioteca local.                     |
| [Sendmessage](external-sendmessage.md)                           | Envia uma mensagem para o plug-in da loja online.                                                                               |
| [showPopup](external-showpopup.md)                               | Instrui Windows Media Player exibir uma página da Web pop-up; ou seja, uma página da Web que aparece em uma janela separada.            |



 

O **objeto** Externo expõe os seguintes eventos para lojas online do tipo 1.



| Evento                                                                         | Descrição                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Ocorre quando uma chamada para o **método External.ChangeView** resulta em um erro.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Ocorre quando uma chamada para o **método External.ChangeViewOnlineList** resulta em um erro. |
| [OnColorChange](external-oncolorchange-event.md)                             | Ocorre quando a cor da interface do Windows Media Player usuário muda.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Ocorre quando o status de logoff do usuário muda ou quando uma tentativa de fazer logoff falha.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Ocorre quando a loja online concluiu o processamento de uma mensagem.                         |
| [Onviewchange](external-onviewchange-event.md)                               | Ocorre quando a exibição é Windows Media Player.                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




