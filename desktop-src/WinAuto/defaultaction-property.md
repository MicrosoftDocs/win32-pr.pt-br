---
title: Propriedade DefaultAction
description: A propriedade DefaultAction de um objeto descreve o método primário de manipulação do objeto do ponto de vista do usuário. A propriedade DefaultAction de um objeto deve ser um verbo ou uma frase de verbo curta.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd5aa70e0c6c633aa5b0ca3fe5c40049dbeb8cf2496c7785eea513821e1d5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325750"
---
# <a name="defaultaction-property"></a>Propriedade DefaultAction

A propriedade **DefaultAction** de um objeto descreve o método primário de manipulação do objeto do ponto de vista do usuário. A propriedade **DefaultAction** de um objeto deve ser um verbo ou uma frase de verbo curta.

A **propriedade DefaultAction** é recuperada chamando [**IAccessible::get \_ accDefaultAction.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)

Para executar a ação padrão de um objeto, os clientes chamam [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).

Nem todos os objetos têm ações padrão e alguns objetos têm uma ação padrão relacionada à sua [**propriedade Value,**](value-property.md) como nos exemplos a seguir:

-   Uma caixa de seleção selecionada tem uma ação padrão de "Desmarcar" e um valor de "Checked".
-   Uma caixa de seleção desmarcada tem uma ação padrão de "Verificar" e um valor de "Desmarcado".
-   Um botão rotulado "Imprimir" tem uma ação padrão de "Pressionar", sem valor.
-   Um controle de texto estático ou um controle de edição que mostra que "Impressora" não tem nenhuma ação padrão, mas tem um valor de "Impressora".

 

 




