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
# <a name="navigating-between-service-task-panes"></a><span data-ttu-id="68405-116">Navegando entre os painéis de tarefas de serviço</span><span class="sxs-lookup"><span data-stu-id="68405-116">Navigating between Service Task Panes</span></span>

<span data-ttu-id="68405-117">Para navegar entre os painéis de tarefas de serviço no Windows Media Player, use o método **NavigateTaskPaneURL** , que está disponível usando o objeto **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="68405-117">To navigate between service task panes in Windows Media Player, you use the **NavigateTaskPaneURL** method, which is available by using the **window.external** object.</span></span> <span data-ttu-id="68405-118">Ao usar esse método, você especifica valores para três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="68405-118">When you use this method, you specify values for three parameters:</span></span>

-   <span data-ttu-id="68405-119">*bstrKeyName*.</span><span class="sxs-lookup"><span data-stu-id="68405-119">*bstrKeyName*.</span></span> <span data-ttu-id="68405-120">Esse é o nome da chave da loja online.</span><span class="sxs-lookup"><span data-stu-id="68405-120">This is the key name of the online store.</span></span> <span data-ttu-id="68405-121">Ao navegar em uma loja online, use o nome da chave do repositório atual.</span><span class="sxs-lookup"><span data-stu-id="68405-121">When navigating within an online store, use the key name of the current store.</span></span>
-   <span data-ttu-id="68405-122">*bstrTaskPane*.</span><span class="sxs-lookup"><span data-stu-id="68405-122">*bstrTaskPane*.</span></span> <span data-ttu-id="68405-123">Esta cadeia de caracteres contém o nome do painel de tarefas de serviço no qual você deseja navegar.</span><span class="sxs-lookup"><span data-stu-id="68405-123">This string contains the name of the service task pane to which you want to navigate.</span></span>
-   <span data-ttu-id="68405-124">*bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="68405-124">*bstrParams*.</span></span> <span data-ttu-id="68405-125">Essa cadeia de caracteres contém os parâmetros de cadeia de caracteres de consulta que você deseja acrescentar à URL da página da web hospedada pelo painel de tarefas de serviço no qual você deseja navegar.</span><span class="sxs-lookup"><span data-stu-id="68405-125">This string contains the query string parameters you want to append to the URL for the webpage hosted by the service task pane to which you want to navigate.</span></span>

<span data-ttu-id="68405-126">A navegação é gerenciada por uma página da Web que você cria, chamada página de navegação.</span><span class="sxs-lookup"><span data-stu-id="68405-126">Navigation is managed by a webpage you create, called the navigate page.</span></span> <span data-ttu-id="68405-127">A URL para a página de navegação é especificada pelo elemento **Navigate** no documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="68405-127">The URL for the navigate page is specified by the **Navigate** element in the ServiceInfo document.</span></span> <span data-ttu-id="68405-128">Quando você chama **NavigateTaskPaneURL**, o Windows Media Player abre a página navegar, não a página da Web especificada pelos elementos **ServiceTask1**, **ServiceTask2** ou **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="68405-128">When you call **NavigateTaskPaneURL**, Windows Media Player opens the navigate page, not the webpage specified by the **ServiceTask1**, **ServiceTask2**, or **ServiceTask3** elements.</span></span> <span data-ttu-id="68405-129">É a página de navegação que recebe a cadeia de caracteres de consulta especificada por *bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="68405-129">It is the navigate page that receives the query string specified by *bstrParams*.</span></span> <span data-ttu-id="68405-130">A página de navegação deve conter as regras que determinam qual conteúdo é exibido em um painel de tarefas de serviço após a navegação.</span><span class="sxs-lookup"><span data-stu-id="68405-130">The navigate page should contain the rules that determine which content displays in a service task pane after navigation.</span></span>

<span data-ttu-id="68405-131">Por exemplo, suponha que você deseja que os usuários cliquem em um link para navegar de **ServiceTask1** para **ServiceTask2**.</span><span class="sxs-lookup"><span data-stu-id="68405-131">For example, suppose you want users to click a link to navigate from **ServiceTask1** to **ServiceTask2**.</span></span> <span data-ttu-id="68405-132">Você pode usar o seguinte HTML para criar o link:</span><span class="sxs-lookup"><span data-stu-id="68405-132">You could use the following HTML to create the link:</span></span>


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



<span data-ttu-id="68405-133">Quando o usuário clica no link de vídeo, o Windows Media Player alterna para **ServiceTask2** e abre a página de navegação, acrescentando a seguinte cadeia de caracteres de consulta à sua URL.</span><span class="sxs-lookup"><span data-stu-id="68405-133">When the user clicks the Video link, Windows Media Player switches to **ServiceTask2** and opens the navigate page, appending the following query string to its URL.</span></span>


```C++
?From=Music&To=2

```



<span data-ttu-id="68405-134">O parâmetro from identifica a página da qual o usuário clicou no link e o parâmetro to identifica o número do painel de tarefas de serviço ao qual ele deseja navegar.</span><span class="sxs-lookup"><span data-stu-id="68405-134">The From parameter identifies the page from which the user clicked the link and the To parameter identifies the number of the service task pane to which he or she wants to navigate.</span></span> <span data-ttu-id="68405-135">(Observe que não há nada de especial sobre esses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="68405-135">(Note that there is nothing special about these parameters.</span></span> <span data-ttu-id="68405-136">Você pode usar quaisquer parâmetros que desejar para qualquer finalidade escolhida.)</span><span class="sxs-lookup"><span data-stu-id="68405-136">You can use any parameters you like for any purpose you choose.)</span></span>

<span data-ttu-id="68405-137">Por exemplo, o código de exemplo a seguir mostra o elemento **Navigate** em um documento do ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="68405-137">For instance, the following example code shows the **Navigate** element in a ServiceInfo document:</span></span>


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



<span data-ttu-id="68405-138">A URL resultante, completa com a cadeia de caracteres de consulta, é mostrada no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="68405-138">The resulting URL, complete with query string, is shown in the following example:</span></span>


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



<span data-ttu-id="68405-139">O código de exemplo a seguir mostra a página de navegação:</span><span class="sxs-lookup"><span data-stu-id="68405-139">The following example code shows the navigate page:</span></span>


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



<span data-ttu-id="68405-140">O código anterior simplesmente cria uma URL e redireciona o navegador para ela.</span><span class="sxs-lookup"><span data-stu-id="68405-140">The preceding code simply creates a URL and redirects the browser to it.</span></span> <span data-ttu-id="68405-141">Primeiro, o código recupera os valores da cadeia de caracteres de consulta de URL e a própria cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="68405-141">First, the code retrieves To values from the URL query string and the query string itself.</span></span> <span data-ttu-id="68405-142">Ele usa o valor do parâmetro to para determinar qual página deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="68405-142">It uses the value of the To parameter to determine which page to display.</span></span> <span data-ttu-id="68405-143">Em seguida, ele acrescenta a cadeia de caracteres de consulta original à URL.</span><span class="sxs-lookup"><span data-stu-id="68405-143">It then appends the original query string to the URL.</span></span> <span data-ttu-id="68405-144">Por fim, ele navega pelo navegador usando uma URL semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="68405-144">Finally, it navigates the browser using a URL similar to the following:</span></span>


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



<span data-ttu-id="68405-145">Sempre que você executar a navegação dessa maneira, certifique-se de especificar [external. SelectedTaskPane](external-selectedtaskpane.md) para garantir que o botão de tarefa correto seja realçado.</span><span class="sxs-lookup"><span data-stu-id="68405-145">Whenever you perform navigation in this manner, be sure to specify [External.SelectedTaskPane](external-selectedtaskpane.md) to ensure that the correct task button is highlighted.</span></span>

-   <span data-ttu-id="68405-146">**Aviso** Tenha cuidado ao usar parâmetros de cadeia de caracteres de consulta para navegação.</span><span class="sxs-lookup"><span data-stu-id="68405-146">**Warning** Be careful how you use query string parameters for navigation.</span></span>

<span data-ttu-id="68405-147">As páginas da Web do HTMLView podem ser fornecidas por qualquer pessoa que criar uma lista de reprodução ASX.</span><span class="sxs-lookup"><span data-stu-id="68405-147">HTMLView webpages can be provided by anyone who creates an ASX playlist.</span></span> <span data-ttu-id="68405-148">Isso significa que sites mal-intencionados podem passar valores de cadeia de caracteres de consulta para sua loja online usando **NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="68405-148">This means that malicious websites can pass query string values to your online store using **NavigateTaskPaneURL**.</span></span> <span data-ttu-id="68405-149">Você deve planejar essa possibilidade para manter sua loja online segura.</span><span class="sxs-lookup"><span data-stu-id="68405-149">You must plan for this possibility to keep your online store secure.</span></span> <span data-ttu-id="68405-150">Por exemplo, se sua loja online simplesmente exibir um valor de cadeia de caracteres de consulta para o usuário, um site mal-intencionado poderá exibir texto inesperado.</span><span class="sxs-lookup"><span data-stu-id="68405-150">For example, if your online store simply displays a query string value to the user, a malicious website could display unexpected text.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68405-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68405-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68405-152">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="68405-152">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="68405-153">**Elemento Navigate**</span><span class="sxs-lookup"><span data-stu-id="68405-153">**Navigate Element**</span></span>](navigate-element.md)
</dt> <dt>

[<span data-ttu-id="68405-154">**Navegação para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="68405-154">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




