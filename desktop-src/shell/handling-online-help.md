---
description: A ajuda online pode surgir em uma variedade de formas, desde informações conceituais detalhadas até definições rápidas. Este tópico inclui as seções a seguir.
title: Manipulando a ajuda online
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: caf576d723b27e1c81bb715ea04743740930b5bb257f03eb3ca0a9ab697affd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223678"
---
# <a name="handling-online-help"></a>Manipulando a ajuda online

A ajuda online pode surgir em uma variedade de formas, desde informações conceituais detalhadas até definições rápidas. Este tópico inclui as seções a seguir.

-   [Sobre a ajuda](#about-help)
    -   [Solicitações de ajuda](#help-requests)
    -   [ajuda para exibir e Windows de ajuda](#help-display-and-windows-help)
-   [Usando a ajuda](#using-help)
    -   [Fornecendo ajuda em uma caixa de diálogo](#providing-help-in-a-dialog-box)
    -   [Definindo a aparência de uma janela de ajuda secundária](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>Sobre a ajuda

Um elemento importante de um aplicativo amigável está prontamente disponível na ajuda online. Windows fornece funções e mensagens que, quando usadas em conjunto com o aplicativo de ajuda do Windows, facilitam a implementação da ajuda online em seu aplicativo. esta visão geral discute os elementos de Windows que dão suporte à ajuda online. ele descreve como usar esses elementos para fornecer aos usuários um meio de solicitar ajuda e explica como usar o Windows aplicativo de ajuda para exibir a ajuda.

### <a name="help-requests"></a>Solicitações de ajuda

a maioria dos aplicativos baseados em Windows fornece informações de ajuda online em uma variedade de formulários, variando da ajuda conceitual que explica a finalidade dos recursos de um aplicativo até a ajuda pop-up que fornece definições rápidas de elementos individuais na interface do usuário do aplicativo. Você usa funções e mensagens para fornecer aos usuários várias maneiras de solicitar acesso a essas informações. As seções a seguir descrevem essas solicitações de ajuda.

### <a name="help-menu"></a>Menu Ajuda

A maioria dos aplicativos fornece acesso de usuário às informações de ajuda, incluindo um menu **ajuda** na janela principal. Quando o usuário seleciona um item em um menu **ajuda** , o procedimento de janela correspondente recebe uma mensagem de [**\_ comando do WM**](../menurc/wm-command.md) que identifica o item selecionado. O aplicativo responde exibindo as informações de ajuda apropriadas, como uma lista de tópicos de ajuda, um índice ou uma introdução ao aplicativo.

### <a name="help-from-the-keyboard"></a>Ajuda do teclado

Windows fornece acesso de usuário para informações de ajuda do teclado notificando o aplicativo sempre que o usuário pressionar a tecla F1. O sistema envia uma mensagem de [**\_ ajuda do WM**](wm-help.md) para a janela que tinha o foco do teclado quando o usuário pressionou a tecla. Se a janela for uma janela filho (por exemplo, um controle em uma caixa de diálogo), a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passará a mensagem para a janela pai. Se um menu estiver ativo quando F1 for pressionado, o sistema enviará a mensagem para a janela associada ao menu. O aplicativo responde exibindo informações de ajuda associadas à janela, ao controle ou ao menu que tem o foco ou está ativo. Por exemplo, se o usuário selecionar um controle em uma caixa de diálogo e pressionar F1, o aplicativo exibirá informações de ajuda para esse controle.

O parâmetro *lParam* da [**\_ ajuda do WM**](wm-help.md) é um ponteiro para uma estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contém informações detalhadas sobre o item para o qual a ajuda é solicitada. Você usa essas informações para determinar o tópico da ajuda a ser exibido. A estrutura **HELPINFO** também inclui as coordenadas do cursor do mouse no momento em que o usuário pressionou a tecla. Você pode usar essas informações para fornecer ajuda com base no local do cursor do mouse.

### <a name="help-from-the-mouse"></a>Ajuda do mouse

o Windows fornece ao usuário acesso às informações de ajuda do mouse notificando o aplicativo sempre que o usuário clica no botão direito do mouse ou clica em uma janela, controle ou menu depois de clicar no botão de pergunta (?). O aplicativo responde exibindo informações de ajuda associadas a uma determinada janela, controle ou menu.

O sistema envia uma mensagem de [**\_ CONTEXTMENU do WM**](../menurc/wm-contextmenu.md) quando o usuário clica com o botão direito do mouse. A janela que foi clicada recebe a mensagem. Se a janela for uma janela filho, como um controle, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passará a mensagem para a janela pai. A mensagem de **\_ CONTEXTMENU do WM** especifica as coordenadas do cursor do mouse. A coordenada x está na palavra de ordem inferior do parâmetro *lParam* e a coordenada y está na palavra de ordem superior. Se o usuário clicou em um controle, o parâmetro *wParam* é o identificador para o controle que recebeu o clique.

O sistema envia uma mensagem de [**\_ ajuda do WM**](wm-help.md) quando o usuário clica em um item em uma janela depois de clicar no botão pergunta (?) que aparece na barra de título da janela. Você pode adicionar um botão de pergunta a uma barra de título especificando o estilo **WS \_ ex \_ CONTEXTHELP** na função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ao criar a janela. O parâmetro *lParam* da **\_ ajuda do WM** é um ponteiro para uma estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contém informações detalhadas sobre o item para o qual a ajuda é solicitada, incluindo as coordenadas do cursor do mouse no momento em que o usuário clicou no botão do mouse.

O botão de pergunta é recomendado para uso somente em caixas de diálogo. No passado, os aplicativos forneceram acesso de usuário para ajudar a obter informações sobre uma caixa de diálogo, fornecendo um botão **ajuda** na caixa de diálogo. Esse método não é mais recomendado. Em vez disso, use o botão de pergunta.

### <a name="help-display-and-windows-help"></a>ajuda para exibir e Windows de ajuda

Quando um aplicativo recebe uma solicitação de ajuda, ele deve exibir as informações de ajuda apropriadas. como o aplicativo de ajuda Windows fornece uma interface de usuário consistente, é recomendável que os aplicativos usem Windows ajuda em vez de outros métodos. para direcionar Windows ajuda para exibir informações de ajuda, um aplicativo usa a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , especificando detalhes como as informações a serem exibidas e a forma da janela na qual exibi-la. As seções a seguir explicam como usar o **WinHelp** para exibir informações de ajuda.

### <a name="help-files"></a>Arquivos da Ajuda

Para exibir informações de ajuda, você deve especificar um arquivo de ajuda ao chamar a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) . o arquivo de ajuda deve ter o formato de arquivo de ajuda do Windows (. hlp) e um ou mais tópicos. Cada tópico é uma unidade distinta de informações, como uma descrição conceitual, um conjunto de instruções, uma imagem, uma definição de glossário e assim por diante. os tópicos devem ser identificados exclusivamente para que Windows ajuda possa localizá-los sempre que forem solicitados. internamente, Windows ajuda usa identificadores de tópico para localizar tópicos, mas os aplicativos geralmente usam identificadores de contexto (valores inteiros exclusivos) para especificar os tópicos a serem exibidos. O autor do arquivo de ajuda deve mapear explicitamente identificadores de contexto para identificadores de tópico na \[ \] seção de mapa do arquivo de projeto usado para criar o arquivo de ajuda.

Quando você especifica um arquivo de ajuda, mas não especifica um caminho, o [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) procura o arquivo de ajuda no diretório de ajuda ou em um diretório especificado pela variável de ambiente Path. Além disso, o **WinHelp** pode encontrar um arquivo de ajuda cujo nome está listado no seguinte local do registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Para aproveitar o registro, você deve criar um nome de valor que tenha o mesmo nome do seu arquivo de ajuda. O valor atribuído a esse nome deve ser o diretório no qual o arquivo de ajuda reside.

Se o [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) não conseguir localizar o arquivo de ajuda fornecido, ele exibirá uma caixa de diálogo que permite ao usuário especificar o local do arquivo de ajuda. Como o **WinHelp** salva as informações de local no registro, ele não pergunta novamente o local do mesmo arquivo de ajuda.

Para obter mais informações sobre como criar e criar um arquivo de ajuda, consulte a documentação fornecida com suas ferramentas de desenvolvimento.

### <a name="starting-windows-help"></a>iniciando Windows ajuda

o exemplo a seguir usa a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para iniciar o Windows aplicativo de ajuda e abrir o arquivo de ajuda para seu tópico de conteúdo.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



Este próximo exemplo abre o arquivo de ajuda do usuário, pesquisa o arquivo para o tópico associado a uma cadeia de caracteres de palavra-chave e, em seguida, exibe o tópico.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Caixa de diálogo tópicos da ajuda

Você pode exibir a caixa de diálogo **Tópicos da ajuda** chamando a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) com o comando **Help \_ Finder** . A caixa de diálogo **Tópicos da ajuda** permite que o usuário selecione os tópicos a serem exibidos exibindo os títulos dos tópicos, as palavras-chave associadas aos tópicos ou as palavras e frases encontradas nos tópicos. Normalmente, os aplicativos exibem essa caixa de diálogo quando o usuário escolhe um comando, como tópicos da ajuda, no menu ajuda. Um aplicativo também poderá exibir essa caixa de diálogo se o usuário pressionar a tecla quando nenhuma janela, controle ou menu específico no aplicativo tiver o foco ou estiver ativo.

No passado, os aplicativos usaram o **\_ conteúdo da ajuda** e os comandos de **\_ índice da ajuda** com a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para exibir o tópico conteúdo e o índice de palavra-chave do arquivo de ajuda. Esses comandos não são mais recomendados. Em vez disso, use o comando **Help \_ Finder** .

### <a name="information-topics"></a>Tópicos de informações

Você pode exibir um tópico específico chamando a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) com o comando de \_ contexto Help e especificando o identificador de contexto para o tópico. Normalmente, os aplicativos usam o \_ comando de contexto Help em resposta às solicitações do usuário para tópicos que contêm informações conceituais ou ajuda de procedimento em vez de informações sobre um controle ou menu específico. Nesses casos, o usuário pode continuar navegando pelo arquivo de ajuda procurando informações relacionadas antes de retornar ao aplicativo.

o comando de contexto da ajuda \_ invoca uma instância regular do Windows ajuda, permitindo que o usuário encontre outros tópicos no arquivo de ajuda. Normalmente, ele exibe a janela principal da ajuda, que inclui uma barra de título, um menu do sistema, os botões minimizar e maximizar, um menu principal, uma barra de navegação opcional, uma borda de dimensionamento e uma área do cliente. O texto do tópico selecionado aparece na área do cliente e o usuário pode navegar pelo arquivo de ajuda usando links quentes ou botões de navegação na janela principal. a instância regular da ajuda do Windows também pode ser usada para exibir a ajuda em uma ou mais janelas secundárias em vez da janela principal.

### <a name="pop-up-topics"></a>Tópicos pop-up

Você pode exibir um tópico pop-up que contém informações para um controle ou menu específico chamando a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) com o comando help \_ WM \_ Help ou Help \_ CONTEXTMENU. Esses comandos exibem um tópico em uma janela pop-up próximo ao controle ou menu correspondente. Para permitir que o usuário volte imediatamente para trabalhar no aplicativo, a janela pop-up é destruída assim que o usuário pressiona uma tecla ou clica com o botão esquerdo do mouse.

Você usa o \_ comando help WM \_ Help ao processar mensagens de [**\_ ajuda do WM**](wm-help.md) para controlar as janelas. Como a maioria dos controles passa a mensagem de **\_ ajuda do WM** para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , o procedimento de caixa de diálogo correspondente (ou o procedimento de janela pai) processa essa mensagem. Em vez de fornecer um identificador de contexto específico, o procedimento da caixa de diálogo deve passar uma matriz de pares de identificador de contexto e controle para o [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , juntamente com o identificador de controle especificado no membro **HItemHandle** da estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) passada com a mensagem de **\_ ajuda do WM** . A função determina o identificador do controle para o qual a mensagem de **\_ ajuda do WM** foi gerada e usa o identificador de contexto correspondente para exibir o tópico apropriado.

Você usa o comando de ContextMenu da ajuda \_ ao processar mensagens de [**\_ ContextMenu do WM**](../menurc/wm-contextmenu.md) . Como a maioria dos controles passa a mensagem de **\_ CONTEXTMENU do WM** para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , o procedimento de caixa de diálogo correspondente (ou o procedimento de janela pai) processa essa mensagem. O procedimento especifica uma matriz de pares de identificador de contexto e controle; ele também especifica o identificador no parâmetro *wParam* ao chamar [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para que a função possa escolher o identificador de contexto apropriado da matriz e exibir o tópico apropriado. Ao contrário do comando HELP WM HELP, HELP CONTEXTMENU primeiro exibe um comando \_ \_ \_ **What's This?** em um menu. Se o usuário escolher o comando, **o WinHelp** exibirá o tópico. Caso contrário, a solicitação será cancelada.

Você também pode exibir tópicos pop-up usando o comando HELP CONTEXTPOPUP e especificando um \_ identificador de contexto do tópico. Esse comando é semelhante ao comando HELP CONTEXT, mas invoca a instância pop-up do Windows Ajuda usada por \_ HELP WM HELP e HELP \_ \_ \_ CONTEXTMENU. Os aplicativos podem usar esse comando em resposta a mensagens [**DE \_ AJUDA**](wm-help.md) do WM para exibir ajuda para menus e janelas que não são controles em uma caixa de diálogo. Para usar esse comando com mais eficiência, o aplicativo deve atribuir identificadores de contexto a esses menus e janelas.

Você pode atribuir um identificador de contexto a qualquer janela ou menu no aplicativo. Quando uma [**mensagem \_ WM HELP**](wm-help.md) é gerada, o sistema inclui o identificador de contexto na estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que é passada para a janela pai na mensagem **AJUDA \_ do WM.** A janela pai pode passar o identificador de contexto para [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para exibir o tópico de ajuda solicitado.

Use a [**função SetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) para atribuir um identificador de contexto a uma janela ou controle e a função [**SetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) para atribuir um identificador de contexto a um menu. Você pode recuperar o identificador de contexto de uma janela ou menu usando a função [**GetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) ou [**GetMenuContextHelpId.**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid)

### <a name="keyword-searches"></a>Pesquisas de palavra-chave

Você pode permitir que o usuário encontre e veja tópicos atribuindo palavras-chave a tópicos no arquivo de ajuda. Uma palavra-chave é simplesmente uma cadeia de caracteres associada a um ou mais tópicos. Windows A Ajuda coleta todas as palavras-chave em um arquivo de ajuda, coloca-as em uma tabela e as exibe na lista Índice da caixa de diálogo **Tópicos** da Ajuda. Quando o usuário seleciona uma palavra-chave, Windows Ajuda exibe o tópico de ajuda associado ou, se houver mais de um tópico associado à palavra-chave, exibirá uma lista de tópicos dos quais o usuário pode escolher.

Em um aplicativo, você pode usar o comando HELP KEY, HELP PARTIALKEY ou HELP MULTIKEY com a \_ \_ função \_ [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para pesquisar e exibir tópicos de ajuda com base em palavras-chave inteiras ou parciais. Especifique o comando, a cadeia de caracteres de palavra-chave, o arquivo de ajuda e o alça para a janela do proprietário. Em todos os casos, se uma única combinação for encontrada, **o WinHelp** exibirá o tópico correspondente. Se mais de uma combinação for encontrada, a função exibirá a caixa de diálogo Tópicos Encontrados e o usuário poderá escolher qual tópico exibir. Se nenhuma corresponder for encontrada, **o WinHelp** exibirá a lista Índice (para HELP KEY e HELP PARTIALKEY) ou exibirá uma mensagem de erro \_ \_ (para HELP \_ MULTIKEY).

Seu aplicativo pode pesquisar várias palavras-chave em uma única chamada para [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) separando as palavras-chave com ponto e vírgula. (Não há suporte para a pesquisa de várias palavras-chave para arquivos de ajuda criados para Windows versão 3. *x*) Ele também poderá pesquisar palavras-chave em vários arquivos de ajuda se o arquivo de ajuda especificado tiver um arquivo contents(.cnt) que contenha comandos :Index ou :Link. Com o comando HELP \_ KEY, **o WinHelp** pesquisa palavras-chave em todos os arquivos especificados por esses comandos. Com os comandos HELP MULTIKEY e HELP PARTIALKEY, a função pesquisa todos os arquivos, exceto aqueles \_ \_ especificados pelos comandos :Link.

Por padrão, Windows Ajuda reconhece apenas a tabela de palavras-chave identificada pelo caractere de nota de rodapé K no arquivo de origem da ajuda. Você pode direcionar Windows ajuda para criar tabelas de palavras-chave adicionais adicionais adicionando um caractere de nota de rodapé diferente de K, com a definição de palavra-chave, no arquivo de origem da ajuda. (O caractere de nota de rodapé A, no entanto, é reservado.) Você deve definir quaisquer tabelas de palavras-chave adicionais usando instruções MULTIKEY na seção OPÇÕES do arquivo de projeto \[ ao criar o arquivo de \] ajuda.

Um aplicativo pode usar o comando HELP SETINDEX com a função WinHelp para direcionar Windows Ajuda para exibir uma tabela de palavras-chave diferente de K em sua \_ lista índice. [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Para direcionar Windows ajuda para pesquisar uma palavra-chave em uma tabela de palavra-chave alternativa, um aplicativo pode usar o comando HELP \_ MULTIKEY. Especifique a palavra-chave e a tabela de palavras-chave [**em uma estrutura MULTIKEYHELP,**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) que você passa para **WinHelp.**

Quando [**o WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) exibe um tópico, ele o exibe na janela especificada pela nota de rodapé ">" para o tópico, na janela especificada pelo comando :Base no arquivo de conteúdo ou na janela principal. Se a janela principal já estiver aberta para um arquivo de ajuda diferente quando você chamar **WinHelp**, a função ocultará a janela principal durante a pesquisa. Nesse caso, cancelar as caixas de diálogo **Tópicos Encontrados** e **Tópicos** da Ajuda fecha a janela principal.

### <a name="secondary-help-windows"></a>Janelas de Ajuda Secundária

A janela principal do aplicativo Windows Ajuda é chamada de janela primária. Windows A ajuda também pode exibir tópicos de ajuda em uma janela secundária. Ao contrário da janela de Ajuda primária, uma janela secundária não contém uma barra de menus. Você pode incluir uma barra de navegação em uma janela secundária e adicionar botões à barra. Você também pode optar por fazer com que Windows Ajuda ajuste automaticamente a altura da janela secundária para acomodar o tópico.

Você deve definir janelas secundárias na seção WINDOWS do arquivo de projeto de ajuda, fornecendo o nome e, opcionalmente, o tamanho inicial e a \[ \] posição de cada janela. Você pode direcionar o aplicativo Windows Ajuda para exibir um tópico em uma janela secundária, aplicando um colchete angular (>) e o nome que você definiu para a janela secundária ao nome do arquivo de ajuda. A cadeia de caracteres resultante é passada para a [**função WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

Um aplicativo pode alterar o tamanho e a posição de uma janela primária ou secundária especificando o endereço de uma estrutura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) e o comando HELP SETWINPOS em uma chamada para \_ [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). **HELPWININFO** especifica o nome da janela e seu novo tamanho e posição.

### <a name="training-card-help"></a>Ajuda do cartão de treinamento

Usando a ajuda do cartão de treinamento, um aplicativo pode exibir uma sequência de instruções para orientar o usuário pelas etapas de uma tarefa. Um cartão de treinamento normalmente consiste em texto que explica uma etapa específica e botões associados a macros TCard, que permitem que o usuário diga ao aplicativo o que fazer em seguida. Os cartões de treinamento só podem ser exibidos em janelas secundárias e não devem conter links a quente para outros tópicos no arquivo de ajuda.

Um aplicativo inicia a instância do cartão de treinamento Windows Ajuda chamando a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) e especificando o comando HELP TCARD em combinação com outro comando, como \_ HELP \_ CONTEXT. Posteriormente, quando o usuário clica em um botão no cartão de treinamento, clica em um ponto de acesso atribuído à macro TCard ou fecha o cartão de treinamento, Windows Ajuda notifica o aplicativo enviando uma mensagem [**\_ TCARD WM.**](wm-tcard.md) O *parâmetro wParam* identifica o botão ou a ação do usuário e o parâmetro *lParam* contém dados adicionais, o significado do qual depende do valor *de wParam*.

### <a name="canceling-help"></a>Cancelando a ajuda

Windows A Ajuda requer que um aplicativo cancele explicitamente a ajuda para que ele possa liberar todos os recursos usados para controlar o aplicativo e seus arquivos de ajuda. O aplicativo pode fazer isso a qualquer momento chamando a [**função WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) e especificando o comando HELP \_ QUIT. Observe que isso não é verdadeiro para a instância pop-up do Windows Ajuda. Um aplicativo não deve tentar fechar uma instância pop-up.

Se um aplicativo tiver feito chamadas ao [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), ele deverá cancelar a ajuda antes de fechar sua janela principal (por exemplo, em resposta à mensagem WM DESTROY no \_ procedimento da janela principal). Um aplicativo precisa chamar **o WinHelp** apenas uma vez para cancelar a ajuda, não importa quantos arquivos de ajuda ele tenha aberto. Windows A ajuda permanece em execução até que todos os aplicativos ou DLLs tenham cancelado a ajuda.

Para fechar a instância do cartão de treinamento Windows Ajuda, você deve especificar os comandos HELP TCARD e HELP QUIT ao \_ \_ chamar [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Um aplicativo não precisa cancelar a instância do cartão de treinamento Windows Ajuda se o usuário cancelá-la primeiro. Windows A Ajuda notifica um aplicativo quando o usuário cancela a instância do cartão de treinamento enviando a mensagem [**\_ WM TCARD**](wm-tcard.md) com o parâmetro *wParam* definido como IDCLOSE.

## <a name="using-help"></a>Usando a Ajuda

Esta seção mostra como fornecer ajuda contextucional para uma caixa de diálogo e como definir a aparência de uma janela de Ajuda secundária.

-   [Fornecendo ajuda em uma caixa de diálogo](#providing-help-in-a-dialog-box)
-   [Definindo a aparência de uma janela de ajuda secundária](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Fornecendo ajuda em uma caixa de diálogo

Para fornecer ajuda contextutiva em uma caixa de diálogo, você deve criar uma matriz que consiste em pares de **valores DWORD.** O primeiro valor em cada par é o identificador de um controle na caixa de diálogo e o segundo é o identificador de contexto do tópico de ajuda para o controle. A matriz deve conter um par de identificadores para cada controle na caixa de diálogo.

O procedimento da caixa de diálogo deve processar as [**mensagens WM \_ HELP**](wm-help.md) e [**WM \_ CONTEXTMENU.**](../menurc/wm-contextmenu.md) O procedimento da caixa de diálogo recebe **AJUDA DO WM \_** quando o usuário pressiona a tecla e **WM \_ CONTEXTMENU** quando o usuário clica no botão direito do mouse.

O *parâmetro lParam* do [**WM \_ HELP**](wm-help.md) contém o endereço de uma [**estrutura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo) O **membro hItemHandle** dessa estrutura identifica o controle para o qual o usuário solicitou ajuda. Você deve passar esse identificador para a [**função WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) junto com o comando HELP WM HELP, o nome do arquivo de ajuda e um ponteiro para a matriz \_ de \_ identificadores. A **função WinHelp** pesquisa na matriz o identificador de controle do controle especificado e recupera o identificador de contexto de ajuda correspondente. Em seguida, a função passa o identificador de contexto de ajuda para Windows Ajuda, que localiza o tópico correspondente e o exibe em uma janela pop-up. Se o controle tiver um identificador de -1, o sistema procurará o próximo controle que é uma parada de tabulação e, em seguida, usará seu identificador para encontrar o identificador de contexto de ajuda. Por esse motivo, é importante que você coloque o texto estático antes dos controles em um arquivo de recurso.

Ao chamar a [**função WinHelp,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) o processamento [**de WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) é semelhante ao processamento [**da AJUDA do WM \_**](wm-help.md) com estas duas exceções:

-   Você passa o *parâmetro wParam* do [**WM \_ CONTEXTMENU,**](../menurc/wm-contextmenu.md)que é o handle para o controle que enviou a mensagem.
-   Especifique o **comando HELP \_ CONTEXTMENU** em vez **de HELP WM \_ \_ HELP**.

O **comando HELP \_ CONTEXTMENU** Windows Ajuda para exibir um menu antes de exibir o tópico de ajuda. O menu é definido pelo sistema. Ele permite que o usuário exibir ajuda para o controle ou exibir a caixa **de diálogo Tópicos** da Ajuda.

O exemplo a seguir mostra como implementar a ajuda contextitivo em uma caixa de diálogo.


```
LRESULT CALLBACK EditDlgProc(HWND hwndDlg, UINT uMsg, 
                             WPARAM wParam, LPARAM lParam) 
{ 
    // Create an array of control identifiers and context identifiers. 
    static DWORD aIds[ ] = 
    { 
        ID_SAVE,   IDH_SAVE, 
        ID_DELETE, IDH_DELETE, 
        ID_COPY,   IDH_COPY, 
        ID_PASTE,  IDH_PASTE, 
        0,0 
    }; 

    switch (uMsg) 
    { 
        case WM_HELP: 
            WinHelp(((LPHELPINFO)lParam)->hItemHandle, "helpfile.hlp", 
                    HELP_WM_HELP, (DWORD)(LPSTR)aIds); 
            break; 

        case WM_CONTEXTMENU: 
            WinHelp((HWND)wParam, "helpfile.hlp", HELP_CONTEXTMENU, 
                    (DWORD)(LPVOID)aIds); 
            break; 
        
        // Process other messages here. 
    } 
    return FALSE; 
}
```



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Definindo a aparência de uma janela de ajuda secundária

Um aplicativo pode definir o tamanho, a posição e o estado de uma janela de ajuda secundária passando o comando HELP SETWINPOS e o endereço de uma estrutura \_ [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) para a [**função WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Os membros de **HELPWININFO especificam** o nome da janela a ser mudada e o novo tamanho, a posição e o estado de exibição da janela.

O exemplo a seguir define a aparência de uma janela secundária chamada \_ "menu wnd". O nome deve ser definido na seção \[ WINDOWS do arquivo de projeto de \] ajuda.


```
BOOL DoWindowSize(VOID) 
{ 
    HANDLE hhwi; 
    LPHELPWININFO lphwi; 
    WORD wSize; 
    char *szWndName = "wnd_menu"; 
    size_t NameLength;      // Does not include the terminating null character
    HRESULT hr
    BOOL retval;

    hr = StringCbLengthA(szWndName, STRSAFE_MAX_CCH, &NameLength);
    
    if (SUCCEEDED(hr))
    {
        // Add 1 to account for the name string's terminating null character.
        NameLength++;
        
        // The HELPWININFO structure contains a minimal TCHAR array of size [2] 
        // that is used for the window name. Since sizeof(HELPWININFO) 
        // includes those two TCHARS, they must be subtracted from the 
        // total when adding the actual string length to calculate the  
        // size of the structure. 
        wSize = sizeof(HELPWININFO) - 2 + NameLength; 
    }
    else
        // Something's amiss with the string.
        return FALSE;
        
    hhwi  = GlobalAlloc(GHND, wSize); 
    lphwi = (LPHELPWININFO)GlobalLock(hhwi); 

    lphwi->wStructSize = wSize; 
    lphwi->x    = 256;      // horizontal position 
    lphwi->y    = 256;      // vertical position 
    lphwi->dx   = 767;      // width 
    lphwi->dy   = 512;      // height 
    lphwi->wMax = SW_SHOW;  // show the window 
    
    // secondary window
    hr = StringCbCopyA(lphwi->rgchMember, sizeof(lphwi->rgchMember), szWndName);
    
    if (SUCCEEDED(hr))
    {
        WinHelp(hwnd, "myhelp.hlp", HELP_SETWINPOS, (DWORD)lphwi); 
     
        GlobalUnlock(hhwi); 
        GlobalFree(hhwi); 

        return TRUE; 
    }
    else
        // There was a problem copying the window name.
        return FALSE;
}
```



 

 
