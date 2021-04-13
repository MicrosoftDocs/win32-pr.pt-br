---
title: Propriedade DefaultAction
description: A propriedade DefaultAction de um objeto descreve o método principal de manipulação do objeto do ponto de vista do usuário. A propriedade DefaultAction de um objeto deve ser um verbo ou uma frase verbal curta.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291901"
---
# <a name="defaultaction-property"></a>Propriedade DefaultAction

A propriedade **DefaultAction** de um objeto descreve o método principal de manipulação do objeto do ponto de vista do usuário. A propriedade **DefaultAction** de um objeto deve ser um verbo ou uma frase verbal curta.

A propriedade **DefaultAction** é recuperada chamando [**IAccessible:: get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).

Para executar a ação padrão de um objeto, os clientes chamam [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).

Nem todos os objetos têm ações padrão e alguns objetos têm uma ação padrão relacionada à sua propriedade [**Value**](value-property.md) , como nos exemplos a seguir:

-   Uma caixa de seleção selecionada tem uma ação padrão de "desmarcar" e um valor de "marcado".
-   Uma caixa de seleção desmarcada tem uma ação padrão de "verificar" e um valor de "desmarcado".
-   Um botão chamado "Print" tem uma ação padrão de "Press", sem valor.
-   Um controle de texto estático ou um controle de edição que mostra "impressora" não tem nenhuma ação padrão, mas tem um valor de "impressora".

 

 




