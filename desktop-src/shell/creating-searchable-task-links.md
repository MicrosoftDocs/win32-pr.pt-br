---
description: A partir do Windows Vista, a exibição de categoria do painel de controle fornece links de tarefas abaixo do ícone de cada item do painel de controle, como mostrado aqui.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Criando links de tarefas pesquisáveis para um item do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826893"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a><span data-ttu-id="76763-103">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="76763-103">Creating Searchable Task Links for a Control Panel Item</span></span>

<span data-ttu-id="76763-104">A partir do Windows Vista, a exibição de categoria do painel de controle fornece links de tarefas abaixo do ícone de cada item do painel de controle, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="76763-104">As of Windows Vista, the Control Panel category view provides task links beneath each Control Panel item's icon as shown here.</span></span>

![links de tarefas na página de categoria sistema e manutenção](images/controlpaneltasklinks.png)

<span data-ttu-id="76763-106">Quando um usuário digita o texto na caixa de **pesquisa** no canto superior direito da janela, os resultados da pesquisa incluem esses links de tarefas, como mostrado aqui para uma pesquisa na palavra "exibir".</span><span class="sxs-lookup"><span data-stu-id="76763-106">When a user enters text in the **Search** box in the upper right of the window, the search results include these task links as shown here for a search on the word "display".</span></span>

![links de tarefas nos resultados da pesquisa do painel de controle](images/controlpanelsearchresults.png)

<span data-ttu-id="76763-108">Este tópico aborda o seguinte:</span><span class="sxs-lookup"><span data-stu-id="76763-108">This topic discusses the following:</span></span>

-   [<span data-ttu-id="76763-109">Práticas recomendadas de link de tarefa</span><span class="sxs-lookup"><span data-stu-id="76763-109">Task Link Best Practices</span></span>](#task-link-best-practices)
-   [<span data-ttu-id="76763-110">Criando um arquivo XML de tarefa</span><span class="sxs-lookup"><span data-stu-id="76763-110">Creating a Task XML File</span></span>](#creating-a-task-xml-file)
-   [<span data-ttu-id="76763-111">Localizando links de tarefas</span><span class="sxs-lookup"><span data-stu-id="76763-111">Localizing Task Links</span></span>](#localizing-task-links)
-   [<span data-ttu-id="76763-112">Palavras-chave e pesquisa</span><span class="sxs-lookup"><span data-stu-id="76763-112">Keywords and Searching</span></span>](#keywords-and-searching)
-   [<span data-ttu-id="76763-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76763-113">Related topics</span></span>](#related-topics)

## <a name="task-link-best-practices"></a><span data-ttu-id="76763-114">Práticas recomendadas de link de tarefa</span><span class="sxs-lookup"><span data-stu-id="76763-114">Task Link Best Practices</span></span>

<span data-ttu-id="76763-115">É recomendável que você forneça links de tarefas para os itens do painel de controle como uma ajuda para os usuários que buscam funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="76763-115">It is recommended that you provide task links for your Control Panel items as an aid to users searching for functionality.</span></span> <span data-ttu-id="76763-116">Também é possível adicionar palavras-chave aos links de tarefa para que um usuário possa encontrá-los mesmo sem conhecer o título ou a terminologia de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="76763-116">It is also possible to add keywords to the task links so that a user can find them even without knowing a task's title or terminology.</span></span>

<span data-ttu-id="76763-117">Os melhores links de tarefas têm três finalidades:</span><span class="sxs-lookup"><span data-stu-id="76763-117">The best task links serve three purposes:</span></span>

1.  <span data-ttu-id="76763-118">Forneça um atalho para a funcionalidade do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="76763-118">Provide a shortcut to the functionality of the Control Panel item.</span></span>
2.  <span data-ttu-id="76763-119">Forneça palavras-chave para que os usuários possam Pesquisar usando seu próprio idioma.</span><span class="sxs-lookup"><span data-stu-id="76763-119">Provide keywords so that users can search using their own language.</span></span> <span data-ttu-id="76763-120">Um usuário pode querer digitar "compactação" porque ele ou ele sabe o termo técnico.</span><span class="sxs-lookup"><span data-stu-id="76763-120">A user may want to type "compaction" because he or she knows the technical term.</span></span> <span data-ttu-id="76763-121">Um usuário pode digitar "DB muito grande" ou "tamanho do banco de dados".</span><span class="sxs-lookup"><span data-stu-id="76763-121">A user may type "DB too big", or "database filesize".</span></span> <span data-ttu-id="76763-122">Adicionar palavras-chave adequadas à tarefa significa que os usuários podem localizar o item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="76763-122">Adding suitable keywords to the task means that users can find your Control Panel item.</span></span>
3.  <span data-ttu-id="76763-123">Forneça dicas sobre o que o item do painel de controle faz.</span><span class="sxs-lookup"><span data-stu-id="76763-123">Provide hints about what the Control Panel item does.</span></span> <span data-ttu-id="76763-124">Quando um usuário vê os links abaixo do ícone de um item do painel de controle, eles podem obter mais informações sobre o que o item do painel de controle é usado para o nome e o ícone sozinhos que podem fornecer.</span><span class="sxs-lookup"><span data-stu-id="76763-124">When a user sees the links beneath a Control Panel item's icon, they can get more information about what the Control Panel item is used for than the name and icon alone can provide.</span></span>

<span data-ttu-id="76763-125">Os links de tarefas devem ser focados no usuário final, não em tecnologia ou recurso.</span><span class="sxs-lookup"><span data-stu-id="76763-125">Task links should be end-user focused, not technology- or feature-focused.</span></span> <span data-ttu-id="76763-126">Por exemplo, "Habilitar compactação de banco de dados" seria uma palavra inadequada porque é um jargão técnico desconhecido para a maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="76763-126">For example, "Enable database compaction" would be bad wording because it is technical jargon unfamiliar to the majority of users.</span></span> <span data-ttu-id="76763-127">"Tornar meu arquivo de banco de dados menor" é melhor porque ele menciona a meta de término real do usuário em vez do mecanismo para chegar lá.</span><span class="sxs-lookup"><span data-stu-id="76763-127">"Make my database file smaller" is better because it mentions the user's actual end goal rather than the mechanism to get there.</span></span> <span data-ttu-id="76763-128">O objetivo não é simplificar, mas sim formular a tarefa em termos do que o usuário deseja realizar.</span><span class="sxs-lookup"><span data-stu-id="76763-128">The goal is not to oversimplify, but rather to phrase the task in terms of what the user wants to accomplish.</span></span>

## <a name="creating-a-task-xml-file"></a><span data-ttu-id="76763-129">Criando um arquivo XML de tarefa</span><span class="sxs-lookup"><span data-stu-id="76763-129">Creating a Task XML File</span></span>

<span data-ttu-id="76763-130">Os links de tarefas são definidos em um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="76763-130">Task links are defined in an XML file.</span></span> <span data-ttu-id="76763-131">Esta seção fornece os detalhes de um arquivo. XML de exemplo que define três links de tarefas para um item do painel de controle chamado **bloco de notas**.</span><span class="sxs-lookup"><span data-stu-id="76763-131">This section provides the details of an example .xml file that defines three task links for a Control Panel item called **Notepad**.</span></span> <span data-ttu-id="76763-132">Ele define títulos, palavras-chave e as linhas de comando para os links de tarefas.</span><span class="sxs-lookup"><span data-stu-id="76763-132">It defines titles, keywords, and the command lines for the task links.</span></span> <span data-ttu-id="76763-133">Ele também ilustra como especificar quais links de tarefa aparecem sob qual categoria.</span><span class="sxs-lookup"><span data-stu-id="76763-133">It also illustrates how to specify which task links appear under which category.</span></span> <span data-ttu-id="76763-134">Um item do painel de controle que é registrado para aparecer em mais de uma categoria tem a opção de mostrar links diferentes dependendo da categoria.</span><span class="sxs-lookup"><span data-stu-id="76763-134">A Control Panel item that is registered to appear in more than one category has the option of showing different links depending on the category.</span></span> <span data-ttu-id="76763-135">As explicações dos vários elementos e das informações fornecidas são dadas como comentários no próprio XML.</span><span class="sxs-lookup"><span data-stu-id="76763-135">Explanations of the various elements and information provided are given as comments in the XML itself.</span></span>


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> <span data-ttu-id="76763-136">A partir do Windows 7, um item do painel de controle pode ser identificado por seu nome canônico em vez de seu nome executável: o elemento **<sh: controlpanel>** pode ser usado no lugar de **<sh: Command>**.</span><span class="sxs-lookup"><span data-stu-id="76763-136">As of Windows 7, a Control Panel item can be identified by its canonical name rather than its executable name: the **<sh:controlpanel>** element can be used in place of **<sh:command>**.</span></span> <span data-ttu-id="76763-137">O elemento **<sh: controlpanel>** também fornece um atributo para especificar a página do item ao qual ele deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="76763-137">The **<sh:controlpanel>** element also provides an attribute to specify the page of the item to which it should open.</span></span> <span data-ttu-id="76763-138">Veja a seguir um exemplo do elemento **<sh: controlpanel>** :</span><span class="sxs-lookup"><span data-stu-id="76763-138">The following shows an example of the **<sh:controlpanel>** element:</span></span>

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a><span data-ttu-id="76763-139">Localizando links de tarefas</span><span class="sxs-lookup"><span data-stu-id="76763-139">Localizing Task Links</span></span>

<span data-ttu-id="76763-140">O texto dos títulos e das palavras-chave dos links de tarefas pode ser armazenado em uma tabela de cadeia de caracteres no módulo do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="76763-140">The text for the task links' titles and keywords can be stored in a string table in the Control Panel item's module.</span></span> <span data-ttu-id="76763-141">Nesse caso, o formato usado no arquivo XML se torna:</span><span class="sxs-lookup"><span data-stu-id="76763-141">In that case, the format used in the XML file becomes:</span></span>


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



<span data-ttu-id="76763-142">Neste exemplo, o texto do nome da tarefa aparece na ID do recurso de cadeia de caracteres 100 em myTextResources.dll, e o texto para as palavras-chave aparece na ID do recurso de cadeia de caracteres 101.</span><span class="sxs-lookup"><span data-stu-id="76763-142">In this example, the text for the task's name appears in string resource ID 100 in myTextResources.dll, and the text for the keywords appears in string resource ID 101.</span></span>

## <a name="keywords-and-searching"></a><span data-ttu-id="76763-143">Palavras-chave e pesquisa</span><span class="sxs-lookup"><span data-stu-id="76763-143">Keywords and Searching</span></span>

<span data-ttu-id="76763-144">A pesquisa do painel de controle localiza links de tarefas com base em seu nome e também em suas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="76763-144">The Control Panel search finds task links based on their name and also on their keywords.</span></span> <span data-ttu-id="76763-145">Ele corresponde a cada palavra na pesquisa com o prefixo de palavras no nome e palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="76763-145">It matches each word in the search with the prefix of words in the name and keywords.</span></span> <span data-ttu-id="76763-146">Por exemplo, a cadeia de caracteres de consulta "CPU" corresponderia à tarefa "ver processos em execução" no exemplo anterior porque "CPU" está na lista de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="76763-146">For example, the query string "cpu" would match the task "See running processes" in the earlier example because "cpu" is in the keyword list.</span></span> <span data-ttu-id="76763-147">A cadeia de caracteres de consulta "pro" também encontraria esse resultado porque a palavra de título "processes" começa com essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76763-147">The query string "pro" would also find that result because the title word "processes" begins with that string.</span></span> <span data-ttu-id="76763-148">Observe que a consulta só corresponde a prefixos.</span><span class="sxs-lookup"><span data-stu-id="76763-148">Note that the query only matches prefixes.</span></span> <span data-ttu-id="76763-149">A cadeia de caracteres de consulta "modelos" não corresponderia a um resultado porque essa cadeia de caracteres, enquanto parte da palavra de título "Process", não inicia essa palavra.</span><span class="sxs-lookup"><span data-stu-id="76763-149">The query string "rocess" would not match a result because that string, while part of the title word "process", does not begin that word.</span></span>

<span data-ttu-id="76763-150">Quando uma consulta de pesquisa contém vários tokens, todos os tokens devem corresponder ao prefixo de alguma palavra-chave ou parte do título da tarefa para um resultado.</span><span class="sxs-lookup"><span data-stu-id="76763-150">When a search query contains multiple tokens, all the tokens must match the prefix of some keyword or part of the task title for a result.</span></span> <span data-ttu-id="76763-151">A consulta "nível de CPU" não corresponde, pois "nível" não está na palavra-chave definida.</span><span class="sxs-lookup"><span data-stu-id="76763-151">The query "cpu level" would not match, because "level" is not in the keyword set.</span></span> <span data-ttu-id="76763-152">A consulta "execução de CPU" daria um resultado, porque "CPU" corresponde a uma palavra-chave e "Run" é o prefixo da palavra "Running" no título da tarefa.</span><span class="sxs-lookup"><span data-stu-id="76763-152">The query "cpu run" would give a result, because "cpu" matches a keyword, and "run" is the prefix of the word "running" in the task's title.</span></span>

<span data-ttu-id="76763-153">O painel de controle não fornece automaticamente a correção ortográfica ou variações como plurals ou hifenização.</span><span class="sxs-lookup"><span data-stu-id="76763-153">Control Panel does not automatically provide spelling correction or variations such as plurals or hyphenation.</span></span> <span data-ttu-id="76763-154">As correspondências também não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76763-154">Matches are also case-insensitive.</span></span> <span data-ttu-id="76763-155">Para garantir uma lista de palavras-chave bem-sucedida, é recomendável fornecer variações por conta própria, como para esse link de tarefa que envolve proteções de tela: "protetores de tela; proteções de telas; proteções de tela;"</span><span class="sxs-lookup"><span data-stu-id="76763-155">To ensure a successful keyword list, it is recommended to provide variations yourself, such as for this task link that involves screen savers: "screensavers;screen-savers;screen savers;"</span></span>

<span data-ttu-id="76763-156">Não é necessário adicionar o "protetor de tela" singular, porque uma consulta que encontra "protetores de tela" também encontrará "protetor de tela" devido à correspondência de prefixo.</span><span class="sxs-lookup"><span data-stu-id="76763-156">There is no need to add the singular "screensaver", because a query that finds "screensavers" will also find "screensaver" due to the prefix match.</span></span> <span data-ttu-id="76763-157">Um usuário digitando, até mesmo, parte da palavra, como "telas", ainda verá uma correspondência em um link de tarefa que tenha "protetores de tela" como palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="76763-157">A user typing even part of the word, like "screensa" will still see a match on a task link that has "screensavers" as a keyword.</span></span> <span data-ttu-id="76763-158">Para idiomas em que os formulários do plural alteram a palavra, é necessário colocar todos os formulários que um usuário poderia esperar para digitar nas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="76763-158">For languages where plural forms change the word, it is necessary to put all the forms a user could reasonably be expected to type into the keywords.</span></span>

<span data-ttu-id="76763-159">Como uma convenção, a Microsoft omitia palavras pequenas como "como faço para" ou "desejo" do conjunto de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="76763-159">As a convention, Microsoft has omitted small words like "how do I" or "I want to" from the set of keywords.</span></span> <span data-ttu-id="76763-160">A expectativa é que a maioria dos usuários simplesmente digite as palavras mais importantes, como "mouse", "alto contraste" ou "driver de vídeo", para obter resultados.</span><span class="sxs-lookup"><span data-stu-id="76763-160">The expectation is that most users will simply type the most important words such as "mouse", "high contrast", or "video driver" to get results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76763-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76763-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76763-162">Itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="76763-162">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="76763-163">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="76763-163">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="76763-164">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="76763-164">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="76763-165">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="76763-165">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="76763-166">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="76763-166">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="76763-167">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="76763-167">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="76763-168">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="76763-168">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="76763-169">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="76763-169">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="76763-170">Acessando o painel de controle no modo de segurança no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76763-170">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



