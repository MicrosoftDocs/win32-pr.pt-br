---
title: Objeto externo para repositórios online do tipo 1
description: Objeto externo para repositórios online do tipo 1
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Armazenamentos online do Windows Media Player, objetos externos
- lojas online, objetos externos
- tipos 1 lojas online, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f50e5e6bfc98ea3669996b06fa4a4defb52452fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916584"
---
# <a name="external-object-for-type-1-online-stores"></a>Objeto externo para repositórios online do tipo 1

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O objeto **externo** fornece funcionalidade a páginas da Web, fornecidas por uma loja online, hospedada no Windows Media Player.

O objeto **externo** expõe as seguintes propriedades para lojas online do tipo 1.



| Propriedade                                                                                  | Descrição                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Recupera o tipo de conta do usuário atual.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Recupera a cor de realce do botão atual para a interface do usuário do Windows Media Player.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Recupera a cor de foco do botão atual para a interface do usuário do Windows Media Player.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Recupera a cor de sombra do botão atual para a interface do usuário do Windows Media Player.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Recupera a cor do sombreamento escuro atual da interface do usuário do Windows Media Player.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Recupera a cor atual de sombreamento claro da interface do usuário do Windows Media Player.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Recupera a cor de sombreamento médio atual da interface do usuário do Windows Media Player.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Recupera o título do botão no painel de lista (também chamado de cesta) no Windows Media Player.                                     |
| [filter](external-filter.md)                                                             | Recupera o filtro de pesquisa em uso no momento pelo Windows Media Player.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Especifica se o Windows Media Player deve ignorar o histórico do Internet Explorer.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Recupera o identificador de um item de mídia específico que é exibido no momento no modo de exibição do Player.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Recupera uma [constante de local de biblioteca](library-location-constants.md) que indica o tipo de exibição atual no Windows Media Player. |
| [pluginRunning](external-pluginrunning.md)                                               | Recupera um valor que indica se o plug-in do repositório online está em execução.                                                          |
| [selectedItemid](external-selecteditemid.md)                                             | Recupera o identificador do item de mídia selecionado no momento no Windows Media Player.                                           |
| [selectedItemtype](external-selecteditemtype.md)                                         | Recupera o tipo do item de mídia selecionado no momento no Windows Media Player.                                                 |
| [agenda](external-task.md)                                                                 | Recupera o nome do painel de tarefas atual.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indica se o feed representado pela página de descoberta atual está sendo exibido no controle de exibição de árvore de biblioteca local.          |
| [userlogin](external-userloggedin.md)                                                 | Recupera um valor que indica se o usuário está conectado à loja online.                                                          |
| [version](external-version.md)                                                           | Recupera a versão atual do Windows Media Player.                                                                                   |
| [viewparameters](external-viewparameters.md)                                             | Recupera os parâmetros associados à exibição atual no Windows Media Player.                                                           |



 

O objeto **externo** expõe os seguintes métodos para lojas online do tipo 1.



| Método                                                            | Descrição                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Adiciona itens de mídia ao painel de lista (também chamado de cesta) no Windows Media Player.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Exibe uma caixa de diálogo para que o usuário possa tentar fazer logon na loja online.                                                 |
| [authenticate](external-authenticate.md)                         | Inicia uma tentativa de autenticar o usuário.                                                                               |
| [comprar](external-buy.md)                                           | Inicia a compra de um conjunto de itens de mídia.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informa ao Windows Media Player que ele não deve exibir uma nova página de descoberta, embora a exibição tenha sido alterada no Player. |
| [changeView](external-changeview.md)                             | Altera a exibição no Windows Media Player.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Altera a exibição no Windows Media Player para exibir uma lista gerada dinamicamente pela loja online.                        |
| [download](external-download.md)                                 | Inicia o download de um conjunto de itens de mídia.                                                                              |
| [reproduzir](external-play.md)                                         | Instrui o Windows Media Player a reproduzir um conjunto de itens de mídia.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Cria uma lista de reprodução dos itens de mídia na exibição atual e salva a lista de reprodução na biblioteca local.                     |
| [sendMessage](external-sendmessage.md)                           | Envia uma mensagem para o plug-in da loja online.                                                                               |
| [showPopup](external-showpopup.md)                               | Instrui o Windows Media Player a exibir uma página da Web pop-up; ou seja, uma página da Web que aparece em uma janela separada.            |



 

O objeto **externo** expõe os seguintes eventos para lojas online do tipo 1.



| Evento                                                                         | Descrição                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Ocorre quando uma chamada para o método **external. ChangeView** resulta em um erro.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Ocorre quando uma chamada para o método **external. ChangeViewOnlineList** resulta em um erro. |
| [OnColorChange](external-oncolorchange-event.md)                             | Ocorre quando a cor da interface do usuário do Windows Media Player é alterada.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Ocorre quando o status de logon do usuário é alterado ou quando uma tentativa de logon falha.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Ocorre quando o armazenamento online termina de processar uma mensagem.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Ocorre quando a exibição é alterada no Windows Media Player.                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




