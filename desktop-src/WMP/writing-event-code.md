---
title: Escrevendo código de evento
description: Escrevendo código de evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player, escrevendo código
- capas, escrevendo código
- eventos, escrevendo código
- escrevendo código para capas, sobre
- Windows Media Player capas, eventos
- skins,events
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39c35864151db1671c2f7fa94caea803f0a33cc1082a3ae44082a90f7bddafb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760566"
---
# <a name="writing-event-code"></a>Escrevendo código de evento

Os eventos são tratados da mesma forma que os atributos. Você deve dar ao evento um valor e o valor é o código que você deseja executar quando o evento acontece. A palavra "on" é adicionada à frente do nome do evento; por exemplo, o evento de clique se **tornará onclick**.

O valor do evento está entre aspas duplas e começa com a palavra JScript seguida por dois-pontos. O código que você deseja executar vem em seguida, seguido por um ponto e vírgula e as aspas duplas de fechamento. Por exemplo, para interromper a reprodução quando o usuário clica em um botão, digite o seguinte como um atributo no código **do elemento BUTTON:**


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Se você tiver um código que exija aspas, use aspas simples. É necessário ter cuidado ao usar aspas para que elas sejam balanceadas corretamente. Aqui está um exemplo de como usar ambos os tipos:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



Você também pode alterar atributos da sua aparência ao manipular um evento externo. Por exemplo, para fechar uma exibição chamada myView, você pode digitar:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipulando eventos**](handling-events.md)
</dt> </dl>

 

 




