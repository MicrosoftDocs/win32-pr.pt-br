---
title: Criando manipuladores de pesquisa
description: O Shell dá suporte a vários utilitários de pesquisa que permitem aos usuários localizar objetos de namespace, como arquivos ou impressoras. Você pode criar um mecanismo de pesquisa personalizado e torná-lo disponível para os usuários implementando e registrando um manipulador de pesquisa.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- manipuladores de pesquisa
- registrar, manipuladores de pesquisa
- manipuladores de pesquisa estáticos
- registrar, manipuladores de pesquisa estáticos
- manipuladores de pesquisa dinâmica
- registrar, manipuladores de pesquisa dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be891247c36687b0305e7e9c60711a233fb9b1d4f7f8554d0103be4cc0dc5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975766"
---
# <a name="creating-search-handlers"></a>Criando manipuladores de pesquisa

\[esse recurso tem suporte apenas no Windows XP ou anterior. em vez disso, Use Windows Search.\]

O Shell dá suporte a vários utilitários de pesquisa que permitem aos usuários localizar objetos de namespace, como arquivos ou impressoras. Você pode criar um mecanismo de pesquisa personalizado e torná-lo disponível para os usuários implementando e registrando um *manipulador de pesquisa*.

Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](/windows/desktop/shell/handlers). Este documento se concentra nesses aspectos da implementação que são específicos para os manipuladores de pesquisa.

-   [Como funcionam os manipuladores de pesquisa](#how-search-handlers-work)
-   [Registrando manipuladores de pesquisa](#registering-search-handlers)
    -   [Registrando um manipulador de pesquisa estático](#registering-a-static-search-handler)
    -   [Registrando um manipulador de pesquisa dinâmica](#registering-a-dynamic-search-handler)
-   [Implementando manipuladores de pesquisa](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Como funcionam os manipuladores de pesquisa

Os usuários têm duas maneiras de selecionar um mecanismo de pesquisa. a primeira maneira é a partir da menu Iniciar. com sistemas anteriores a Windows 2000, selecionar o comando **localizar** no menu **iniciar** exibe um submenu dos mecanismos de pesquisa disponíveis. com o Windows 2000 e posterior, o comando **Find** do menu de arte **St** é renomeado como Search. a ilustração a seguir mostra o botão de **pesquisa** em um sistema Windows XP.

![o submenu Pesquisar do menu iniciar](images/searchhandler1.jpg)

os usuários também podem iniciar uma pesquisa do Windows Explorer. em sistemas anteriores a Windows 2000, eles clicam no comando **localizar** no menu **ferramentas** para exibir, essencialmente, o mesmo menu como aquele associado ao menu **iniciar** . no entanto, Windows Explorer para Windows 2000 trata os mecanismos de pesquisa de forma muito diferente. Em vez de manipular mecanismos de pesquisa como um submenu do menu **ferramentas** , agora há um botão **Pesquisar** na barra de ferramentas. Clicar nesse botão abre o painel de **pesquisa** da barra do Explorer. A ilustração a seguir mostra o painel pesquisa **de arquivos e pastas** .

![painel de pesquisa da barra do Windows Explorer](images/searchhandler2.jpg)

há várias diferenças em como Windows 2000 e sistemas anteriores gerenciam manipuladores de pesquisa que afetam a implementação e o registro.



| pré-Windows 2000                                                                                                                                                                                                       | Windows 2000 e posterior                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Os manipuladores de pesquisa são implementados como um tipo de [manipulador de menu de atalho](/windows/desktop/shell/context-menu-handlers).                                                                                                                     | Os manipuladores de pesquisa podem ser implementados como manipuladores de menu de atalho ou como documentos HTML dinâmico (DHTML).                                                                                                                                                                                                               |
| Os manipuladores de pesquisa podem ser estáticos ou dinâmicos. Manipuladores estáticos são carregados somente quando são selecionados pelo usuário. Os manipuladores dinâmicos são carregados pelo shell na inicialização e não são encerrados até que o Shell saia. | Os manipuladores implementados como manipuladores de menu de atalho podem ser estáticos ou dinâmicos. Os manipuladores implementados como documentos DHTML devem ser estáticos.                                                                                                                                                                           |
| os manipuladores de pesquisa são exibidos no submenu **localizar** do menu **iniciar** e no submenu **localizar** do menu **ferramentas** do Windows Explorer.                                                                                  | Os manipuladores de pesquisa aparecem apenas no submenu **Pesquisar** do menu **Iniciar** . para disponibilizar um painel de pesquisa personalizado por meio da barra de menus do Windows Explorer, você deve implementá-lo como um [objeto de faixa](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)). em seguida, ele é listado no submenu **barra do explorer** do menu **exibir** do Windows Explorer. |



 

## <a name="registering-search-handlers"></a>Registrando manipuladores de pesquisa

Os manipuladores de pesquisa são registrados na subchave **FindExtensions** dos tipos de arquivo.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

A partir desse ponto, o procedimento de registro depende se o manipulador deve ser estático ou dinâmico. Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](/windows/desktop/shell/handlers).

### <a name="registering-a-static-search-handler"></a>Registrando um manipulador de pesquisa estático

Os manipuladores de pesquisa estáticos são carregados somente quando são iniciados pelo usuário. Essa abordagem funciona melhor para DLLs que são pequenas e podem ser carregadas rapidamente. Se você estiver usando o DHTML para implementar seu manipulador, ele deverá ser estático. Para registrar um manipulador de extensão estático, crie uma subchave chamada para o manipulador sob a subchave **estática** da subchave **FindExtensions** . O nome não é usado pelo sistema, mas não deve ser idêntico a outros nomes de manipuladores de pesquisa na subchave **FindExtensions** .

### <a name="shortcut-menu-based-search-handlers"></a>Manipuladores de pesquisa baseados em menu de atalho

Se o manipulador for implementado como um [manipulador de menu de atalho](/windows/desktop/shell/context-menu-handlers), defina o valor padrão da subchave Name do manipulador para o GUID do identificador de classe (CLSID) do objeto. Na subchave Name do manipulador, crie uma subchave chamada **0** (zero) e defina seu valor padrão como a cadeia de caracteres que será exibida no submenu **Pesquisar** ou **Localizar** . Você pode habilitar atalhos de teclado da maneira usual, precedendo o caractere de atalho com um e comercial (&). Você pode ter um ícone pequeno opcional exibido à direita do texto do menu criando uma subchave **DefaultIcon** na subchave **0** . Defina seu valor padrão como uma cadeia de caracteres que contém o caminho do arquivo que contém o ícone, seguido por uma vírgula, seguido pelo índice de base zero do ícone.

O exemplo a seguir registra o manipulador de pesquisa **MySearchEngine** . O texto do menu é "meu mecanismo de pesquisa", com M especificado como a tecla de atalho. O ícone está em C: \\ MyDir \\MySearch.dll, com um índice de 2.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {MySearchEngine CLSID GUID}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
```

### <a name="dhtml-based-search-handlers"></a>Manipuladores de pesquisa baseados em DHTML

com o Windows 2000, você também pode implementar um manipulador de pesquisa como um documento DHTML. Seu nome está listado no submenu **Pesquisar** do menu **Iniciar** . quando o usuário o seleciona, ele inicia o Windows Explorer com a barra do explorer aberta no documento de pesquisa. Você também pode especificar um documento DHTML a ser exibido à direita da barra do Explorer. Não é possível iniciar um manipulador diferente no painel de pesquisa padrão. os mecanismos de pesquisa podem ser iniciados diretamente do Windows Explorer, mas somente se forem implementados como [objetos de faixa](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)).

Para registrar um manipulador de pesquisa baseado em DHTML, defina a subchave Name do manipulador como a forma de cadeia de caracteres de CLSID \_ ShellSearchExt (atualmente, {169A0691-8DF9-11D1-A1C4-00C04FD75D13}) e crie as seguintes subchaves.

1.  Crie uma subchave **0**(zero) na subchave de nome do manipulador e defina seu valor padrão como o texto do menu.
2.  Para que um ícone seja exibido ao lado do texto do menu, crie uma subchave **DefaultIcon** em **0** e defina seu valor padrão como o caminho e o índice do ícone.
3.  Crie uma subchave **SearchGUID** em **0**. Atribua um GUID ao documento DHTML e defina o valor padrão de **SearchGUID** para seu formulário de cadeia de caracteres. Este GUID não precisa ser registrado em **HKEY \_ classes \_ raiz \\ CLSID**.
4.  Crie uma subchave de **URL** em **SearchGUID**. Defina seu valor padrão como o caminho do documento HTML que aparecerá na barra do Explorer.
5.  Crie uma subchave **UrlNavNew** em **SearchGUID**. Defina seu valor padrão como o caminho do documento HTML que será exibido à direita da barra do Explorer.

O exemplo a seguir registra o manipulador de pesquisa **MySearchEngine** implementado como um documento DHTML. O texto do menu é "meu mecanismo de pesquisa", com M especificado como a tecla de atalho. O ícone está em C: \\ MyDir \\MySearch.dll, com um índice de 2. O documento DHTML da barra do Explorer é C: \\ MyDir \\MySearch.htm e o documento que será exibido à direita da barra do Explorer é c: \\ mydir \\MySearchPage.htm.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {169A0691-8DF9-11d1-A1C4-00C04FD75D13}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
                                 SearchGUID
                                    (Default) = {My Search GUID}
                                    Url
                                       (Default) = C:\MyDir\MySearch.htm
                                    UrlNavNew
                                       (Default) = C:\MyDir\MySearchPage.htm
```

### <a name="registering-a-dynamic-search-handler"></a>Registrando um manipulador de pesquisa dinâmica

Se o manipulador for implementado como um [manipulador de menu de atalho](/windows/desktop/shell/context-menu-handlers), você também poderá registrá-lo como um manipulador dinâmico. Nesse caso, ele será carregado com o Shell e será encerrado somente quando o Shell for encerrado. Os manipuladores de pesquisa dinâmica respondem muito mais rapidamente do que os manipuladores estáticos quando são iniciados pelo usuário. Essa abordagem funciona melhor se a DLL do manipulador pode demorar muito tempo para ser carregada ou se for provável que seja chamada com frequência.

Os manipuladores de pesquisa dinâmica são registrados na subchave **FindExtensions** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Crie uma subchave de **FindExtensions** chamada para o manipulador e defina seu valor padrão para o GUID CLSID do manipulador. Os ícones de menu não têm suporte para manipuladores de pesquisa dinâmica. O exemplo a seguir registra MySearchEngine como um manipulador de pesquisa dinâmica.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     MySearchEngine
                        (Default) = {MySearchEngine CLSID GUID}
                        0
                           (Default) = &My Search Engine
```

Ao contrário dos manipuladores de pesquisa estáticos, você não especifica o texto do menu no registro. Quando o manipulador for carregado, o Shell chamará o método [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) do manipulador para adicionar itens ao submenu **Localizar** ou **Pesquisar** .

## <a name="implementing-search-handlers"></a>Implementando manipuladores de pesquisa

Manipuladores de pesquisa podem ser implementados como manipuladores de menu de atalho para todas as versões do Windows. Por Windows 2000, eles também podem ser implementados como documentos DHTML.

Para uma discussão geral sobre como implementar manipuladores de menu de atalho, consulte [Criando manipuladores de menu de contexto.](/windows/desktop/shell/context-menu-handlers) Os manipuladores de pesquisa diferem dos manipuladores de menu de atalho padrão de apenas algumas maneiras.

Para manipuladores de menu estático, o **submenu** **Encontrar** ou Pesquisar é criado com base nas informações no Registro. Não é necessário fazer com que o manipulador adicione um item de menu, como faria um manipulador de menu de atalho normal. O Shell gerencia manipuladores de menu estático da seguinte maneira.

-   Quando o usuário inicia o item de menu do manipulador, o Shell carrega a DLL do manipulador e chama [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para notificar o manipulador para iniciar o mecanismo de pesquisa. Os [**métodos IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) e [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) não são chamados.
-   Quando [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é chamado, o membro **lpVerb** da estrutura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) que é passada identifica o comando. A palavra de ordem baixa **de lpVerb** é definida como o equivalente numérico do nome da sub-chave do comando. Como essa sub-chave normalmente é **nomeada como 0,** **lpVerb** geralmente é definido como zero. Em seguida, o manipulador deve iniciar o mecanismo de pesquisa.

Os manipuladores de pesquisa dinâmica são implementados da mesma maneira que os manipuladores de menu de atalho normais. A principal exceção é que, quando [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) é chamado, os argumentos *pidlFolder* e *lpdobj* são definidos como **NULL.**

Manipuladores de pesquisa baseados em DHTML são implementados como um documento DHTML normal. Eles podem incluir qualquer tecnologia HTML, DHTML ou de script com suporte da Windows Internet Explorer.

 

 