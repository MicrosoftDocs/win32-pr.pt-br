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
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a>Criando links de tarefas pesquisáveis para um item do painel de controle

A partir do Windows Vista, a exibição de categoria do painel de controle fornece links de tarefas abaixo do ícone de cada item do painel de controle, como mostrado aqui.

![links de tarefas na página de categoria sistema e manutenção](images/controlpaneltasklinks.png)

Quando um usuário digita o texto na caixa de **pesquisa** no canto superior direito da janela, os resultados da pesquisa incluem esses links de tarefas, como mostrado aqui para uma pesquisa na palavra "exibir".

![links de tarefas nos resultados da pesquisa do painel de controle](images/controlpanelsearchresults.png)

Este tópico aborda o seguinte:

-   [Práticas recomendadas de link de tarefa](#task-link-best-practices)
-   [Criando um arquivo XML de tarefa](#creating-a-task-xml-file)
-   [Localizando links de tarefas](#localizing-task-links)
-   [Palavras-chave e pesquisa](#keywords-and-searching)
-   [Tópicos relacionados](#related-topics)

## <a name="task-link-best-practices"></a>Práticas recomendadas de link de tarefa

É recomendável que você forneça links de tarefas para os itens do painel de controle como uma ajuda para os usuários que buscam funcionalidade. Também é possível adicionar palavras-chave aos links de tarefa para que um usuário possa encontrá-los mesmo sem conhecer o título ou a terminologia de uma tarefa.

Os melhores links de tarefas têm três finalidades:

1.  Forneça um atalho para a funcionalidade do item do painel de controle.
2.  Forneça palavras-chave para que os usuários possam Pesquisar usando seu próprio idioma. Um usuário pode querer digitar "compactação" porque ele ou ele sabe o termo técnico. Um usuário pode digitar "DB muito grande" ou "tamanho do banco de dados". Adicionar palavras-chave adequadas à tarefa significa que os usuários podem localizar o item do painel de controle.
3.  Forneça dicas sobre o que o item do painel de controle faz. Quando um usuário vê os links abaixo do ícone de um item do painel de controle, eles podem obter mais informações sobre o que o item do painel de controle é usado para o nome e o ícone sozinhos que podem fornecer.

Os links de tarefas devem ser focados no usuário final, não em tecnologia ou recurso. Por exemplo, "Habilitar compactação de banco de dados" seria uma palavra inadequada porque é um jargão técnico desconhecido para a maioria dos usuários. "Tornar meu arquivo de banco de dados menor" é melhor porque ele menciona a meta de término real do usuário em vez do mecanismo para chegar lá. O objetivo não é simplificar, mas sim formular a tarefa em termos do que o usuário deseja realizar.

## <a name="creating-a-task-xml-file"></a>Criando um arquivo XML de tarefa

Os links de tarefas são definidos em um arquivo XML. Esta seção fornece os detalhes de um arquivo. XML de exemplo que define três links de tarefas para um item do painel de controle chamado **bloco de notas**. Ele define títulos, palavras-chave e as linhas de comando para os links de tarefas. Ele também ilustra como especificar quais links de tarefa aparecem sob qual categoria. Um item do painel de controle que é registrado para aparecer em mais de uma categoria tem a opção de mostrar links diferentes dependendo da categoria. As explicações dos vários elementos e das informações fornecidas são dadas como comentários no próprio XML.


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
> A partir do Windows 7, um item do painel de controle pode ser identificado por seu nome canônico em vez de seu nome executável: o elemento **<sh: controlpanel>** pode ser usado no lugar de **<sh: Command>**. O elemento **<sh: controlpanel>** também fornece um atributo para especificar a página do item ao qual ele deve ser aberto. Veja a seguir um exemplo do elemento **<sh: controlpanel>** :

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a>Localizando links de tarefas

O texto dos títulos e das palavras-chave dos links de tarefas pode ser armazenado em uma tabela de cadeia de caracteres no módulo do item do painel de controle. Nesse caso, o formato usado no arquivo XML se torna:


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



Neste exemplo, o texto do nome da tarefa aparece na ID do recurso de cadeia de caracteres 100 em myTextResources.dll, e o texto para as palavras-chave aparece na ID do recurso de cadeia de caracteres 101.

## <a name="keywords-and-searching"></a>Palavras-chave e pesquisa

A pesquisa do painel de controle localiza links de tarefas com base em seu nome e também em suas palavras-chave. Ele corresponde a cada palavra na pesquisa com o prefixo de palavras no nome e palavras-chave. Por exemplo, a cadeia de caracteres de consulta "CPU" corresponderia à tarefa "ver processos em execução" no exemplo anterior porque "CPU" está na lista de palavras-chave. A cadeia de caracteres de consulta "pro" também encontraria esse resultado porque a palavra de título "processes" começa com essa cadeia de caracteres. Observe que a consulta só corresponde a prefixos. A cadeia de caracteres de consulta "modelos" não corresponderia a um resultado porque essa cadeia de caracteres, enquanto parte da palavra de título "Process", não inicia essa palavra.

Quando uma consulta de pesquisa contém vários tokens, todos os tokens devem corresponder ao prefixo de alguma palavra-chave ou parte do título da tarefa para um resultado. A consulta "nível de CPU" não corresponde, pois "nível" não está na palavra-chave definida. A consulta "execução de CPU" daria um resultado, porque "CPU" corresponde a uma palavra-chave e "Run" é o prefixo da palavra "Running" no título da tarefa.

O painel de controle não fornece automaticamente a correção ortográfica ou variações como plurals ou hifenização. As correspondências também não diferenciam maiúsculas de minúsculas. Para garantir uma lista de palavras-chave bem-sucedida, é recomendável fornecer variações por conta própria, como para esse link de tarefa que envolve proteções de tela: "protetores de tela; proteções de telas; proteções de tela;"

Não é necessário adicionar o "protetor de tela" singular, porque uma consulta que encontra "protetores de tela" também encontrará "protetor de tela" devido à correspondência de prefixo. Um usuário digitando, até mesmo, parte da palavra, como "telas", ainda verá uma correspondência em um link de tarefa que tenha "protetores de tela" como palavra-chave. Para idiomas em que os formulários do plural alteram a palavra, é necessário colocar todos os formulários que um usuário poderia esperar para digitar nas palavras-chave.

Como uma convenção, a Microsoft omitia palavras pequenas como "como faço para" ou "desejo" do conjunto de palavras-chave. A expectativa é que a maioria dos usuários simplesmente digite as palavras mais importantes, como "mouse", "alto contraste" ou "driver de vídeo", para obter resultados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Itens do painel de controle](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
</dt> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Processamento de mensagens do painel de controle](message-processing.md)
</dt> <dt>

[Executando itens do painel de controle](executing-control-panel-items.md)
</dt> <dt>

[Estendendo itens do painel de controle do sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Acessando o painel de controle no modo de segurança no Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



