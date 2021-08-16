---
description: Esta seção descreve as estruturas Windows Shell.
title: Estruturas de shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fa046223ba3aa6a6e98d6e74f623aeaad9e85d3a10148bb688eb385c0e7c22fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675799"
---
# <a name="shell-structures"></a>Estruturas de shell

Esta seção descreve as estruturas Windows Shell.

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
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a><br/></td>
<td>Uma estrutura de tamanho variável que contém informações sobre um nome de arquivo de menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a><br/></td>
<td>Contém informações sobre um item de menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a><br/></td>
<td>Contém informações sobre uma mensagem da barra de aplicativos do sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a><br/></td>
<td>Fornece informações de categoria de aplicativo para Adicionar/Remover Programas Painel de Controle. A <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>estrutura APPCATEGORYINFOLIST</strong></a> é usada para criar uma lista completa de categorias para um editor de aplicativos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a><br/></td>
<td>Fornece uma lista de categorias de aplicativos com suporte de um editor de aplicativos para Adicionar/Remover Programas no Painel de Controle. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a><br/></td>
<td>Fornece informações sobre um aplicativo publicado para o utilitário add/remove programs Painel de Controle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a><br/></td>
<td>Define as informações <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>usadas por AssocCreateForClasses para</strong></a> recuperar uma interface <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> para uma determinada associação de arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a><br/></td>
<td>Contém informações sobre uma faixa de pastas. Essa estrutura é usada com os métodos <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand::GetBandInfoSFB</strong></a> e <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand::SetBandInfoSFB.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a><br/></td>
<td>Contém informações sobre um site de banda. Essa estrutura é usada com os métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite::GetBandSiteInfo</strong></a> <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>e IBandSite::SetBandSiteInfo.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a><br/></td>
<td>Contém membros protegidos da classe base. <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> define o estado do navegador e é usado com <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2::GetBaseBrowserData</strong></a> e <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2::P utBaseBrowserData</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a><br/></td>
<td>Define as coordenadas dos cantos superior esquerdo e inferior direito de um retângulo de borda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a><br/></td>
<td>Contém parâmetros para a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>função SHBrowseForFolder</strong></a> e recebe informações sobre a pasta selecionada pelo usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a><br/></td>
<td>Contém informações de categoria. Uma categoria de componente é um grupo de classes COM (Component Object Model) relacionadas logicamente que compartilham um CATID (identificador de categoria comum).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>Cida</strong></a><br/></td>
<td>Usado com o <a href="clipboard.md">formato CFSTR_SHELLIDLIST</a> área de transferência para transferir o ponteiro para uma PIDL (lista de identificadores de item) de um ou mais objetos de namespace do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a><br/></td>
<td>Define informações de coluna. Usado por membros da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a><br/></td>
<td>Contém informações necessárias para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> para invocar um comando de menu de atalho.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a><br/></td>
<td>Contém informações estendidas sobre um comando de menu de atalho. Essa estrutura é uma versão estendida <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>de CMINVOKECOMMANDINFO</strong></a> que permite o uso de valores Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a><br/></td>
<td>Usado genericamente para filtrar elementos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>Componente</strong></a><br/></td>
<td>Usado pelo Windows 2000 para manter informações sobre um componente. Essa estrutura substitui a <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>estrutura IE4COMPONENT.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a><br/></td>
<td>Contém as opções de item de área de trabalho.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a><br/></td>
<td>Contém informações sobre a posição e o tamanho de um componente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a><br/></td>
<td>Usado pelo Windows 2000 para manter informações sobre o estado de um componente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a><br/></td>
<td>Define a estrutura do item de conflito.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a><br/></td>
<td>Define a estrutura de informações de resultado do conflito.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a><br/></td>
<td>Contém informações de recurso e um valor definido pelo aplicativo para uma caixa de diálogo com suporte por um Painel de Controle aplicativo. A <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>função CPlApplet</strong></a> do aplicativo Painel de Controle retorna essas informações ao Painel de Controle em resposta a uma <a href="cpl-inquire.md"><strong>mensagem CPL_INQUIRE</strong></a> dados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a><br/></td>
<td>Contém detalhes sobre uma credencial.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a><br/></td>
<td>Descreve um único campo em uma credencial. Por exemplo, uma cadeia de caracteres ou uma imagem de usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a><br/></td>
<td>Usado com a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>função SHCreateShellFolderViewEx.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a><br/></td>
<td>Serve como o título de algumas das estruturas de dados extras usadas <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>por IShellLinkDataList.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a><br/></td>
<td>Contém informações de menu de contexto usadas <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>por SHCreateDefaultContextMenu</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a><br/></td>
<td>Usado por pastas delegadas no lugar de uma <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>estrutura ITEMIDLIST</strong></a> padrão.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a><br/></td>
<td>Contém informações detalhadas para um item de pasta do Shell. Usado com a <a href="sfvm-getdetailsof.md"><strong>notificação SFVM_GETDETAILSOF</strong></a> dados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a><br/></td>
<td>Contém argumentos adicionais usados <a href="dfm-invokecommandex.md"><strong>pelo DFM_INVOKECOMMANDEX</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a><br/></td>
<td>Recebe informações de versão específicas da DLL. Ele é usado com a <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>função DllGetVersion.</strong></a> <br/>
<blockquote>
[!Note]<br />
No lugar dessa estrutura, você pode usar a <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>estrutura DLLVERSIONINFO2.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a><br/></td>
<td>Recebe informações de versão específicas da DLL. Ele é usado com a <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>função DllGetVersion.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a><br/></td>
<td>Descreve a imagem e o texto que acompanha um objeto drop.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a><br/></td>
<td>Define o formato <a href="clipboard.md">CF_HDROP</a> área de transferência. Os dados a seguir são uma lista dupla terminada em nulo de nomes de arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a><br/></td>
<td>Contém um bloco de dados extra usado <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>por IShellLinkDataList.</strong></a> Ele contém a ID do instalador Windows link.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a><br/></td>
<td>Armazena informações sobre o estado do link do Shell. Essa estrutura é usada para seções de dados extras que são marcadas com EXP_PROPERTYSTORAGE_SIG.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a><br/></td>
<td>Mantém um bloco de dados extra usado pelo <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Ele contém informações especiais da pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a><br/></td>
<td>Mantém um bloco de dados extra usado pelo <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Ele mantém cadeias de caracteres de ambiente expansível para o ícone ou destino.<br/></td>
</tr>
<tr class="even">
<td><a href="ext-button.md"><strong>EXT_BUTTON</strong></a><br/></td>
<td>Contém informações sobre um botão que uma DLL de extensão do Gerenciador de arquivos está adicionando à barra de ferramentas do Gerenciador de arquivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a><br/></td>
<td>Usado por um objeto enumerador <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> para retornar informações sobre os objetos de pesquisa com suporte por um objeto de pasta do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a><br/></td>
<td>Contém a definição de formato da área de transferência para CFSTR_FILE_ATTRIBUTES_ARRAY.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>Descritor de</strong></a><br/></td>
<td>descreve as propriedades de um arquivo que está sendo copiado por meio da área de transferência durante uma operação de <a href="dragdrop.md">arrastar e soltar</a> do Microsoft ActiveX.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a><br/></td>
<td>Define o formato da área de transferência CF_FILEGROUPDESCRIPTOR.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a><br/></td>
<td>Contém informações sobre a unidade selecionada na janela do Active File Manager (a janela de diretório ou a janela de resultados da pesquisa).<br/></td>
</tr>
<tr class="even">
<td><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a><br/></td>
<td>Contém informações sobre um arquivo selecionado na janela do Gerenciador de arquivos ativo (a janela de diretório ou a janela de resultados da pesquisa).<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a><br/></td>
<td>Contém informações que o Gerenciador de arquivos usa para adicionar uma cadeia de caracteres de ajuda para um menu ou item de comando de barra de ferramentas.<br/></td>
</tr>
<tr class="even">
<td><a href="fms-load.md"><strong>FMS_LOAD</strong></a><br/></td>
<td>Contém informações que o Gerenciador de arquivos usa para adicionar um menu personalizado fornecido por uma DLL de extensão do Gerenciador de arquivos. A estrutura também fornece um valor delta que a DLL de extensão pode usar para manipular o menu personalizado depois que o Gerenciador de arquivos tiver carregado o menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a><br/></td>
<td>Contém informações sobre os botões personalizados a serem adicionados à barra de ferramentas do Gerenciador de arquivos. Os botões são fornecidos por uma DLL de extensão do Gerenciador de arquivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a><br/></td>
<td>Contém informações de exibição de pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a><br/></td>
<td>Contém informações que o Visualizador de arquivos usa para exibir um arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a><br/></td>
<td>Contém informações sobre um item para o qual foi solicitada ajuda contextual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a><br/></td>
<td>Contém o tamanho e a posição de uma janela de ajuda primária ou secundária. Um aplicativo pode definir essas informações chamando a função <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> com o valor HELP_SETWINPOS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a><br/></td>
<td>Usado pelo Microsoft Internet Explorer 4,0 e pelo Microsoft Internet Explorer 4, 1 para manter informações sobre um componente. com o Windows 2000, ele é substituído pela estrutura do <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>componente</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDlist</strong></a><br/></td>
<td>Contém uma lista de identificadores de item.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ESPAÇAmento de linhas</strong></a><br/></td>
<td>Armazena as dimensões dos dois tamanhos possíveis de espaçamento de ícone que estão disponíveis para exibição: pequeno e grande. Usado por <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView:: GetItemSpacing</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a><br/></td>
<td>Define as especificidades de uma pasta conhecida.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a><br/></td>
<td>Define os atributos de uma fonte.<br/></td>
</tr>
<tr class="odd">
<td><a href="mruinfo.md"><strong>MRUINFO</strong></a><br/></td>
<td>Contém informações que definem uma nova lista MRU (usada mais recentemente). Usado por <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a><br/></td>
<td>especifica uma palavra-chave a ser pesquisada e a tabela de palavras-chave a ser pesquisada Windows ajuda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a><br/></td>
<td>Contém informações que descrevem um endereço de rede.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a><br/></td>
<td>Descreve um endereço de rede.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a><br/></td>
<td>Contém informações de recursos e um valor definido pelo aplicativo para uma caixa de diálogo com suporte por um aplicativo do painel de controle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a><br/></td>
<td>Contém informações que o sistema precisa para exibir notificações na área de notificação. Usado pelo <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a><br/></td>
<td>Contém informações usadas pelo <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> para identificar o ícone para o qual recuperar o retângulo delimitador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a><br/></td>
<td>Define o formato da área de transferência CF_NETRESOURCE.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a><br/></td>
<td>Estrutura personalizada de desenho usada pelos métodos <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a><br/></td>
<td>Mantém um bloco de dados extra usado pelo <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Ele contém propriedades do console.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a><br/></td>
<td>Mantém um bloco de dados extra usado pelo <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Ele contém a página de código do console.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a><br/></td>
<td>Identifica uma determinada folha de propriedades nas páginas de propriedades de uma impressora e se essa folha de propriedades deve ser modal. Opcionalmente, usada com a função <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a><br/></td>
<td>Armazena informações para a função <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>SOBREPÕE</strong></a><br/></td>
<td>Contém informações usadas em e/s (entrada/saída) assíncrona (sobreposta).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a><br/></td>
<td>Usado pela função <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>parseURL</strong></a> para retornar a URL analisada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a><br/></td>
<td>Especifica a pasta de destino de um atalho de pasta e seus atributos. Essa estrutura é usada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3:: GetFolderTargetInfo</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: InitializeEx</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a><br/></td>
<td>Estrutura da tabela de aceleração. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame:: GetWindowContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO</strong></a><br/></td>
<td>Contém informações usadas ao carregar ou descarregar um perfil de usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a><br/></td>
<td>Fornece informações sobre um aplicativo publicado de um editor de aplicativos para <strong>Adicionar ou remover programas</strong> no painel de controle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a><br/></td>
<td>contém informações para mesclar itens de menu em menus Windows Explorer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a><br/></td>
<td>Usado pela função <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> para descrever uma única interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a><br/></td>
<td>Um intervalo de memória de tipo arbitrário que representa uma estrutura <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> serializada. Os programas não devem inspecionar o conteúdo de <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>um SERIALIZEDPROPERTYVALUE</strong></a>; Em vez disso, eles devem manipulá-lo com as funções <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> e <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a><br/></td>
<td>Essa estrutura é usada com a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>função SHCreateShellFolderView.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a><br/></td>
<td>Armazena informações de posição para um item. Usado com mensagens <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a><br/></td>
<td>Contém o nome de um arquivo de Ajuda HTML e um tópico nesse arquivo. Usado com a <a href="sfvm-gethelptopic.md"><strong>notificação SFVM_GETHELPTOPIC</strong></a> dados. Essa estrutura requer cadeias de caracteres Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a><br/></td>
<td>Contém os detalhes de uma página a ser adicionada à folha <strong>Propriedades de um</strong> objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a><br/></td>
<td>Contém dados usados por <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> para identificar um item – neste caso, como <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>um IShellItem</strong></a>– e o processo ao qual ele está associado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a><br/></td>
<td>Contém dados usados por <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> para identificar um item – neste caso, por um PIDL absoluto – e o processo ao qual ele está associado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a><br/></td>
<td>Contém dados usados por <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> para identificar um item, nesse caso, por meio de <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>um IShellLink</strong></a>e o processo ao qual ele está associado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a><br/></td>
<td>Contém e recebe informações para notificações de alteração. Essa estrutura é usada com a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>função SHChangeNotifyRegister</strong></a> e a <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> notificação.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a><br/></td>
<td>Contém informações que identificam um arquivo específico. Ele é usado por <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> ao solicitar dados para um arquivo específico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a><br/></td>
<td>Especifica o identificador FMTID/PID de uma coluna que será exibida pela exibição Windows Detalhes do Explorer. <br/>
<blockquote>
[!Note]<br />
A partir Windows Vista, <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> é considerado um formulário herdado e não deve ser usado. Em seu lugar, use a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>estrutura PROPERTYKEY.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a><br/></td>
<td>Contém informações sobre as propriedades de uma coluna. Ele é usado por <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider::GetColumnInfo.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a><br/></td>
<td>Passa informações de inicialização <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>para IColumnProvider::Initialize</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a><br/></td>
<td>Recebe dados de item em resposta a uma chamada para <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a><br/></td>
<td>Contém as informações necessárias para criar uma imagem de arrastar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a><br/></td>
<td>Define o recurso de item shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a><br/></td>
<td>Relata informações detalhadas sobre um item em uma pasta shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a><br/></td>
<td>Contém informações usadas <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>pelo ShellExecuteEx.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a><br/></td>
<td>Contém um conjunto de sinalizadores que indicam as configurações atuais do Shell. Essa estrutura é usada com a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>função SHGetSettings.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a><br/></td>
<td>Contém configurações para o estado do Shell. Essa estrutura é usada com a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>função SHGetSetSettings.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a><br/></td>
<td>Contém informações sobre um objeto de arquivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a><br/></td>
<td>Contém informações que a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>função SHFileOperation</strong></a> usa para executar operações de arquivo. <br/>
<blockquote>
[!Note]<br />
A partir Windows Vista, o uso da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> é recomendado nessa função.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a><br/></td>
<td>Contém configurações de pasta personalizadas. Essa estrutura é usada com a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>função SHGetSetFolderCustomSettings.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>ADEMID</strong></a><br/></td>
<td>Define um identificador de item.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a><br/></td>
<td>Contém os nomes de caminho novos e antigos para cada arquivo que foi movido, copiado ou renomeado pela <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>função SHFileOperation.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a><br/></td>
<td>Contém as informações de tamanho e contagem de itens recuperadas pela <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>função SHQueryRecycleBin.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a><br/></td>
<td>Recebe informações usadas para recuperar um ícone do Shell de estoque. Essa estrutura é usada em uma <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>chamada SHGetStockIconInfo</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a><br/></td>
<td>Fornece informações de aplicativo <strong>especializadas para Adicionar/Remover Programas</strong> no Painel de Controle. Essa estrutura não é aplicável a aplicativos publicados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a><br/></td>
<td>Contém informações sobre a notificação de alteração. Ele é usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback::CallbackSM.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a><br/></td>
<td>Contém informações de uma faixa de menus.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a><br/></td>
<td>Contém informações sobre um item de uma faixa de menus.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a><br/></td>
<td>Contém informações sobre uma atualização de software.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a><br/></td>
<td>Armazena informações sobre como classificar uma coluna exibida na exibição de pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a><br/></td>
<td>Contém cadeias de caracteres retornadas dos métodos de interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a><br/></td>
<td>Contém os parâmetros para o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>método IShellView2::CreateViewWindow2.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a><br/></td>
<td>Define um manipulador para uma sincronização agendada. Usado com <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule::AddItem.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a><br/></td>
<td>Descreve a estrutura de informações da ID de conflito.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a><br/></td>
<td>Fornece informações sobre o manipulador para uso no <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>método ISyncMgrSynchronize::GetHandlerInfo.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a><br/></td>
<td>Fornece informações sobre os itens que estão sendo enumerados pela interface <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a><br/></td>
<td>Fornece informações de erro para uso <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>no método ISyncMgrSynchronizeCallback::LogError.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a><br/></td>
<td>Fornece informações de status enquanto uma sincronização está em andamento. Essa estrutura é usada com o método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback::P rogress</strong></a> e corresponde a um único item de sincronização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a><br/></td>
<td>Usado com a notificação de <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> para especificar o número de botões a serem adicionados à barra de ferramentas, bem como como eles são adicionados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a><br/></td>
<td>Usado por métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> para definir botões usados em uma barra de ferramentas inserida na representação em miniatura de uma janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a><br/></td>
<td>Contém as opções de exibição de papel de parede. Usado com membros da interface <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a><br/></td>
<td>Armazena dados de janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a><br/></td>
<td>Especifica o contexto de uma extração de miniatura. Usado por <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings:: SetContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a><br/></td>
<td>Valores usados por <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache:: GetThumbnail</strong></a> para especificar opções para a extração e a exibição da imagem em miniatura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a><br/></td>
<td>Contém um identificador exclusivo para uma miniatura no cache de miniaturas do sistema.<br/></td>
</tr>
</tbody>
</table>



 

 

 
