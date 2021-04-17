---
title: Objeto externo para lojas online do tipo 2
description: Objeto externo para lojas online do tipo 2
ms.assetid: d12e7480-39ec-4d32-9cf9-5555d0f92d80
keywords:
- Armazenamentos online do Windows Media Player, objetos externos
- lojas online, objetos externos
- tipo 2 lojas online, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c412cac301d61aeb791131e85bb8bc60f390201d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498738"
---
# <a name="external-object-for-type-2-online-stores"></a>Objeto externo para lojas online do tipo 2

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O objeto **externo** pode fornecer funcionalidade para páginas da Web que são fornecidas por uma loja online do tipo 2 e hospedadas no Windows Media Player.

O objeto **externo** expõe as propriedades a seguir.



| Propriedade                                                        | Descrição                                                                               |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md) | Recupera a cor de realce do botão atual para a interface do usuário do Windows Media Player. |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md) | Recupera a cor de foco do botão atual para a interface do usuário do Windows Media Player.     |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)       | Recupera a cor de sombra do botão atual para a interface do usuário do Windows Media Player.    |
| [appColorDark](external-appcolordark.md)                       | Recupera a cor do sombreamento escuro atual da interface do usuário do Windows Media Player.       |
| [appColorLight](external-appcolorlight.md)                     | Recupera a cor atual de sombreamento claro da interface do usuário do Windows Media Player.      |
| [appColorMedium](external-appcolormedium.md)                   | Recupera a cor de sombreamento médio atual da interface do usuário do Windows Media Player.     |
| [DownloadManager](external-downloadmanager.md)                 | Recupera o objeto **DownloadManager** .                                                 |
| [SelectedTaskPane](external-selectedtaskpane.md)               | Especifica ou recupera o painel de tarefas selecionado no momento.                                  |
| [version](external-version.md)                                 | Recupera a versão atual do Windows Media Player.                                    |



 

O objeto **externo** expõe os métodos a seguir.



| Método                                                  | Descrição                                                                          |
|---------------------------------------------------------|--------------------------------------------------------------------------------------|
| [NavigateTaskPaneURL](external-navigatetaskpaneurl.md) | Abre uma página da Web no painel de tarefas especificado e altera o foco para o painel especificado. |
| [playMedia (preterido)](external-playmedia.md)        | Especifica a URL de um item de mídia digital a ser reproduzido.                                   |



 

O objeto **externo** expõe o evento a seguir.



| Evento                                             | Descrição                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [OnColorChange](external-oncolorchange-event.md) | Ocorre quando a cor da interface do usuário do Windows Media Player é alterada. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




