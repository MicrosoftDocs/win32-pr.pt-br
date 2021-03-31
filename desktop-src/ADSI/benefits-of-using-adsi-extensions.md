---
title: Benefícios do uso de extensões ADSI
description: A maneira como os métodos de extensão são implementados depende do gravador de extensão.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004879"
---
# <a name="benefits-of-using-adsi-extensions"></a>Benefícios do uso de extensões ADSI

A maneira como os métodos de extensão são implementados depende do gravador de extensão. Um gravador de extensão pode até mesmo implementar um método completamente fora do escopo do diretório. Por exemplo, um desenvolvedor de backup e restauração de planos de software para estender um objeto chamado **computador**. O desenvolvedor deve criar dois métodos: **backup** e **restauração**. Esses métodos operam remotamente no computador físico no qual o objeto de **computador** no diretório aponta. Agindo como uma extensão, o componente acessa a infraestrutura de ADSI e é exibido por clientes ADSI como parte integrante do objeto.

Os cenários a seguir descrevem situações em que a criação de uma extensão para ADSI seria vantajosa:

-   Crie uma extensão para integrar um componente ao objeto de diretório. Como há um objeto de **usuário** no diretório, um desenvolvedor de RH pode querer criar uma extensão ADSI que popula outros dados no diretório quando um **usuário** é criado.
-   Crie uma extensão se um componente exigir uma pesquisa de diretório. Um componente pode exigir um diretório como um ponto de partida para uma pesquisa. Por exemplo, ao criar um novo aplicativo. Um objeto de aplicativo, **ToolApp**, pode ser publicado no diretório. Seu aplicativo pode dar suporte a notificações de status em uma coleção de servidores de email. Você decide tornar este aplicativo uma extensão ADSI.

    Agora, um usuário pode pesquisar todas as instâncias de **ToolApp** no diretório. Para cada objeto retornado, o usuário pode emitir uma chamada para **NotifyNow ()**. Um aplicativo ou extensão pode obter mais dados de objeto atual no diretório e notificar cada servidor de forma assíncrona.

-   Crie uma extensão como uma junção entre namespaces e modelos de programação. Por exemplo, um ISV inventa um novo modelo de objeto para serviços de impressão. O objeto **PrintQueue** já está definido no diretório. O ISV pode criar uma extensão ADSI e associá-la ao objeto **PrintQueue** . Os usuários ADSI podem se associar a um objeto **PrintQueue** e começar a usar o modelo de objeto para o ISV. Da perspectiva do cliente ADSI, esse ponto de junção é transparente.
-   Crie uma extensão para simplificar as tarefas. Muitas tarefas no diretório podem ser realizadas pesquisando e configurando vários atributos em um objeto ou vários objetos. Ao criar uma única função para manipular vários atributos, ele simplifica o desenvolvimento de gravadores de aplicativos e scripts.

Para clientes ADSI, as extensões enriquecem o ambiente de programação ADSI de várias maneiras:

-   Os desenvolvedores que criam clientes ADSI não precisam aprender um novo modelo de programação. As extensões fazem parte do ADSI. Eles usariam o mesmo paradigma para pesquisa, manipulação de dados e objetos de proteção.
-   Os administradores podem gerenciar aplicativos habilitados para diretório relacionados usando extensões.
-   Os consumidores de extensão podem exibir um objeto e uma extensão ADSI como um objeto integrado.
-   Os componentes existentes podem ser integrados ao ADSI, o que permite que as extensões aproveitem os investimentos existentes e criem sinergias entre os componentes.

Extensões ADSI foram projetadas com os seguintes objetivos:

-   Fácil de implementar. Com as tecnologias atuais da Microsoft existentes, Microsoft Visual C++ sistema de desenvolvimento e o Active Template Library, uma extensão pode ser criada rapidamente.
-   Os clientes exibem um IDispatch. Da perspectiva dos gravadores de script e automação, os métodos e as propriedades de extensão são mesclados de forma transparente em um objeto ADSI.
-   Depende. Os gravadores de extensão podem estender de forma independente o ADSI sem conhecimento prévio das extensões existentes.

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



**LastBackUp** é uma propriedade e **BackUpNow** é um método fornecido pelo gravador de extensão. O código mostra os benefícios para os consumidores de extensão e provedores. O gravador de extensão não precisa criar uma nova maneira de filtrar, Pesquisar e acessar o diretório. O consumidor de extensão não precisa aprender um novo paradigma de programação. Novos métodos e propriedades que o gravador de extensão fornece são exibidos como parte do ADSI.

 

 




