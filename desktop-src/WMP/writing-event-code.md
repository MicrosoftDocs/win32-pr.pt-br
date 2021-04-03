---
title: Gravando código de evento
description: Gravando código de evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Capas do Windows Media Player, escrevendo código
- capas, escrevendo código
- eventos, escrevendo código
- escrevendo código para capas, sobre
- Capas, eventos do Windows Media Player
- capas, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006125"
---
# <a name="writing-event-code"></a>Gravando código de evento

Os eventos são tratados de forma semelhante aos atributos. Você deve dar um valor ao evento e o valor é o código que você deseja executar quando o evento acontece. A palavra "on" é adicionada à frente do nome do evento; por exemplo, o evento de clique ficará **onclick**.

O valor do evento está entre aspas duplas e começa com a palavra JScript seguida por dois-pontos. O código que você deseja executar vem em seguida, seguido por um ponto e vírgula e as aspas duplas de fechamento. Por exemplo, para interromper a reprodução quando o usuário clica em um botão, digite o seguinte como um atributo no código do elemento **Button** :


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Se você tiver um código que requer aspas, use aspas simples. É necessário tomar cuidado ao usar aspas para que elas sejam balanceadas corretamente. Veja um exemplo de como usar os dois tipos:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



Você também pode alterar os atributos da sua aparência ao manipular um evento externo. Por exemplo, para fechar um modo de exibição chamado MyView, você poderia digitar:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipulando eventos**](handling-events.md)
</dt> </dl>

 

 




