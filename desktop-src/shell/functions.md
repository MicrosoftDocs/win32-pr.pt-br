---
description: Esta seção descreve as funções do shell do Windows.
title: Funções do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f4d6c0c4-8db3-4721-80f5-2a73bb57cd99
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c8e31bdaac8ec581504326c17d5d37012dd019d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988992"
---
# <a name="shell-functions"></a>Funções do Shell

\[Esta função não é mais implementada.\]

Esta seção descreve as funções do shell do Windows.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="intsafe-h-functions-bumper.md">Funções Intsafe. h</a><br/></td>

</tr>
<tr class="even">
<td><a href="library-functions-bumper.md">Funções de biblioteca</a><br/></td>

</tr>
<tr class="odd">
<td><a href="path-functions.md">Funções de caminho</a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a><br/></td>
<td>Recupera um objeto que implementa uma interface <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>AssocGetDetailsOfPropKey</strong></a><br/></td>
<td>Recupera o valor de uma determinada chave de propriedade usando as informações de associação de arquivo fornecidas pelas <a href="nse-works.md">extensões de namespace</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a><br/></td>
<td>Cria um menu de contexto para um grupo selecionado de objetos de pasta de arquivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>CIShutdown</strong></a><br/></td>
<td>Desliga o indexador de conteúdo e fecha todos os catálogos abertos. <br/>
<blockquote>
[!Note]<br />
Não há suporte para essa função a partir do Windows 8.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>CommandLineToArgvW</strong></a><br/></td>
<td>Analisa uma cadeia de caracteres de linha de comando Unicode e retorna uma matriz de ponteiros para os argumentos de linha de comando, juntamente com uma contagem desses argumentos, de forma semelhante aos valores de <em>argv</em> e <em>argc</em> de tempo de execução padrão C.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a><br/></td>
<td>Serve como o ponto de entrada para um aplicativo do painel de controle. Esta é uma função de retorno de chamada definida pela biblioteca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>CreateAppContainerProfile</strong></a><br/></td>
<td>Cria um perfil por usuário e por aplicativo para aplicativos da Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a><br/></td>
<td>Recupera as variáveis de ambiente para o usuário especificado. Esse bloco pode então ser passado para a função <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>CreateProcessAsUser</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="createmrulist.md"><strong>CreateMRUListW</strong></a><br/></td>
<td>Cria uma nova lista MRU (usada mais recentemente).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>CreateProfile</strong></a><br/></td>
<td>Cria um novo perfil de usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>DefScreenSaverProc</strong></a><br/></td>
<td>Fornece o processamento padrão para todas as mensagens que um aplicativo de proteção de tela não processa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>DefSubclassProc</strong></a><br/></td>
<td>Chama o próximo manipulador na cadeia de subclasse de uma janela. O último manipulador na cadeia de subclasse chama o procedimento de janela original para a janela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>DeleteAppContainerProfile</strong></a><br/></td>
<td>Exclui o perfil especificado por usuário e por aplicativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>DeleteProfile</strong></a><br/></td>
<td>Exclui o perfil do usuário e todas as configurações relacionadas ao usuário do computador especificado. O chamador deve ter privilégios administrativos para excluir o perfil de um usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>DestroyEnvironmentBlock</strong></a><br/></td>
<td>Libera as variáveis de ambiente criadas pela função <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>DeriveAppContainerSidFromAppContainerName</strong></a><br/></td>
<td>Obtém o SID do perfil especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName</strong></a><br/></td>
<td>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName é reservado para uso futuro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>DLLGETVERSIONPROC</em></a><br/></td>
<td>Implementado por muitas das DLLs do shell do Windows para permitir que os aplicativos obtenham informações de versão específicas da DLL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a><br/></td>
<td>Registra se uma janela aceita arquivos soltos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>DragFinish</strong></a><br/></td>
<td>Libera a memória que o sistema alocou para uso na transferência de nomes de arquivo para o aplicativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>DragQueryFile</strong></a><br/></td>
<td>Recupera os nomes dos arquivos ignorados que resultam de uma operação de arrastar e soltar com êxito.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>DragQueryPoint</strong></a><br/></td>
<td>Recupera a posição do ponteiro do mouse no momento em que um arquivo foi Descartado durante uma operação de arrastar e soltar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>DuplicateIcon</strong></a><br/></td>
<td>Cria uma duplicata de um ícone especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>ExpandEnvironmentStringsForUser</strong></a><br/></td>
<td>Expande a cadeia de caracteres de origem usando o bloco de ambiente estabelecido para o usuário especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>ExtractAssociatedIcon</strong></a><br/></td>
<td>Obtém um identificador para um ícone armazenado como um recurso em um arquivo ou um ícone armazenado no arquivo executável associado de um arquivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>ExtractIcon</strong></a><br/></td>
<td>Obtém um identificador para um ícone do arquivo executável especificado, DLL ou arquivo de ícone. <br/> Para recuperar uma matriz de identificadores para ícones grandes ou pequenos, use a função <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a><br/></td>
<td>A função <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> cria uma matriz de identificadores para ícones grandes ou pequenos extraídos do arquivo executável especificado, dll ou arquivo de ícone.<br/></td>
</tr>
<tr class="odd">
<td><a href="fileiconinit.md"><strong>FileIconInit</strong></a><br/></td>
<td>Inicializa ou reinicializa a lista de imagens do sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>FindExecutable</strong></a><br/></td>
<td>Recupera o nome e o identificador do arquivo executável (. exe) associado a um arquivo de documento específico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>FreeConfirmConflictItem</strong></a><br/></td>
<td>Libera os recursos que foram alocados para uma estrutura de <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>FreeIDListArray</strong></a><br/></td>
<td>Libera a memória usada por um ponteiro para uma matriz de lista de PIDL (lista de identificadores de item).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>FreeIDListArrayChild</strong></a><br/></td>
<td>Libera o espaço de memória para a matriz de ponteiros para IDs de item filho. Isso libera o PITEMID_CHILDs dentro da matriz e a própria matriz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>FreeIDListArrayFull</strong></a><br/></td>
<td>Libera o espaço de memória para a matriz PIDL. Isso libera o PIDLIST_ABSOLUTEs dentro da matriz e a própria matriz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>FreeKnownFolderDefinitionFields</strong></a><br/></td>
<td>Libera os campos alocados no resultado de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>IKnownFolder:: GetFolderDefinition</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="freemrulist.md"><strong>FreeMRUList</strong></a><br/></td>
<td>Libera o identificador associado à lista MRU e grava os dados armazenados em cache no registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>GetAllUsersProfileDirectory</strong></a><br/></td>
<td>Recupera o caminho para a raiz do diretório que contém os dados de programa compartilhados por todos os usuários.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>GetAppContainerFolderPath</strong></a><br/></td>
<td>Obtém o caminho da pasta de dados do aplicativo local para o contêiner do aplicativo especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>GetAppContainerRegistryLocation</strong></a><br/></td>
<td>Obtém o local do armazenamento do registro associado a um contêiner de aplicativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>GetContractDelegateWindow</strong></a><br/></td>
<td>Recupera uma janela que foi definida como um delegado para a janela de primeiro plano principal de um aplicativo com a finalidade de associar a janela delegada aos contratos do aplicativo. Use essa função se você for um desenvolvedor que escreve um aplicativo da Windows Store em C++ nativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>GetCurrentProcessExplicitAppUserModelID</strong></a><br/></td>
<td>Recupera a ID do modelo de usuário (AppUserModelID) do aplicativo definido pelo aplicativo e explícito para o processo atual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>GetDefaultUserProfileDirectory</strong></a><br/></td>
<td>Recupera o caminho para a raiz do perfil do usuário padrão.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>GetDpiForShellUiComponent</strong></a><br/></td>
<td>Recupera os pontos por polegada (DPI) ocupados por uma <a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a> com base no fator de escala atual e <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>GetMenuContextHelpId</strong></a><br/></td>
<td>Recupera o identificador de contexto de ajuda associado ao menu especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>GetProfilesDirectory</strong></a><br/></td>
<td>Recupera o caminho para o diretório raiz onde os perfis de usuário são armazenados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>Getprofiletype</strong></a><br/></td>
<td>Recupera o tipo de perfil carregado para o usuário atual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a><br/></td>
<td>Obtém o fator de escala preferencial para um dispositivo de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>GetScaleFactorForMonitor</strong></a><br/></td>
<td>Obtém o fator de escala de um monitor específico. Essa função substitui <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>GetUserProfileDirectory</strong></a><br/></td>
<td>Recupera o caminho para o diretório raiz do perfil do usuário especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>GetWindowContextHelpId</strong></a><br/></td>
<td>Recupera o identificador de contexto da ajuda, se houver, associado à janela especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>GetWindowSubclass</strong></a><br/></td>
<td>Recupera os dados de referência para o retorno de chamada da subclasse da janela especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>IDListContainerIsConsistent</strong></a><br/></td>
<td>Verifica se a estrutura de contêiner de um IDList é válida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>ILAppendID</strong></a><br/></td>
<td>Acrescenta ou precede uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> para uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>ILClone</strong></a><br/></td>
<td>Clona uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>ILCloneChild</strong></a><br/></td>
<td>Clona uma estrutura de <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> filho.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>ILCloneFirst</strong></a><br/></td>
<td>Clona a primeira estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> em uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>ILCloneFull</strong></a><br/></td>
<td>Clona uma estrutura de <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> completa, ou absoluta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>ILCombine</strong></a><br/></td>
<td>Combina duas estruturas <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>ILCreateFromPath</strong></a><br/></td>
<td>Retorna a estrutura de <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> associada a um caminho de arquivo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>ILFindChild</strong></a><br/></td>
<td>Determina se uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> especificada é o filho de outra estrutura <strong>ITEMIDLIST</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>ILFindLastID</strong></a><br/></td>
<td>Retorna um ponteiro para a última estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> em uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>ILFree</strong></a><br/></td>
<td>Libera uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> alocada pelo shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>ILGetNext</strong></a><br/></td>
<td>Recupera a próxima estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> em uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>ILGetSize</strong></a><br/></td>
<td>Retorna o tamanho, em bytes, de uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>ILIsAligned</strong></a><br/></td>
<td>Verifica se uma <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> constante está alinhada em um limite de ponteiro, que é um DWORD em arquiteturas de 32 bits e um <strong>valor</strong> <strong>QWORD</strong> em arquiteturas de 64 bits.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>ILIsChild</strong></a><br/></td>
<td>Verifica se um PIDL é um PIDL filho, que é um PIDL com exatamente um <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>ILIsEmpty</strong></a><br/></td>
<td>Verifica se uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> está vazia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>ILIsEqual</strong></a><br/></td>
<td>Testa se duas estruturas <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> são iguais em uma comparação binária.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>ILIsParent</strong></a><br/></td>
<td>Testa se uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> é o pai de outra estrutura <strong>ITEMIDLIST</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>ILNext (PCUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Recupera a próxima estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> em uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>ILNext (PUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Recupera a próxima estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> em uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>ILRemoveLastID</strong></a><br/></td>
<td>Remove a última estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> de uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>ILSaveToStream</strong></a><br/></td>
<td>Salva uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> em um fluxo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>ILSkip (PCUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Ignora um determinado número de bytes em uma estrutura de <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> de constante, não alinhada e relativa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>ILSkip (PUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Ignora um determinado número de bytes em uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> relativa e não alinhada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>InetIsOffline</strong></a><br/></td>
<td>Determina se o sistema está conectado à Internet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>InitNetworkAddressControl</strong></a><br/></td>
<td>Inicializa a classe da janela de controle de endereço de rede.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a><br/></td>
<td>Carrega o perfil do usuário especificado. O perfil pode ser um <a href="local-user-profiles.md">perfil de usuário local</a> ou um <a href="roaming-user-profiles.md">perfil de usuário móvel</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a><br/></td>
<td>Executa a caixa de diálogo tipo de conteúdo MIME não registrado.<br/>
<blockquote>
[!Note]<br />
Windows XP Service Pack 2 (SP2) ou posterior: essa função não é mais suportada.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>PathMakeUniqueName</strong></a><br/></td>
<td>Cria um nome de caminho exclusivo a partir de um modelo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>PathYetAnotherMakeUniqueName</strong></a><br/></td>
<td>Cria um nome de arquivo exclusivo com base em um nome de arquivo existente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a><br/></td>
<td>Permite que um aplicativo registre uma função de retorno de chamada por meio da qual pode ser notificado de que sua biblioteca está entrando ou saindo de um estado suspenso. O aplicativo pode usar essas informações para executar as operações necessárias, como preservar o estado, que deve ser executado nesse ponto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>RegisterDialogClasses</strong></a><br/></td>
<td>Registra qualquer classe de janela não padrão exigida por uma caixa de diálogo de configuração de proteção de tela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a><br/></td>
<td>Registra um evento que é disparado quando a escala possivelmente foi alterada. Essa função substitui <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a><br/></td>
<td>Registra uma janela para receber retornos de chamada ao dimensionar as alterações de informações.<br/>
<blockquote>
[!Note]<br />
Não há suporte para essa função a partir de Windows 8.1. Use <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a> em vez disso.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>RemoveWindowSubclass</strong></a><br/></td>
<td>Remove um retorno de chamada de subclasse de uma janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a><br/></td>
<td>Revoga o registro de uma janela, impedindo que ela receba retornos de chamada ao dimensionar as informações de alterações.<br/>
<blockquote>
[!Note]<br />
Não há suporte para essa função a partir de Windows 8.1. Use <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a> em vez disso.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>ScreenSaverConfigureDialog</strong></a><br/></td>
<td>Recebe mensagens enviadas para a caixa de diálogo de configuração de uma proteção de tela. Uma proteção de tela que permite a configuração do usuário deve definir essa função.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>ScreenSaverProc</strong></a><br/></td>
<td>Recebe mensagens enviadas para a janela de proteção de tela especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>SetContractDelegateWindow</strong></a><br/></td>
<td>Associa uma janela de aplicativo que não seja a janela de primeiro plano principal com os contratos de um aplicativo. Use essa função se você for um desenvolvedor que escreve um aplicativo da Windows Store em C++ nativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>SetCurrentProcessExplicitAppUserModelID</strong></a><br/></td>
<td>Especifica um AppUserModelID exclusivo definido pelo aplicativo que identifica o processo atual para a barra de tarefas. Esse identificador permite que um aplicativo agrupe seus processos e janelas associados em um único botão da barra de tarefas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>SetMenuContextHelpId</strong></a><br/></td>
<td>Associa um identificador de contexto de ajuda a um menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>SetWindowContextHelpId</strong></a><br/></td>
<td>Associa um identificador de contexto de ajuda com a janela especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>SetWindowSubclass</strong></a><br/></td>
<td>Instala ou atualiza um retorno de chamada de subclasse de janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a><br/></td>
<td>Notifica o sistema de que um item foi acessado, para fins de rastreamento dos itens usados mais recentemente e com mais frequência. Essa função também pode ser usada para limpar todos os dados de uso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>SHAppBarMessage</strong></a><br/></td>
<td>Envia uma mensagem AppBar para o sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>SHAssocEnumHandlers</strong></a><br/></td>
<td>Retorna um objeto de enumeração para um conjunto especificado de manipuladores de extensão de nome de arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>SHAssocEnumHandlersForProtocolByApplication</strong></a><br/></td>
<td>Obtém uma interface de enumeração que fornece acesso a manipuladores associados a um determinado protocolo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a><br/></td>
<td>Dado um item de namespace de shell especificado na forma de uma pasta e uma lista de identificadores de item relativa a essa pasta, essa função é associada ao pai do item de namespace e, opcionalmente, retorna um ponteiro para o componente final da lista de identificadores de item.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>SHBindToFolderIDListParentEx</strong></a><br/></td>
<td>Estende a função <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a> permitindo que o chamador especifique um contexto de associação.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>SHBindToObject</strong></a><br/></td>
<td>Recupera e associa a um objeto especificado usando o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> do namespace do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>SHBindToParent</strong></a><br/></td>
<td>Usa um ponteiro para uma PIDL (lista de identificadores de item totalmente qualificado) e retorna um ponteiro de interface especificado no objeto pai.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a><br/></td>
<td>Exibe uma caixa de diálogo que permite ao usuário selecionar uma pasta do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a><br/></td>
<td>Bloqueia a memória compartilhada associada a um evento de notificação de alteração do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a><br/></td>
<td>Desbloqueia a memória compartilhada para uma notificação de alteração.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a><br/></td>
<td>Notifica o sistema sobre um evento que um aplicativo executou. Um aplicativo deve usar essa função se executar uma ação que possa afetar o Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>SHChangeNotifyDeregister</strong></a><br/></td>
<td>Cancela o registro do processo de janela do cliente de receber mensagens <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a><br/></td>
<td>Registra uma janela para receber notificações do sistema de arquivos ou do Shell, se o sistema de arquivos oferecer suporte a notificações.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a><br/></td>
<td>Habilita o registro assíncrono e o cancelamento de registro de um thread.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>SHCreateAssociationRegistration</strong></a><br/></td>
<td>Cria um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> com base na implementação de estoque da interface fornecida pelo Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>SHCreateDataObject</strong></a><br/></td>
<td>Cria um objeto de dados em uma pasta pai.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a><br/></td>
<td>Cria um objeto que representa a implementação do menu de contexto padrão do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>SHCreateDefaultExtractIcon</strong></a><br/></td>
<td>Cria um extrator de ícones padrão, cujos padrões podem ser configurados por meio da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>SHCreateDefaultPropertiesOp</strong></a><br/></td>
<td>Cria uma operação de arquivo que define as propriedades padrão no item de shell que ainda não foram definidas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a><br/></td>
<td>Cria e inicializa um objeto de item de Shell a partir de um PIDL. O objeto de item do Shell resultante dá suporte à interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a><br/></td>
<td>Cria e inicializa um objeto de item de Shell a partir de um nome de análise.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>SHCreateItemFromRelativeName</strong></a><br/></td>
<td>Cria e inicializa um objeto de item de Shell a partir de um nome de análise relativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>SHCreateItemInKnownFolder</strong></a><br/></td>
<td>Cria um objeto de item de Shell para um único arquivo que existe dentro de uma pasta conhecida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a><br/></td>
<td>Crie um item de Shell, considerando uma pasta pai e uma ID de item filho.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a><br/></td>
<td>Cria uma nova instância do objeto de exibição de pasta do shell padrão (DefView).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a><br/></td>
<td>Cria uma nova instância do objeto de exibição de pasta do shell padrão. É recomendável que você use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> em vez dessa função.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>SHCreateShellItem</strong></a><br/></td>
<td>Cria um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> . <br/>
<blockquote>
[!Note]<br />
É recomendável que você use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a> em vez desta função.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>SHCreateShellItemArray</strong></a><br/></td>
<td>Cria um objeto de matriz de item de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>SHCreateShellItemArrayFromDataObject</strong></a><br/></td>
<td>Cria um objeto de matriz de item de Shell a partir de um objeto de dados. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>SHCreateShellItemArrayFromIDLists</strong></a><br/></td>
<td>Cria um objeto de matriz de item de Shell de uma lista de estruturas <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>SHCreateShellItemArrayFromShellItem</strong></a><br/></td>
<td>Cria uma matriz de um elemento a partir de um único item de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>SHDefExtractIcon</strong></a><br/></td>
<td>Fornece um manipulador padrão para extrair um ícone de um arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>SHDoDragDrop</strong></a><br/></td>
<td>Executa uma operação de arrastar e soltar. Dá suporte à criação de origem de arrastar sob demanda, bem como a arrastar imagens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a><br/></td>
<td>Envia uma mensagem para a área de status da barra de tarefas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a><br/></td>
<td>Obtém as coordenadas de tela do retângulo delimitador de um ícone de notificação.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>ShellAbout</strong></a><br/></td>
<td>Exibe uma caixa de diálogo <strong>ShellAbout</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="shellddeinit.md"><strong>ShellDDEInit</strong></a><br/></td>
<td>Registra os serviços de troca dinâmica de dados de Shell (DDE) no processo atual, notificando o sistema de que o processo atual deseja hospedar objetos DDE.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a><br/></td>
<td>Executa uma operação em um arquivo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a><br/></td>
<td>Executa uma operação em um arquivo especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>SHEmptyRecycleBin</strong></a><br/></td>
<td>Esvazia a lixeira na unidade especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>SHEnumerateUnreadMailAccounts</strong></a><br/></td>
<td>Enumera as contas de usuário que têm email não lido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>SHEvaluateSystemCommandTemplate</strong></a><br/></td>
<td>Impõe a validação estrita dos parâmetros usados em uma chamada para <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> ou <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a><br/></td>
<td>Copia, move, renomeia ou exclui um objeto do sistema de arquivos. Essa função foi substituída no Windows Vista por <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>SHFreeNameMappings</strong></a><br/></td>
<td>Libera um objeto de mapeamento de nome de arquivo que foi recuperado pela função <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a><br/></td>
<td>Recupera dados de propriedade estendida de uma lista de identificadores relativa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>SHGetDesktopFolder</strong></a><br/></td>
<td>Recupera a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> para a pasta de área de trabalho, que é a raiz do namespace do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>SHGetDiskFreeSpaceEx</strong></a><br/></td>
<td>Recupera informações de espaço em disco para um volume de disco.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>SHGetDriveMedia</strong></a><br/></td>
<td>Retorna o tipo de mídia que está na unidade especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>SHGetFileInfo</strong></a><br/></td>
<td>Recupera informações sobre um objeto no sistema de arquivos, como um arquivo, pasta, diretório ou raiz da unidade.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>SHGetFolderPathEx</strong></a><br/></td>
<td>Recupera o caminho completo de uma pasta conhecida identificada pelo <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>da pasta. Isso estende o <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a> permitindo que você defina o tamanho inicial do buffer de cadeia de caracteres.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>SHGetIconOverlayIndex</strong></a><br/></td>
<td>Retorna o índice do ícone de sobreposição na lista de imagens do sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>SHGetIDListFromObject</strong></a><br/></td>
<td>Recupera o PIDL de um objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>SHGetImageList</strong></a><br/></td>
<td>Recupera uma lista de imagens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>SHGetInstanceExplorer</strong></a><br/></td>
<td>Recupera uma interface que permite extensões de shell hospedadas e outros componentes para impedir que o processo de host seja fechado prematuramente. O processo de host é normalmente o Windows Explorer ou o Windows Internet Explorer, mas essa função também pode ser usada por outros aplicativos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a><br/></td>
<td>Cria um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> ou um objeto relacionado com base em um item especificado por um <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>SHGetItemFromObject</strong></a><br/></td>
<td>Recupera um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> para um objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>SHGetKnownFolderIDList</strong></a><br/></td>
<td>Recupera o caminho de uma pasta conhecida como uma estrutura de <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>SHGetKnownFolderItem</strong></a><br/></td>
<td>Recupera um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> que representa uma pasta conhecida.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a><br/></td>
<td>Recupera o caminho completo de uma pasta conhecida identificada pelo <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>da pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>SHGetLocalizedName</strong></a><br/></td>
<td>Recupera o nome localizado de um arquivo em uma pasta do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a><br/></td>
<td>Recupera o nome de exibição de um item identificado por seu IDList.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>SHGetNameFromPropertyKey</strong></a><br/></td>
<td>Recupera o nome canônico da propriedade, dado seu <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>SHGetNewLinkInfo</strong></a><br/></td>
<td>Cria um nome para um novo atalho com base no destino proposto do atalho. Essa função não cria o atalho, apenas o nome.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a><br/></td>
<td>Converte uma lista de identificadores de item em um caminho de sistema de arquivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>SHGetPathFromIDListEx</strong></a><br/></td>
<td>Converte uma lista de identificadores de item em um caminho de sistema de arquivos. Essa função estende o <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a> permitindo que você defina o tamanho inicial do buffer da cadeia de caracteres e declare as opções abaixo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a><br/></td>
<td>Recupera as configurações de opção do shell atual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a><br/></td>
<td>Recupera informações sobre ícones de shell definidos pelo sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>SHGetTemporaryPropertyForItem</strong></a><br/></td>
<td>Recupera a propriedade temporária para o item especificado. Uma propriedade temporária é um repositório de leitura/gravação que contém propriedades somente pelo tempo de vida do objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> , em vez de ser persistido no item.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>SHGetUnreadMailCount</strong></a><br/></td>
<td>Recupera a contagem de mensagens não lidas de um usuário especificado para qualquer ou todas as contas de email.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>SHIsFileAvailableOffline</strong></a><br/></td>
<td>Determina se um arquivo ou pasta está disponível para uso offline. Essa função também determina se o arquivo deve ser aberto da rede, do cache de Arquivos Offline local ou de ambos os locais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>SHLoadInProc</strong></a><br/></td>
<td>Cria uma instância da classe de objeto especificada de dentro do contexto do processo do Shell. <br/> <strong>Windows Vista</strong> e posterior: essa função foi desabilitada e retorna E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>SHLoadNonloadedIconOverlayIdentifiers</strong></a><br/></td>
<td>Sinaliza o shell que durante a próxima operação que requer informações de sobreposição, ele deve carregar identificadores de sobreposição de ícone que falharam na criação ou não estavam presentes para criação na inicialização. Identificadores que já foram carregados não são afetados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>SHLocalStrDup</strong></a><br/></td>
<td>Faz uma cópia de uma cadeia de caracteres na memória alocada recentemente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>SHMultiFileProperties</strong></a><br/></td>
<td>Exibe uma folha de propriedades mesclada para um conjunto de arquivos. Os valores de propriedade comuns a todos os arquivos são mostrados enquanto aqueles que diferem exibem a cadeia de caracteres <strong>(vários valores)</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>SHOpenFolderAndSelectItems</strong></a><br/></td>
<td>Abre uma janela do Windows Explorer com os itens especificados em uma pasta específica selecionada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a><br/></td>
<td>Exibe a caixa de diálogo <strong>abrir com</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/showsharefolderui"><strong>ShowShareFolderUI</strong></a><br/></td>
<td>Exibe a guia <strong>compartilhamento de pasta</strong> na folha de propriedades da pasta especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>SHParseDisplayName</strong></a><br/></td>
<td>Converte o nome de exibição de um objeto de namespace de Shell em uma lista de identificadores de item e retorna os atributos do objeto. Essa função é o método preferencial para converter uma cadeia de caracteres em um PIDL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>SHPathPrepareForWrite</strong></a><br/></td>
<td>Verifica se o caminho existe. Isso inclui a remontagem de unidades de rede mapeadas, solicitando que a mídia ejetorada seja reinserida, criando os caminhos, solicitando que a mídia seja formatada e fornecendo as interfaces de usuário apropriadas, se necessário. As permissões de leitura/gravação para a mídia não são verificadas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a><br/></td>
<td>Recupera o tamanho da lixeira e o número de itens nela, para uma unidade especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a><br/></td>
<td>Verifica o estado do computador para que o usuário atual determine se o envio de uma notificação é apropriado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>SHRemoveLocalizedName</strong></a><br/></td>
<td>Remove o nome localizado de um arquivo em uma pasta do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>SHRunControlPanel</strong></a><br/></td>
<td>Abre um item do painel de controle. <br/>
<blockquote>
[!Note]<br />
Não há suporte para essa função no Windows Vista
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>SHSetDefaultProperties</strong></a><br/></td>
<td>Aplica o conjunto padrão de propriedades em um item de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>SHSetInstanceExplorer</strong></a><br/></td>
<td>Fornece uma interface que permite que extensões de shell hospedadas e outros componentes impeçam que seu processo de host seja fechado prematuramente. O processo de host é normalmente o Windows Explorer ou o Internet Explorer, mas essa função também pode ser usada por outros aplicativos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>SHSetKnownFolderPath</strong></a><br/></td>
<td>Redireciona uma pasta conhecida para um novo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>SHSetLocalizedName</strong></a><br/></td>
<td>Define o nome localizado de um arquivo em uma pasta do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>SHSetTemporaryPropertyForItem</strong></a><br/></td>
<td>Define uma propriedade temporária para o item especificado. Uma propriedade temporária é mantida em um repositório de leitura/gravação que contém propriedades somente pelo tempo de vida do objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> , em vez de escrevê-las de volta no item.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>SHSetUnreadMailCount</strong></a><br/></td>
<td>Armazena a contagem de mensagens não lidas do usuário atual para uma conta de email especificada no registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>SHTestTokenMembership</strong></a><br/></td>
<td>Usa <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>CheckTokenMembership</strong></a> para testar se o token fornecido é um membro do grupo local com o RID especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>SHUpdateImage</strong></a><br/></td>
<td>Notifica o Shell de que uma imagem na lista de imagens do sistema foi alterada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>SoftwareUpdateMessageBox</strong></a><br/></td>
<td>Exibe uma caixa de mensagem padrão que pode ser usada para notificar um usuário de que um aplicativo foi atualizado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>StgMakeUniqueName</strong></a><br/></td>
<td>Cria um nome exclusivo para um fluxo ou objeto de armazenamento de um modelo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>StrStrNIW</strong></a><br/></td>
<td>Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>StrStrNW</strong></a><br/></td>
<td>Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres. A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TranslateURL</strong></a><br/></td>
<td>Aplica traduções comuns a uma determinada cadeia de caracteres de URL, criando uma nova cadeia de caracteres de URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>UnloadUserProfile</strong></a><br/></td>
<td>Descarrega o perfil de um usuário que foi carregado pela função <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> . O chamador deve ter privilégios administrativos no computador. Para obter mais informações, consulte a seção comentários da função <strong>LoadUserProfile</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>UnregisterAppStateChangeNotification</strong></a><br/></td>
<td>Cancela uma notificação de alteração registrada por meio do <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a><br/></td>
<td>Cancela o registro para o evento de alteração de escala registrado por meio de <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a>. Essa função substitui <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLAssociationDialog</strong></a><br/></td>
<td>Invoca a caixa de diálogo protocolo de URL não registrado. Essa caixa de diálogo permite que o usuário selecione um aplicativo a ser associado a um protocolo desconhecido anteriormente.<br/>
<blockquote>
[!Note]<br />
Windows XP SP2 ou posterior: não há mais suporte para essa função.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>WinExecError</strong></a><br/></td>
<td>Recupera o valor de erro gerado se a função <a href="/windows/win32/api/winbase/nf-winbase-winexec">WinExec</a> não pode executar um aplicativo especificado. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a><br/></td>
<td>Inicia a ajuda do Windows (Winhelp.exe) e passa dados adicionais que indicam a natureza da ajuda solicitada pelo aplicativo.<br/></td>
</tr>
</tbody>
</table>



 

 

 
