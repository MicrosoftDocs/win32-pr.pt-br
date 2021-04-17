---
title: Navegando entre os painéis de tarefas de serviço
description: Navegando entre os painéis de tarefas de serviço
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Lojas online do Windows Media Player, navegando
- lojas online, navegando
- Digite 2 lojas online, navegando
- Lojas online do Windows Media Player, painéis de tarefas de serviço
- lojas online, painéis de tarefas de serviço
- Digite 2 lojas online, painéis de tarefas de serviço
- Repositórios online do Windows Media Player, painéis de tarefas
- lojas online, painéis de tarefas
- Digite 2 lojas online, painéis de tarefas
- navegando no tipo 2 lojas online
- Windows Media Player, painéis de tarefas de serviço
- Windows Media Player, painéis de tarefas
- painéis de tarefas de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292184"
---
# <a name="navigating-between-service-task-panes"></a>Navegando entre os painéis de tarefas de serviço

Para navegar entre os painéis de tarefas de serviço no Windows Media Player, use o método **NavigateTaskPaneURL** , que está disponível usando o objeto **Window. external** . Ao usar esse método, você especifica valores para três parâmetros:

-   *bstrKeyName*. Esse é o nome da chave da loja online. Ao navegar em uma loja online, use o nome da chave do repositório atual.
-   *bstrTaskPane*. Esta cadeia de caracteres contém o nome do painel de tarefas de serviço no qual você deseja navegar.
-   *bstrParams*. Essa cadeia de caracteres contém os parâmetros de cadeia de caracteres de consulta que você deseja acrescentar à URL da página da web hospedada pelo painel de tarefas de serviço no qual você deseja navegar.

A navegação é gerenciada por uma página da Web que você cria, chamada página de navegação. A URL para a página de navegação é especificada pelo elemento **Navigate** no documento serviceInfo. Quando você chama **NavigateTaskPaneURL**, o Windows Media Player abre a página navegar, não a página da Web especificada pelos elementos **ServiceTask1**, **ServiceTask2** ou **ServiceTask3** . É a página de navegação que recebe a cadeia de caracteres de consulta especificada por *bstrParams*. A página de navegação deve conter as regras que determinam qual conteúdo é exibido em um painel de tarefas de serviço após a navegação.

Por exemplo, suponha que você deseja que os usuários cliquem em um link para navegar de **ServiceTask1** para **ServiceTask2**. Você pode usar o seguinte HTML para criar o link:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Quando o usuário clica no link de vídeo, o Windows Media Player alterna para **ServiceTask2** e abre a página de navegação, acrescentando a seguinte cadeia de caracteres de consulta à sua URL.


```C++
?From=Music&To=2

```



O parâmetro from identifica a página da qual o usuário clicou no link e o parâmetro to identifica o número do painel de tarefas de serviço ao qual ele deseja navegar. (Observe que não há nada de especial sobre esses parâmetros. Você pode usar quaisquer parâmetros que desejar para qualquer finalidade escolhida.)

Por exemplo, o código de exemplo a seguir mostra o elemento **Navigate** em um documento do ServiceInfo:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



A URL resultante, completa com a cadeia de caracteres de consulta, é mostrada no exemplo a seguir:


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



O código anterior simplesmente cria uma URL e redireciona o navegador para ela. Primeiro, o código recupera os valores da cadeia de caracteres de consulta de URL e a própria cadeia de caracteres de consulta. Ele usa o valor do parâmetro to para determinar qual página deve ser exibida. Em seguida, ele acrescenta a cadeia de caracteres de consulta original à URL. Por fim, ele navega pelo navegador usando uma URL semelhante à seguinte:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Sempre que você executar a navegação dessa maneira, certifique-se de especificar [external. SelectedTaskPane](external-selectedtaskpane.md) para garantir que o botão de tarefa correto seja realçado.

-   **Aviso** Tenha cuidado ao usar parâmetros de cadeia de caracteres de consulta para navegação.

As páginas da Web do HTMLView podem ser fornecidas por qualquer pessoa que criar uma lista de reprodução ASX. Isso significa que sites mal-intencionados podem passar valores de cadeia de caracteres de consulta para sua loja online usando **NavigateTaskPaneURL**. Você deve planejar essa possibilidade para manter sua loja online segura. Por exemplo, se sua loja online simplesmente exibir um valor de cadeia de caracteres de consulta para o usuário, um site mal-intencionado poderá exibir texto inesperado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento Navigate**](navigate-element.md)
</dt> <dt>

[**Navegação para lojas online do tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




