---
title: Navegando entre painéis de tarefa de serviço
description: Navegando entre painéis de tarefa de serviço
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player online, navegando
- lojas online, navegando
- tipo 2 lojas online, navegando
- Windows Media Player online, painéis de tarefas de serviço
- lojas online, painéis de tarefas de serviço
- tipo 2 lojas online, painéis de tarefas de serviço
- Windows Media Player online, painéis de tarefas
- lojas online, painéis de tarefas
- tipo 2 lojas online, painéis de tarefas
- navegando em lojas online do tipo 2
- Windows Media Player, painéis de tarefas de serviço
- Windows Media Player, painéis de tarefas
- painéis de tarefas de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f54a82f2637fe11b0a2a7703cc241c47e799999a89b56ba8ba19c079b7393de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647576"
---
# <a name="navigating-between-service-task-panes"></a>Navegando entre painéis de tarefa de serviço

Para navegar entre os painéis de tarefa de serviço Windows Media Player, use o método **NavigateTaskPaneURL,** que está disponível usando o **objeto window.external.** Ao usar esse método, você especifica valores para três parâmetros:

-   *bstrKeyName.* Esse é o nome da chave da loja online. Ao navegar em uma loja online, use o nome da chave do armazenamento atual.
-   *bstrTaskPane.* Essa cadeia de caracteres contém o nome do painel de tarefas de serviço para o qual você deseja navegar.
-   *bstrParams.* Essa cadeia de caracteres contém os parâmetros de cadeia de caracteres de consulta que você deseja anexar à URL da página da Web hospedada pelo painel de tarefas de serviço para o qual você deseja navegar.

A navegação é gerenciada por uma página da Web que você cria, chamada de página de navegação. A URL da página de navegação é especificada pelo **elemento Navigate** no documento ServiceInfo. Quando você chama **NavigateTaskPaneURL,** Windows Media Player abre a página de navegação, não a página da Web especificada pelos elementos **ServiceTask1,** **ServiceTask2** ou **ServiceTask3.** É a página de navegação que recebe a cadeia de caracteres de consulta especificada por *bstrParams.* A página de navegação deve conter as regras que determinam qual conteúdo é exibido em um painel de tarefas de serviço após a navegação.

Por exemplo, suponha que você queira que os usuários cliquem em um link para navegar de **ServiceTask1** para **ServiceTask2**. Você pode usar o seguinte HTML para criar o link:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Quando o usuário clica no link Vídeo, Windows Media Player alterna para **ServiceTask2** e abre a página de navegação, ao lado da cadeia de caracteres de consulta a seguir para sua URL.


```C++
?From=Music&To=2

```



O parâmetro From identifica a página da qual o usuário clicou no link e o parâmetro To identifica o número do painel de tarefas de serviço para o qual deseja navegar. (Observe que não há nada de especial nesses parâmetros. Você pode usar os parâmetros que quiser para qualquer finalidade escolhida.)

Por exemplo, o código de exemplo a seguir mostra **o elemento Navigate** em um documento ServiceInfo:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



A URL resultante, completa com cadeia de caracteres de consulta, é mostrada no exemplo a seguir:


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



O código de exemplo a seguir mostra a página de navegação:


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



O código anterior simplesmente cria uma URL e redireciona o navegador para ela. Primeiro, o código recupera valores para da cadeia de caracteres de consulta de URL e da própria cadeia de caracteres de consulta. Ele usa o valor do parâmetro To para determinar qual página exibir. Em seguida, ele anexa a cadeia de caracteres de consulta original à URL. Por fim, ele navega pelo navegador usando uma URL semelhante à seguinte:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Sempre que você executar a navegação dessa maneira, especifique [External.SelectedTaskPane](external-selectedtaskpane.md) para garantir que o botão de tarefa correto seja realçado.

-   **Aviso** Tenha cuidado ao usar parâmetros de cadeia de caracteres de consulta para navegação.

As páginas da Web htmlView podem ser fornecidas por qualquer pessoa que cria uma playlist ASX. Isso significa que sites mal-intencionados podem passar valores de cadeia de caracteres de consulta para seu armazenamento online usando **NavigateTaskPaneURL**. Você deve planejar essa possibilidade para manter sua loja online segura. Por exemplo, se sua loja online simplesmente exibir um valor de cadeia de caracteres de consulta para o usuário, um site mal-intencionado poderá exibir texto inesperado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web em Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento Navigate**](navigate-element.md)
</dt> <dt>

[**Navegação para lojas online do tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




