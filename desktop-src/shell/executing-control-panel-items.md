---
description: Discute métodos de abertura de um item Painel de Controle para Windows Vista e sistemas posteriores, bem como abranger comandos Painel de Controle herdado.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Executando Painel de Controle itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb941bb7542b0d786d682e6626e8d78faea8bd7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478412"
---
# <a name="executing-control-panel-items"></a>Executando Painel de Controle itens

> [!Note]  
> Se você estiver procurando a lista de nomes canônicos e de módulo para Painel de Controle, consulte Nomes canônicos [de Painel de Controle itens](controlpanel-canonical-names.md).

 

Há duas maneiras de abrir um Painel de Controle item:

-   O usuário pode abrir Painel de Controle e abrir um item clicando ou clicando duas vezes no ícone do item.
-   O usuário ou um aplicativo pode iniciar um item Painel de Controle executando-o diretamente no prompt de linha de comando.

Um aplicativo pode abrir o Painel de Controle programaticamente usando a [**função WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



O exemplo a seguir mostra como um aplicativo pode iniciar o item Painel de Controle chamado **MyCpl.cpl** usando a [**função WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Quando um Painel de Controle item é aberto por meio de uma linha de comando, você pode instruí-lo a abrir para uma guia específica no item. Devido à adição e remoção de determinadas guias em alguns itens Windows Vista Painel de Controle, a numeração das guias pode ter sido alterada em Windows XP. Por exemplo, o exemplo a seguir inicia a quarta guia no item Sistema no Windows XP e a terceira guia no Windows Vista.


```
control.exe sysdm.cpl,,3
```



Este tópico aborda o seguinte:

-   [Windows Nomes canônicos do Vista](#windows-vista-canonical-names)
-   [Novos comandos para Windows Vista](#new-commands-for-windows-vista)
-   [Comandos Painel de Controle herdado](#legacy-control-panel-commands)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Nomes canônicos do Vista

No Windows Vista e posterior, o método preferencial de iniciar um item Painel de Controle de uma linha de comando é usar o nome canônico do Painel de Controle item. Um nome canônico é uma cadeia de caracteres não localizada que o Painel de Controle item declara no Registro. O valor de usar um nome canônico é que ele abstrai o nome do módulo do Painel de Controle item. Um item pode ser implementado em um .dll e posteriormente ser reimplementado como um .exe ou alterar seu nome de módulo. Desde que o nome canônico permaneça o mesmo, qualquer programa que o abra usando esse nome canônico não precisará ser atualizado.

Por convenção, o nome canônico é formado como "CorporationName.ControlPanelItemName".

O exemplo a seguir mostra como um aplicativo pode iniciar o Painel de Controle item **Windows Atualizar** com [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Para iniciar um Painel de Controle com seu nome canônico, use: "%systemroot% \\ system32 \\control.exe /name *canonicalName"*

Para abrir uma sub page específica em um item ou abri-la com parâmetros adicionais, use: "%systemroot% \\ system32 \\control.exe /name **canonicalName** /page **pageName"**

Um aplicativo também pode implementar o método [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) para iniciar Painel de Controle itens, incluindo a capacidade de abrir uma subpásia específica.

Para ver uma lista completa de Painel de Controle canônicos de item, consulte [Nomes canônicos de Painel de Controle itens](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Novos comandos para Windows Vista

No Windows Vista, algumas opções que foram acessadas por um módulo .cpl no Windows XP agora são implementadas como .exe arquivos. Isso fornece segurança adicionada, permitindo que os usuários padrão sejam solicitados a fornecer credenciais de administrador ao tentar iniciar os arquivos. As opções que não exigem segurança extra são acessadas pelas mesmas linhas de comando que foram usadas no Windows XP. Veja a seguir uma lista de comandos usados no Windows Vista para acessar guias específicas de Painel de Controle itens:

### <a name="personalization"></a>Personalização

-   Tamanho da fonte e DPI: %windir% \\ system32 \\DpiScaling.exe
-   Resolução de tela: %windir% \\ system32 \\control.exe desk.cpl,Configurações,@Settings
-   Configurações de exibição: %windir% \\ system32 \\control.exe desk.cpl,Configurações,@Settings
-   Temas: %windir% \\ system32 \\control.exe desk.cpl,Temas,@Themes
-   Protetor de tela: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver
-   Multi monitor: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor
-   Esquema de cores: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization
-   Tela de fundo da área de trabalho: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /page pageWallpaper

> [!Note]  
> As edições Starter e Basic não são control.exe comando /name Microsoft.Personalization.

 

### <a name="system"></a>Sistema

-   Desempenho: %windir% \\ system32 \\SystemPropertiesPerformance.exe
-   Acesso remoto: %windir% \\ system32 \\SystemPropertiesRemote.exe
-   Nome do computador: %windir% \\ system32 \\SystemPropertiesComputerName.exe
-   Proteção do sistema: %windir% \\ system32 \\SystemPropertiesProtection.exe
-   Propriedades avançadas do sistema: %windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programas e Recursos

-   Adicionar ou remover programas: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures
-   Windows recursos: %windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Opções regionais e de idioma

-   Teclado: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"
-   Local: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"
-   Administrativo: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"

### <a name="folder-options"></a>Opções de Pasta

-   Pesquisa de pasta: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 2
-   Associações de arquivo: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc
-   Exibição: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 7
-   Geral: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 0

### <a name="power-options"></a>Opções de Energia

-   Editar as configurações atuais do plano: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pagePlanSettings
-   Configurações do sistema: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings
-   Criar um plano de energia: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageCriateNewPlan
-   Não há nenhum comando canônico para a página Configurações avançado, ele é acessado da maneira mais antiga: %windir% \\ system32 \\control.exe powercfg.cpl,,3

## <a name="legacy-control-panel-commands"></a>Comandos Painel de Controle herdado

Quando você usa a [**função WinExec,**](/windows/win32/api/winbase/nf-winbase-winexec) o sistema pode reconhecer comandos Painel de Controle especiais. Esses comandos são pré-Windows Vista.




| | | control.exe área de trabalho | Inicia a janela <strong>Propriedades de Vídeo</strong> aplicativo.<blockquote>[!Note]<br />As edições Starter e Basic não são suportadas por este comando.</blockquote><br /> | | control.exe cor | Inicia a janela <strong>Propriedades de Vídeo</strong> com a <strong>guia</strong> Aparência pré-selecionada. | | control.exe data/hora | Inicia a janela <strong>Propriedades de Data e</strong> Hora. | | control.exe internacional | Inicia a janela <strong>Opções Regionais e de</strong> Idioma. | | control.exe mouse | Inicia a janela <strong>Propriedades do</strong> Mouse. | | control.exe teclado | Inicia a janela <strong>Propriedades do</strong> Teclado. | | control.exe impressoras | Exibe a <strong>pasta Impressoras e Faxes.</strong> | | control.exe fontes | Exibe a <strong>pasta Fontes.</strong> | 




 

Para Windows 2000 e sistemas posteriores:



| Comando                    | Descrição                                              |
|----------------------------|----------------------------------------------------------|
| control.exe pastas        | Inicia a janela **Opções de** Pasta.                  |
| control.exe netware        | Inicia a janela **Novell NetWare** (se instalada).   |
| control.exe telefonia      | Inicia a janela **opções Telefone e Modem.**         |
| control.exe admintools     | Exibe a **pasta Ferramentas Administrativas.**            |
| control.exe schedtasks     | Exibe a pasta **Tarefas Agendadas.**                 |
| control.exe netconnections | Exibe a pasta **Conexões de** Rede.             |
| control.exe inomeado       | Inicia a **janela Monitor ComEdido** (se instalada). |
| control.exe userpasswords  | Inicia a janela **Contas de** Usuário.                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Painel de Controle itens](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
</dt> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Processamento de mensagens do painel de controle](message-processing.md)
</dt> <dt>

[Estendendo itens do painel de controle do sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> <dt>

[acessando o painel de controle no modo de Cofre em Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
