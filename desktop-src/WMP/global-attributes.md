---
title: atributos globais (Windows Media Player SDK)
description: Atributos globais
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- aparências de Windows Media Player, atributos globais
- capas, atributos globais
- referência para capas, atributos globais
- atributos globais
- atributos, global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2d52b6489a28eff20e3a7e5c7180fc9e2db9309c0fe42880bfc779a23f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648076"
---
# <a name="global-attributes"></a>Atributos globais

Atributos globais são atributos que fornecem fácil acesso a determinados elementos ou objetos do player de qualquer lugar dentro de uma capa.

O atributo global do **Player** é uma referência ao objeto do [Player](player-object.md) e é usado para acessar a funcionalidade principal do Windows Media Player. O exemplo a seguir usa o **Player** para iniciar a reprodução de mídia digital.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



O atributo global **Theme** é uma referência ao elemento [Theme](theme-element.md) . Essa é a maneira apropriada de acessar atributos de **tema** , em vez de especificar uma ID dentro do elemento **Theme** . O exemplo a seguir usa o **tema** para abrir uma nova exibição.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



O atributo global **View** é uma referência à [exibição](view-element.md)atual. Isso pode ser usado em vez da ID especificada nos vários elementos de **exibição** . O exemplo a seguir usa **View** para fechar a exibição atual.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



O atributo global de **evento** é usado para acessar os atributos de evento de ambiente a partir de manipuladores de eventos. O exemplo a seguir usa o **evento** para determinar se a tecla Alt é pressionada quando um botão é clicado.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



O atributo global **playerApplication** é uma referência ao objeto [playerApplication](playerapplication-object.md) e é usado por arquivos de capa fornecidos como interfaces de usuário personalizadas para controles de Player remotos. O controle Player só pode ser inserido no modo remoto em programas C++ que implementam a interface **IWMPRemoteMediaServices** . O exemplo a seguir usa **playerApplication** para alternar para o modo completo do Player.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Para obter mais informações, consulte [atributos de evento de ambiente](ambient-event-attributes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Diversos**](miscellaneous.md)
</dt> </dl>

 

 




