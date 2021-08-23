---
title: Trabalhando com o player
description: Trabalhando com o player
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player capas, atributo de jogador no JScript
- skins, atributo de player no JScript
- atributos, player
- atributo player
- JScript arquivos para capas, atributo de player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77098f161244488d5097d2d022f105628a43ba50a40218da01295d99f2de0cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566978"
---
# <a name="working-with-the-player"></a>Trabalhando com o player

Ao usar o Microsoft JScript para acessar métodos e propriedades do Windows Media Player, você deve usar o nome "player" para o nome do controle. Por exemplo, para referenciar o método Stop, você deve digitar:


```C++
player.Controls.Stop()

```



O **atributo** global do player é a chave para acessar o controle Windows Media Player por meio de scripts de capa. Por meio desse atributo, todos os objetos do controle Windows Media Player se tornam acessíveis para modificação em tempo de executar por meio de suas propriedades e métodos. Além disso, o **elemento PLAYER** está disponível para que você possa especificar manipuladores de eventos e o atributo **de URL** em tempo de design.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando JScript**](using-jscript.md)
</dt> </dl>

 

 




