---
title: Trabalhando com o Player
description: Trabalhando com o Player
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Capas do Windows Media Player, atributo Player no JScript
- capas, atributo Player em JScript
- atributos, Player
- atributo do Player
- Arquivos JScript para capas, atributo Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364448"
---
# <a name="working-with-the-player"></a>Trabalhando com o Player

Ao usar o Microsoft JScript para acessar métodos e propriedades do Windows Media Player, você deve usar o nome "Player" para o nome do controle. Por exemplo, para fazer referência ao método stop, você deve digitar:


```C++
player.Controls.Stop()

```



O atributo global do **Player** é a chave para acessar o controle do Windows Media Player por meio de script de capa. Por meio desse atributo, todos os objetos do controle do Windows Media Player tornam-se acessíveis para a modificação de tempo de execução por meio de suas propriedades e métodos. Além disso, o elemento **Player** está disponível para que você possa especificar manipuladores de eventos e o atributo **URL** em tempo de design.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o JScript**](using-jscript.md)
</dt> </dl>

 

 




