---
description: Discute métodos de abrir um item do painel de controle para o Windows Vista e sistemas posteriores, além de abranger comandos herdados do painel de controle.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Executando itens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989046"
---
# <a name="executing-control-panel-items"></a>Executando itens do painel de controle

> [!Note]  
> Se você estiver procurando a lista de nomes canônicos e de módulo para itens do painel de controle, consulte [nomes canônicos de itens do painel de controle](controlpanel-canonical-names.md).

 

Há duas maneiras de abrir um item do painel de controle:

-   O usuário pode abrir o painel de controle e, em seguida, abrir um item clicando ou clicando duas vezes no ícone do item.
-   O usuário ou um aplicativo pode iniciar um item do painel de controle executando-o diretamente do prompt de linha de comando.

Um aplicativo pode abrir o painel de controle programaticamente usando a função [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



O exemplo a seguir mostra como um aplicativo pode iniciar o item do painel de controle chamado **MyCpl.cpl** usando a função [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Quando um item do painel de controle é aberto por meio de uma linha de comando, você pode instruí-lo a abrir para uma determinada guia no item. Devido à adição e remoção de determinadas guias em alguns itens do painel de controle do Windows Vista, a numeração das guias pode ter mudado do Windows XP. Por exemplo, os exemplos a seguir iniciam a quarta guia no item do sistema no Windows XP e a terceira guia do Windows Vista.


```
control.exe sysdm.cpl,,3
```



Este tópico aborda o seguinte:

-   [Nomes canônicos do Windows Vista](#windows-vista-canonical-names)
-   [Novos comandos para o Windows Vista](#new-commands-for-windows-vista)
-   [Comandos do painel de controle herdado](#legacy-control-panel-commands)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-vista-canonical-names"></a>Nomes canônicos do Windows Vista

No Windows Vista e posterior, o método preferencial de iniciar um item do painel de controle a partir de uma linha de comando é usar o nome canônico do item do painel de controle. Um nome canônico é uma cadeia de caracteres não localizada que o item do painel de controle declara no registro. O valor de usar um nome canônico é que ele abstrai o nome do módulo do item do painel de controle. Um item pode ser implementado em uma. dll e, posteriormente, ser reimplementado como um. exe ou alterar o nome do módulo. Desde que o nome canônico permaneça o mesmo, então qualquer programa que o abre usando esse nome canônico não precisa ser atualizado.

Por convenção, o nome canônico é formado como "Corporationname. ControlPanelItemName".

O exemplo a seguir mostra como um aplicativo pode iniciar o item do painel de controle **Windows Update** com [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Para iniciar um item do painel de controle com seu nome canônico, use: "% SystemRoot% \\ system32 \\control.exe/name *canônicaname*"

Para abrir uma subpágina específica em um item ou abri-la com parâmetros adicionais, use: "% SystemRoot% \\ system32 \\control.exe/name **Canônicaname** / **PageName**"

Um aplicativo também pode implementar o método [**IOpenControlPanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) para iniciar itens do painel de controle, incluindo a capacidade de abrir uma subpágina específica.

Para obter uma lista completa de nomes canônicos de itens do painel de controle, consulte [nomes canônicos de itens do painel de controle](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Novos comandos para o Windows Vista

No Windows Vista, algumas opções que foram acessadas por um módulo. cpl no Windows XP agora são implementadas como arquivos. exe. Isso fornece segurança adicional, permitindo que os usuários padrão sejam solicitados a fornecer credenciais de administrador ao tentar iniciar os arquivos. As opções que não exigem segurança extra são acessadas pelas mesmas linhas de comando que foram usadas no Windows XP. Veja a seguir uma lista de comandos usados no Windows Vista para acessar guias específicas de itens do painel de controle:

### <a name="personalization"></a>Personalização

-   Tamanho da fonte e DPI:% WINDIR% \\ system32 \\DpiScaling.exe
-   Resolução de tela:% WINDIR% \\ system32 \\control.exe desk.cpl, configurações,@Settings
-   Configurações de exibição:% WINDIR% \\ system32 \\control.exe desk.cpl, configurações,@Settings
-   Temas:% WINDIR% \\ system32 \\control.exe desk.cpl, temas,@Themes
-   Proteção de tela:% WINDIR% \\ system32 \\control.exe desk.cpl, proteção de tela,@screensaver
-   Vários monitores:% WINDIR% \\ system32 \\control.exe desk.cpl, monitor,@Monitor
-   Esquema de cores:% WINDIR% \\ system32 \\control.exe/name Microsoft. Personalization/pageColorization
-   Plano de fundo da área de trabalho:% WINDIR% \\ system32 \\control.exe/name Microsoft. Personalization/pageWallpaper

> [!Note]  
> As edições inicial e básica não dão suporte ao comando control.exe/name Microsoft. Personalization.

 

### <a name="system"></a>Sistema

-   Desempenho:% WINDIR% \\ system32 \\SystemPropertiesPerformance.exe
-   Acesso remoto:% WINDIR% \\ system32 \\SystemPropertiesRemote.exe
-   Nome do computador:% WINDIR% \\ system32 \\SystemPropertiesComputerName.exe
-   Proteção do sistema:% WINDIR% \\ system32 \\SystemPropertiesProtection.exe
-   Propriedades avançadas do sistema:% WINDIR% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programas e Recursos

-   Adicionar ou remover programas:% WINDIR% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures
-   Recursos do Windows:% WINDIR% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Opções regionais e de idioma

-   Teclado:% SystemRoot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions//p: "teclado"
-   Local:% SystemRoot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions//p: "local"
-   Administrativo:% SystemRoot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions//p: "administrativo"

### <a name="folder-options"></a>Opções de Pasta

-   Pesquisa de pastas:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opções \_ rundll 2
-   Associações de arquivo:% WINDIR% \\ system32 \\control.exe/name Microsoft. defaultprograms/pageFileAssoc
-   Exibição:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opções \_ rundll 7
-   Geral:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opções \_ rundll 0

### <a name="power-options"></a>Opções de Energia

-   Editar configurações do plano atual:% WINDIR% \\ system32 \\control.exe/name Microsoft. poweroptions/pagePlanSettings
-   Configurações do sistema:% WINDIR% \\ system32 \\control.exe/name Microsoft. poweroptions/pageGlobalSettings
-   Criar um plano de energia:% WINDIR% \\ system32 \\control.exe/name Microsoft. poweroptions/pageCreateNewPlan
-   Não há nenhum comando canônico para a página de configurações avançadas, ele é acessado da maneira mais antiga:% WINDIR% \\ system32 \\control.exe powercfg.cpl,, 3

## <a name="legacy-control-panel-commands"></a>Comandos do painel de controle herdado

Quando você usa a função [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , o sistema pode reconhecer comandos especiais do painel de controle. Esses comandos são preessados no Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Área de trabalho control.exe</td>
<td>Inicia a janela <strong>Propriedades de exibição</strong> .
<blockquote>
[!Note]<br />
As edições inicial e básica não oferecem suporte a esse comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Cor control.exe</td>
<td>Inicia a janela <strong>Propriedades de exibição</strong> com a guia <strong>aparência</strong> selecionada.</td>
</tr>
<tr class="odd">
<td>Data/hora control.exe</td>
<td>Inicia a janela de <strong>Propriedades de data e hora</strong> .</td>
</tr>
<tr class="even">
<td>control.exe internacional</td>
<td>Inicia a janela <strong>Opções regionais e de idioma</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe mouse</td>
<td>Inicia a janela <strong>Propriedades do mouse</strong> .</td>
</tr>
<tr class="even">
<td>control.exe teclado</td>
<td>Inicia a janela <strong>Propriedades do teclado</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe impressoras</td>
<td>Exibe a pasta <strong>impressoras e aparelhos de fax</strong> .</td>
</tr>
<tr class="even">
<td>control.exe fontes</td>
<td>Exibe a pasta <strong>fontes</strong> .</td>
</tr>
</tbody>
</table>



 

Para sistemas Windows 2000 e posteriores:



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| control.exe pastas        | Inicia a janela de **Opções de pasta** .                  |
| control.exe NetWare        | Inicia a janela do **Novell NetWare** (se instalado).   |
| control.exe telefonia      | Inicia a janela **Opções de telefone e modem** .         |
| control.exe AdminTools     | Exibe a pasta **Ferramentas administrativas** .            |
| control.exe schedtasks     | Exibe a pasta **tarefas agendadas** .                 |
| control.exe netconnections | Exibe a pasta **conexões de rede** .             |
| control.exe infravermelho       | Inicia a janela do **Monitor de infravermelho** (se instalado). |
| Senhas de Usercontrol.exe  | Inicia a janela **contas de usuário** .                   |



 

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

[Estendendo itens do painel de controle do sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> <dt>

[Acessando o painel de controle no modo de segurança no Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
