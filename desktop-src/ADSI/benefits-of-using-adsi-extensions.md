---
title: Benefícios do uso de extensões ADSI
description: A maneira como os métodos de extensão são implementados depende do autor da extensão.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a680e1eefbc05dac84b3420bee23287eda2bd02325274532109544b04ff73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018139"
---
# <a name="benefits-of-using-adsi-extensions"></a>Benefícios do uso de extensões ADSI

A maneira como os métodos de extensão são implementados depende do autor da extensão. Um autor de extensão pode até mesmo implementar um método completamente fora do escopo do diretório. Por exemplo, um desenvolvedor de planos de software de backup e restauração para estender um objeto chamado **computador**. O desenvolvedor deve criar dois métodos: **BackUp** e **Restore**. Esses métodos operam remotamente no computador físico para o qual o objeto **de** computador no diretório aponta. Ao atuar como uma extensão, o componente acessa a infraestrutura ADSI e é exibido pelos clientes ADSI como parte integrante do objeto.

Os cenários a seguir descrevem situações em que criar uma extensão para ADSI seria vantajoso:

-   Crie uma extensão para integrar um componente ao objeto de diretório. Como há um objeto **de** usuário no diretório, um desenvolvedor de RH pode querer criar uma extensão ADSI que preencha outros dados no diretório quando um **usuário** é criado.
-   Crie uma extensão se um componente exigir uma pesquisa de diretório. Um componente pode exigir um diretório como ponto de partida para uma busca. Por exemplo, ao criar um novo aplicativo. Um objeto de aplicativo, **ToolApp**, pode ser publicado no diretório . Seu aplicativo pode dar suporte a notificações de status em uma coleção de servidores de email. Você decide tornar esse aplicativo uma extensão ADSI.

    Agora, um usuário pode pesquisar todas as instâncias do **ToolApp** no diretório . Para cada objeto retornado, o usuário pode emitir uma chamada para **NotifyNow().** Um aplicativo ou extensão pode obter dados de objeto mais atuais no diretório e notificar cada servidor de forma assíncrona.

-   Crie uma extensão como uma junção entre namespaces e modelos de programação. Por exemplo, um ISV inventará um novo modelo de objeto para serviços de impressão. O **objeto printQueue** já está definido no diretório . O ISV pode criar uma extensão ADSI e associá-la ao **objeto printQueue.** Os usuários ADSI podem se vincular a **um objeto printQueue** e começar a usar o modelo de objeto para o ISV. Da perspectiva do cliente ADSI, esse ponto de junção é transparente.
-   Crie uma extensão para simplificar as tarefas. Muitas tarefas no diretório podem ser realizadas pesquisando e definindo vários atributos em um objeto ou vários objetos. Ao criar uma única função para manipular vários atributos, ela simplifica o desenvolvimento para autores de aplicativos e scripts.

Para clientes ADSI, as extensões enriquecem o ambiente de programação ADSI de várias maneiras:

-   Os desenvolvedores que criam clientes ADSI não têm que aprender um novo modelo de programação. As extensões fazem parte da ADSI. Eles usariam o mesmo paradigma para pesquisa, manipulação de dados e proteção de objetos.
-   Os administradores podem gerenciar aplicativos relacionados habilitados para diretório usando extensões.
-   Os consumidores de extensão podem exibir um objeto ADSI e uma extensão como um objeto integrado.
-   Os componentes existentes podem ser integrados à ADSI, o que permite que as extensões aproveitem os investimentos existentes e criem uma sinéreia entre componentes.

As extensões ADSI foram projetadas com os seguintes objetivos:

-   Fácil de implementar. Com as tecnologias atuais da Microsoft, Microsoft Visual C++ de desenvolvimento e o Active Template Library, uma extensão pode ser criada rapidamente.
-   Os clientes visualizam um IDispatch. Da perspectiva dos autores de script e automação, os métodos de extensão e as propriedades são mesclados de forma transparente em um objeto ADSI.
-   Independente. Os autores de extensão podem estender a ADSI de forma independente sem conhecimento prévio das extensões existentes.

Considere este cenário: um desenvolvedor corporativo ou um ISV precisa desenvolver um programa de backup. Esse aplicativo de backup permite que um administrador faça backup de todos os computadores em uma unidade organizacional. Com uma extensão ADSI, o script a seguir é possível.


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



**LastBackUp** é uma propriedade e **BackUpNow** é um método que o autor da extensão fornece. O código mostra os benefícios para consumidores e provedores de extensão. O autor da extensão não precisa criar uma nova maneira de filtrar, pesquisar e acessar o diretório. O consumidor de extensão não precisa reaprender um novo paradigma de programação. Novos métodos e propriedades que o autor da extensão fornece são exibidos como parte da ADSI.

 

 




