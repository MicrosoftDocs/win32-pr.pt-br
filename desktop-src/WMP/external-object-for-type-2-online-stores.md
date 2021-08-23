---
title: Objeto externo para lojas online do tipo 2
description: Objeto externo para lojas online do tipo 2
ms.assetid: d12e7480-39ec-4d32-9cf9-5555d0f92d80
keywords:
- Windows Media Player online, objetos externos
- lojas online, objetos externos
- tipo 2 lojas online, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d177dd4bcac34e5a8e8a72f53f184c4e0dfffec41b3cef0c0080e2fe1840cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648876"
---
# <a name="external-object-for-type-2-online-stores"></a>Objeto externo para lojas online do tipo 2

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **objeto** Externo pode fornecer funcionalidade para páginas da Web fornecidas por um armazenamento online do tipo 2 e hospedadas em Windows Media Player.

O **objeto** Externo expõe as propriedades a seguir.



| Propriedade                                                        | Descrição                                                                               |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md) | Recupera a cor de realçada do botão atual para a Windows Media Player do usuário. |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md) | Recupera a cor de foco do botão atual para a Windows Media Player do usuário.     |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)       | Recupera a cor de sombra do botão atual para a Windows Media Player do usuário.    |
| [appColorDark](external-appcolordark.md)                       | Recupera a cor sombreada escura atual da interface Windows Media Player usuário.       |
| [appColorLight](external-appcolorlight.md)                     | Recupera a cor sombreada à luz atual da interface Windows Media Player usuário.      |
| [appColorMedium](external-appcolormedium.md)                   | Recupera a cor sombreada média atual da interface Windows Media Player usuário.     |
| [DownloadManager](external-downloadmanager.md)                 | Recupera o **objeto DownloadManager.**                                                 |
| [SelectedTaskPane](external-selectedtaskpane.md)               | Especifica ou recupera o painel de tarefas selecionado no momento.                                  |
| [version](external-version.md)                                 | Recupera a versão atual do Windows Media Player.                                    |



 

O **objeto** Externo expõe os métodos a seguir.



| Método                                                  | Descrição                                                                          |
|---------------------------------------------------------|--------------------------------------------------------------------------------------|
| [NavigateTaskPaneURL](external-navigatetaskpaneurl.md) | Abre uma página da Web no painel de tarefas especificado e altera o foco para o painel especificado. |
| [playMedia (preterido)](external-playmedia.md)        | Especifica a URL de um item de mídia digital a ser reproduzir.                                   |



 

O **objeto** Externo expõe o evento a seguir.



| Evento                                             | Descrição                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [OnColorChange](external-oncolorchange-event.md) | Ocorre quando a cor da interface do Windows Media Player usuário muda. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




