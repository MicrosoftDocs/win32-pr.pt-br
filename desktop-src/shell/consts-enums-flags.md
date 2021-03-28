---
description: Esta seção descreve as constantes, enumerações e sinalizadores do shell do Windows.
title: Constantes, enumerações e sinalizadores do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 638beaa7-a065-4ab3-8eb5-286a306a8f24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2070ef1acc37262a526186862f46afa002c47343
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172393"
---
# <a name="shell-constants-enumerations-and-flags"></a>Constantes, enumerações e sinalizadores do Shell

Esta seção descreve as constantes, enumerações e sinalizadores do shell do Windows.

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
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svgio"><strong>_SVGIO</strong></a><br/></td>
<td>Usado com os métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items"><strong>IFolderView:: Items</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount"><strong>IFolderView:: ItemCount</strong></a>e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject"><strong>IShellView:: getitemobject</strong></a> para restringir ou controlar os itens em suas coleções.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svsif"><strong>_SVSIF</strong></a><br/></td>
<td>Indica sinalizadores usados por <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> para especificar um tipo de seleção a ser aplicado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appactionflags"><strong>APPACTIONFLAGS</strong></a><br/></td>
<td>Especifica as ações de gerenciamento de aplicativos com suporte por um editor de aplicativos. Esses sinalizadores são bitmasks passados para <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getpossibleactions"><strong>IShellApp:: GetPossibleActions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appinfodataflags"><strong>APPINFODATAFLAGS</strong></a><br/></td>
<td>Especifica as informações do aplicativo a serem retornadas de <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getappinfo"><strong>IShellApp:: GetAppInfo</strong></a>. Esses sinalizadores são bitmasks usadas no membro <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>dwMask</strong></a> da estrutura <strong>APPINFODATA</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_orientation"><strong>APPLICATION_VIEW_ORIENTATION</strong></a><br/></td>
<td>Define o conjunto de modos de orientação de exibição para uma janela (exibição do aplicativo). Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: GetApplicationViewOrientation</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: SetApplicationViewOrientation</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_size_preference"><strong>APPLICATION_VIEW_SIZE_PREFERENCE</strong></a><br/></td>
<td>Define o conjunto de preferências de tamanho de janela geral (exibição de aplicativo) possíveis. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchsourceviewsizepreference-getsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference:: GetSourceViewSizePreference</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference"><strong>ILaunchTargetViewSizePreference:: GetTargetViewSizePreference</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_state"><strong>APPLICATION_VIEW_STATE</strong></a><br/></td>
<td>Indica o estado de exibição atual de um aplicativo da Windows Store. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings:: SetApplicationViewState</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings:: IsApplicationViewStateSupported</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocdata"><strong>ASSOCDATA</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata"><strong>IQueryAssociations:: GetData</strong></a> para definir o tipo de dados que será retornado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/shell/assocf_str"><strong>ASSOCF</strong></a><br/></td>
<td>Fornece informações para os métodos de interface <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>ASSOCIATIONLEVEL</strong></a><br/></td>
<td>Especifica a origem da associação padrão para uma extensão de nome de arquivo. Usado por métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>ASSOCIATIONTYPE</strong></a><br/></td>
<td>Especifica o tipo de associação para um aplicativo. Usado por métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assockey"><strong>ASSOCKEY</strong></a><br/></td>
<td>Especifica o tipo de chave a ser retornado por <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getkey"><strong>IQueryAssociations:: GetKey</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr"><strong>ASSOCSTR</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring"><strong>IQueryAssociations:: GetString</strong></a> para definir o tipo de cadeia de caracteres que será retornado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action"><strong>ATTACHMENT_ACTION</strong></a><br/></td>
<td>Fornece um conjunto de sinalizadores a serem usados com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute::P</strong></a> executar para indicar a ação a ser executada mediante a confirmação do usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt"><strong>ATTACHMENT_PROMPT</strong></a><br/></td>
<td>Fornece um conjunto de sinalizadores a serem usados com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute::P</strong></a> em seguida para indicar o tipo de interface do usuário de prompt a ser exibido.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-autocompletelistoptions"><strong>AUTOCOMPLETELISTOPTIONS</strong></a><br/></td>
<td>Especifica quais objetos são enumerados para listas de preenchimento automático.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shldisp/ne-shldisp-autocompleteoptions"><strong>Preenchimento automático</strong></a><br/></td>
<td>Especifica os valores usados por <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-getoptions"><strong>IAutoComplete2:: getoptions</strong></a> e <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions"><strong>IAutoComplete2:: SetOptions</strong></a> para as opções em torno de preenchimento automático.<br/></td>
</tr>
<tr class="even">
<td><a href="str-constants.md"><strong>Associar chaves de cadeia de caracteres de contexto</strong></a><br/></td>
<td>Um conjunto de chaves de cadeia de caracteres que são usadas com o método <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> para especificar um contexto de associação.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shdeprecated/ne-shdeprecated-bnstate"><strong>BNSTATE</strong></a><br/></td>
<td>Preterido. Usado por <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-setnavigatestate"><strong>IBrowserService:: Setnavigatestate</strong></a> e <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-getnavigatestate"><strong>IBrowserService:: getnavigatestate</strong></a> para especificar Estados de navegação.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-_browserframeoptions"><strong>BROWSERFRAMEOPTIONS</strong></a><br/></td>
<td>Usado com o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibrowserframeoptions-getframeoptions"><strong>IBrowserFrameOptions:: Getframeoptions</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags"><strong>CATEGORYINFO_FLAGS</strong></a><br/></td>
<td>Fornece um conjunto de sinalizadores para uso com a estrutura de <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags"><strong>CATSORT_FLAGS</strong></a><br/></td>
<td>Especifica métodos para classificar dados de categoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)"><strong>CDCONTROLSTATE</strong></a><br/></td>
<td>Especifica os valores que indicam se um controle está visível e habilitado. Usado por membros da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags"><strong>CM_ENUM_FLAGS</strong></a><br/></td>
<td>Usado por membros da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> para especificar qual conjunto de colunas está sendo solicitado, todos ou apenas os visíveis no momento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_mask"><strong>CM_MASK</strong></a><br/></td>
<td>Indica quais valores na estrutura de <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> devem ser definidos durante chamadas para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo"><strong>IColumnManager:: SetColumnInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_set_width_value"><strong>CM_SET_WIDTH_VALUE</strong></a><br/></td>
<td>Especifica valores de largura em pixels e inclui suporte especial para padrão e AutoSize. Usado por membros da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> por meio da estrutura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_state"><strong>CM_STATE</strong></a><br/></td>
<td>Especifica os valores de estado da coluna. Usado por membros da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> por meio da estrutura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_account_options"><strong>CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS</strong></a><br/></td>
<td>Indica o tipo de credencial que um provedor de credenciais deve retornar para associar ao &quot; outro &quot; bloco de usuário. Usado pelo <a href="/windows/desktop/api/CredentialProvider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions"><strong>ICredentialProviderUserArray_GetAccountOptions</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_credential_field_options"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</strong></a><br/></td>
<td>Fornece opções de personalização para um único campo em uma interface de usuário de logon ou credencial.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state"><strong>CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</strong></a><br/></td>
<td>Descreve o estado de um campo e como ele pode interagir com ele. Os campos podem ser exibidos por um provedor de credenciais em uma variedade de diferentes Estados interativos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_state"><strong>CREDENTIAL_PROVIDER_FIELD_STATE</strong></a><br/></td>
<td>Especifica o estado de um único campo na interface do usuário da credencial.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_type"><strong>CREDENTIAL_PROVIDER_FIELD_TYPE</strong></a><br/></td>
<td>Especifica um tipo de campo de credencial. Usado pelo <a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_get_serialization_response"><strong>CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE</strong></a><br/></td>
<td>Descreve a resposta quando um provedor de credenciais tenta serializar credenciais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_status_icon"><strong>CREDENTIAL_PROVIDER_STATUS_ICON</strong></a><br/></td>
<td>Indica qual ícone de status deve ser exibido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_usage_scenario"><strong>CREDENTIAL_PROVIDER_USAGE_SCENARIO</strong></a><br/></td>
<td>Declara os cenários em que há suporte para um provedor de credenciais. Um cenário de uso do provedor de credenciais (CPUS) permite que o provedor de credenciais forneça comportamento de enumeração distinto e configuração de campo de interface do usuário entre cenários.<br/></td>
</tr>
<tr class="even">
<td><a href="csidl.md"><strong>CSIDl</strong></a><br/></td>
<td><blockquote>
<p><b>Observação: </b> A partir do Windows Vista, esses valores foram substituídos por valores de <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> . Consulte esse tópico para obter uma lista das novas constantes e seus valores CSIDl correspondentes. Para sua conveniência, os valores de <strong>KNOWNFOLDERID</strong> correspondentes também são indicados aqui para cada valor de CSIDL.</p>
<p>Há suporte para o sistema CSIDl no Windows Vista por motivos de compatibilidade. No entanto, o novo desenvolvimento deve usar valores de <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> em vez de valores de CSIDL.<br/></p>
</blockquote>
<br/> Os valores CSIDl (lista de ID de item especial de constante) fornecem uma maneira exclusiva independente do sistema de identificar pastas especiais usadas frequentemente por aplicativos, mas que podem não ter o mesmo nome ou local em um determinado sistema. Por exemplo, a pasta do sistema pode ser &quot; C:\Windows &quot; em um sistema e &quot; C:\Winnt &quot; em outro. Essas constantes são definidas em shlobj. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="ctf.md"><strong>Sinalizadores de CTF</strong></a><br/></td>
<td>Sinalizadores que controlam o comportamento da função de chamada. Usado por <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread"><strong>SHCreateThread</strong></a> e <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadwithhandle"><strong>SHCreateThreadWithHandle</strong></a>. Nessas funções, esses valores são definidos como sendo do tipo SHCT_FLAGS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags"><strong>DATAOBJ_GET_ITEM_FLAGS</strong></a><br/></td>
<td>Valores usados pela função <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a> para especificar opções relacionadas ao processamento do objeto de origem.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-tagdeskbandcid"><strong>Sinalizadores de comando DBID</strong></a><br/></td>
<td>Essas IDs de comando podem ser enviadas para o contêiner do objeto de banda com <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec"><strong>IOleCommandTarget:: exec</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id"><strong>DEF_SHARE_ID</strong></a><br/></td>
<td>Valores que especificam a pasta que está sendo acionada por métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype"><strong>DEFAULTSAVEFOLDERTYPE</strong></a><br/></td>
<td>Especifica o local de salvamento padrão.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-default_folder_menu_restrictions"><strong>DEFAULT_FOLDER_MENU_RESTRICTIONS</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position"><strong>DESKTOP_WALLPAPER_POSITION</strong></a><br/></td>
<td>Especifica como o papel de parede da área de trabalho deve ser exibido.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ne-shtypes-device_scale_factor"><strong>DEVICE_SCALE_FACTOR</strong></a><br/></td>
<td>Indica um fator de escala de dispositivo falsificado, como uma porcentagem. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings:: SetApplicationViewState</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings:: IsApplicationViewStateSupported</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-display_device_type"><strong>DISPLAY_DEVICE_TYPE</strong></a><br/></td>
<td>Indica se o dispositivo é um tipo de tela primária ou de imersão.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype"><strong>DROPIMAGETYPE</strong></a><br/></td>
<td>Valores usados com a estrutura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a> para especificar a imagem de remoção.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a><br/></td>
<td>Os valores de <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a> representam o estado de comando de um item de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags"><strong>EXPLORER_BROWSER_FILL_FLAGS</strong></a><br/></td>
<td>Esses sinalizadores são usados com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject"><strong>IExplorerBrowser:: FillFromObject</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options"><strong>EXPLORER_BROWSER_OPTIONS</strong></a><br/></td>
<td>Esses sinalizadores são usados com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions"><strong>IExplorerBrowser:: getoptions</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions"><strong>IExplorerBrowser:: SetOptions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_explorerpanestate"><strong>EXPLORERPANESTATE</strong></a><br/></td>
<td>Indique os sinalizadores usados por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate"><strong>IExplorerPaneVisibility:: Getpanestate</strong></a> para obter o estado atual do painel do Windows Explorer fornecido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap"><strong>FDAP</strong></a><br/></td>
<td>Especifica o posicionamento da lista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response"><strong>FDE_OVERWRITE_RESPONSE</strong></a><br/></td>
<td>Especifica os valores usados pelo método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite"><strong>IFileDialogEvents:: onoverwrite</strong></a> para indicar a resposta de um aplicativo a uma solicitação de substituição durante uma operação de salvamento usando a caixa de diálogo arquivo comum.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response"><strong>FDE_SHAREVIOLATION_RESPONSE</strong></a><br/></td>
<td>Especifica os valores usados pelo método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onshareviolation"><strong>IFileDialogEvents:: OnShareViolation</strong></a> para indicar a resposta de um aplicativo a uma violação de compartilhamento que ocorre quando um arquivo é aberto ou salvo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fffp_mode"><strong>FFFP_MODE</strong></a><br/></td>
<td>Descreve critérios de correspondência. Usado por métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type"><strong>FILE_USAGE_TYPE</strong></a><br/></td>
<td>Constantes usadas por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getusage"><strong>IFileIsInUse:: getusage</strong></a> para indicar como um arquivo em uso está sendo usado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions"><strong>FILEOPENDIALOGOPTIONS</strong></a><br/></td>
<td>Define o conjunto de opções disponíveis para uma caixa de diálogo abrir ou salvar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a><br/></td>
<td>Indica as constantes <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> que são usadas no valor EditFlags de uma chave de registro <a href="fa-progids.md">ProgID</a> de associação de arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a><br/></td>
<td>Usado pelos métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-getmode"><strong>IObjectWithFolderEnumMode:: GetMode</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-setmode"><strong>IObjectWithFolderEnumMode:: setmode</strong></a> para obter e definir os modos de exibição para as pastas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags"><strong>FOLDERFLAGS</strong></a><br/></td>
<td>Um conjunto de sinalizadores que especificam opções de exibição de pasta. Os sinalizadores são independentes um do outro e podem ser usados em qualquer combinação.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode"><strong>FOLDERLOGICALVIEWMODE</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderviewsettings-getviewmode"><strong>IFolderViewSettings:: Getviewmode</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode"><strong>ISearchFolderItemFactory:: SetFolderLogicalViewMode</strong></a> para descrever o modo de exibição.<br/></td>
</tr>
<tr class="odd">
<td><a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a><br/></td>
<td>Os valores de <a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a> representam um modelo de exibição aplicado a uma pasta, geralmente com base em seu uso e conteúdo pretendidos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode"><strong>FOLDERVIEWMODE</strong></a><br/></td>
<td>Especifica o tipo de exibição de pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-folderviewoptions"><strong>FOLDERVIEWOPTIONS</strong></a><br/></td>
<td>Usado por métodos da interface <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a> para ativar as opções do Windows Vista que não têm suporte por padrão no Windows 7 e sistemas posteriores, bem como desativando novas opções do Windows 7.<br/></td>
</tr>
<tr class="even">
<td><a href="iactivedesktop-flags.md"><strong>Sinalizadores de IActiveDesktop</strong></a><br/></td>
<td>Esta seção descreve os sinalizadores usados pelos métodos de interface <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-ieshortcutflags"><strong>IESHORTCUTFLAGS</strong></a><br/></td>
<td>Especifica como um atalho deve ser tratado pelo navegador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category"><strong>KF_CATEGORY</strong></a><br/></td>
<td>Valor que representa uma categoria pela qual uma pasta registrada com o sistema de pastas conhecido pode ser classificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags"><strong>KF_DEFINITION_FLAGS</strong></a><br/></td>
<td>Sinalizadores que especificam determinados comportamentos de pasta conhecidos. Usado com a estrutura de <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags"><strong>KF_REDIRECT_FLAGS</strong></a><br/></td>
<td>Sinalizadores usados por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect"><strong>IKnownFolderManager:: Redirect</strong></a> para especificar detalhes de um redirecionamento de pasta conhecido, como permissões e propriedade para a pasta redirecionada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities"><strong>KF_REDIRECTION_CAPABILITIES</strong></a><br/></td>
<td>Sinalizadores que especificam os recursos de redirecionamento atuais de uma pasta conhecida. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities"><strong>IKnownFolder:: GetRedirectionCapabilities</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag"><strong>KNOWN_FOLDER_FLAG</strong></a><br/></td>
<td>Especifique opções de recuperação especiais para pastas conhecidas. Esses valores substituem os valores de <a href="csidl.md"><strong>CSIDL</strong></a> , que têm significados paralelos.<br/></td>
</tr>
<tr class="odd">
<td><a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a><br/></td>
<td>As constantes <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> representam GUIDs que identificam as pastas padrão registradas com o sistema como <a href="known-folders.md">pastas conhecidas</a>. Essas pastas são instaladas com o Windows Vista e sistemas operacionais posteriores, e um computador terá apenas pastas apropriadas para ele instalado. Para obter descrições dessas pastas, consulte <a href="csidl.md"><strong>CSIDL</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter"><strong>LIBRARYFOLDERFILTER</strong></a><br/></td>
<td>Define opções para filtrar itens de pasta. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions"><strong>LIBRARYMANAGEDIALOGOPTIONS</strong></a><br/></td>
<td>Usado pelo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui"><strong>SHShowManageLibraryUI</strong></a> para definir opções para tratar uma colisão de nomes ao salvar uma biblioteca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags"><strong>LIBRARYOPTIONFLAGS</strong></a><br/></td>
<td>Especifica as opções de biblioteca.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags"><strong>LIBRARYSAVEFLAGS</strong></a><br/></td>
<td>Especifica as opções para tratar uma colisão de nome ao salvar uma biblioteca. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-mimeassociationdialog_in_flags"><strong>MIMEASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>Usado com a função <a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a> para determinar como ela é executada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility"><strong>MONITOR_APP_VISIBILITY</strong></a><br/></td>
<td>Especifica se uma exibição está mostrando janelas da área de trabalho em vez de aplicativos da Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="mp-popupflags.md"><strong>MP_POPUPFLAGS constantes</strong></a><br/></td>
<td>Representam opções disponíveis ao exibir um menu pop-up.<br/></td>
</tr>
<tr class="odd">
<td><a href="net-string.md"><strong>NET_STRING</strong></a><br/></td>
<td>Representa tipos de endereço de rede. Use uma ou mais (como uma combinação de bits) das constantes a seguir para criar uma máscara de endereço de rede a ser usada com a macro <a href="/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype"><strong>NetAddr_SetAllowType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nstcfoldercapabilities"><strong>NSTCFOLDERCAPABILITIES</strong></a><br/></td>
<td>Especifica o estado de um item de árvore. Esses valores são usados por métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate"><strong>NSTCITEMSTATE</strong></a><br/></td>
<td>Especifica o estado de um item de árvore. Esses valores são usados por métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcstyle"><strong>NSTCSTYLE</strong></a><br/></td>
<td>Descreve as características de um determinado controle de árvore de namespace.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-nstcstyle2"><strong>NSTCSTYLE2</strong></a><br/></td>
<td>Usado pelos métodos de <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a> para especificar os estilos de exibição estendidos em uma árvore de namespace de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf"><strong>NWMF</strong></a><br/></td>
<td>Sinalizadores usados por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow"><strong>INewWindowManager:: EvaluateNewWindow</strong></a>. Esses valores são fatores na decisão de se uma janela pop-up deve ser exibida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-package_execution_state"><strong>PACKAGE_EXECUTION_STATE</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-perceived"><strong>VISTAS</strong></a><br/></td>
<td>Especifica o tipo percebido de um arquivo. Esse conjunto de constantes é usado na função <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype"><strong>AssocGetPerceivedType</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-pubappinfoflags"><strong>PUBAPPINFOFLAGS</strong></a><br/></td>
<td>Especifica quais membros na estrutura <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a> são válidos. Esses sinalizadores são bitmasks definidos no membro <strong>dwMask</strong> e passados para <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo"><strong>IPublishedApp:: GetPublishedAppInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-query_user_notification_state"><strong>QUERY_USER_NOTIFICATION_STATE</strong></a><br/></td>
<td>Especifica o estado do computador para o usuário atual em relação ao propriety de enviar uma notificação. Usado por <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="hkey-type.md"><strong>Tipos de dados do registro</strong></a><br/></td>
<td>Esses tipos de dados podem ser usados para especificar o tipo de um valor de registro.<br/></td>
</tr>
<tr class="even">
<td><a href="regsam.md"><strong>REGSAM</strong></a><br/></td>
<td>Um tipo de dados usado para especificar os atributos de acesso de segurança no registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions"><strong>Quanto</strong></a><br/></td>
<td>Esses sinalizadores são usados com a função <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>SHRestricted</strong></a> . <strong>SHRestricted</strong> é usado para determinar se uma política de administrador especificada está em vigor. Em muitos casos, os aplicativos precisam modificar determinados comportamentos para atender às políticas aplicadas pelos administradores do sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-scale_change_flags"><strong>SCALE_CHANGE_FLAGS</strong></a><br/></td>
<td>Sinalizadores que são usados para indicar a alteração de dimensionamento que ocorreu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status"><strong>SCNRT_STATUS</strong></a><br/></td>
<td>Indica se é para habilitar ou desabilitar o registro assíncrono e o cancelamento de registro para <a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-tagsfbs_flags"><strong>SFBS_FLAGS</strong></a><br/></td>
<td>Especifica como a função <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a> deve tratar o arredondamento de dígitos não exibidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="sfgao.md"><strong>SFGAO</strong></a><br/></td>
<td>Atributos que podem ser recuperados em um item (arquivo ou pasta) ou conjunto de itens.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shard"><strong>FRAGMENTOS</strong></a><br/></td>
<td>Indica a interpretação dos dados passados por <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> em seu parâmetro <em>VP</em> para identificar o item cujas estatísticas de uso estão sendo controladas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role"><strong>SHARE_ROLE</strong></a><br/></td>
<td>Especifica as permissões de acesso atribuídas aos <strong>usuários</strong> ou à pasta <strong>pública</strong> . Usado em <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-createshare"><strong>createshare</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-getsharepermissions"><strong>GetSharePermissions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-shcolstate"><strong>SHCOLSTATE</strong></a><br/></td>
<td>Descreve como uma propriedade deve ser tratada. Esses valores são definidos em Shtypes. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shcontf"><strong>SHCONTF</strong></a><br/></td>
<td>Determina os tipos de itens incluídos em uma enumeração. Esses valores são usados com o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: EnumObjects</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags"><strong>SHELL_LINK_DATA_FLAGS</strong></a><br/></td>
<td>Especifica as configurações de opção. Usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags"><strong>IShellLinkDataList:: GetFlags</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-setflags"><strong>IShellLinkDataList:: SetFlags</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a><br/></td>
<td>Identifica o tipo de componente da interface do usuário que é necessário no Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions"><strong>ShellFolderViewOptions</strong></a><br/></td>
<td>Especifica as opções de exibição retornadas pela propriedade <a href="shellfolderview-viewoptions.md"><strong>ViewOptions</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants"><strong>ShellSpecialFolderConstants</strong></a><br/></td>
<td>Especifica valores exclusivos independentes do sistema que identificam pastas especiais. Essas pastas são usadas com frequência por aplicativos, mas que podem não ter o mesmo nome ou local em um determinado sistema. Por exemplo, a pasta do sistema pode ser &quot; C:\Windows &quot; em um sistema e &quot; C:\Winnt &quot; em outro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ExDisp/ne-exdisp-shellwindowfindwindowoptions"><strong>ShellWindowFindWindowOptions</strong></a><br/></td>
<td>Especifica as opções para localizar a janela na coleção de janelas do Shell. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/ne-exdisp-shellwindowtypeconstants"><strong>ShellWindowTypeConstants</strong></a><br/></td>
<td>Especifica os tipos de janelas do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shgdnf"><strong>SHGDNF</strong></a><br/></td>
<td>Define os valores usados com os métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof"><strong>IShellFolder:: SetNameOf</strong></a> para especificar o tipo de nome de arquivo ou pasta usado por esses métodos. <br/>
<blockquote>
<b>Observação</b>:<br />
Antes do Windows 7, esses valores eram empacotados como a enumeração SHGNO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shglobalcounter"><strong>SHGLOBALCOUNTER</strong></a><br/></td>
<td>Identificadores para vários contadores globais ou variáveis compartilhadas. Cada contador global pode ser incrementado ou diminuído usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterincrement"><strong>SHGlobalCounterIncrement</strong></a> e <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterdecrement"><strong>SHGlobalCounterDecrement</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregdel_flags"><strong>SHREGDEL_FLAGS</strong></a><br/></td>
<td>Fornece um conjunto de valores que indicam de qual chave base um item será excluído.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregenum_flags"><strong>SHREGENUM_FLAGS</strong></a><br/></td>
<td>Fornece um conjunto de valores que indicam a chave de base que será usada para uma enumeração.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-shstockiconid"><strong>SHSTOCKICONID</strong></a><br/></td>
<td>Usado pelo <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a> para identificar o ícone do sistema de ações a ser recuperado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_sichintf"><strong>SICHINTF</strong></a><br/></td>
<td>Usado para determinar como comparar dois itens de Shell. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-compare"><strong>IShellItem:: Compare</strong></a> usa esse tipo enumerado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn"><strong>SIGDN</strong></a><br/></td>
<td>Solicita o formato do nome de exibição de um item para recuperar por meio de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname"><strong>IShellItem:: GetDisplayName</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction"><strong>SPACTION</strong></a><br/></td>
<td>Descreve uma ação que está sendo executada que requer o progresso a ser mostrado ao usuário usando uma interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_spbeginf"><strong>SPBEGINF</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin"><strong>IActionProgress:: Begin</strong></a>, essas constantes especificam determinadas operações de interface do usuário que devem ser habilitadas ou desabilitadas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext"><strong>TEXTO</strong></a><br/></td>
<td>Especifica o tipo de texto descritivo que está sendo fornecido para uma interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="srrf.md"><strong>SRRF</strong></a><br/></td>
<td>Sinalizadores que restringem os dados a serem definidos ou retornados.<br/></td>
</tr>
<tr class="odd">
<td><a href="ssf-constants.md"><strong>Constantes SSF</strong></a><br/></td>
<td>Usado pela função <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> para especificar quais membros de sua estrutura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>shellstate</strong></a> devem ser definidos ou recuperados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag"><strong>STPFLAG</strong></a><br/></td>
<td>Usado pelo método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties"><strong>ITaskbarList4:: SetTabProperties</strong></a> para especificar as propriedades da guia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status"><strong>SVUIA_STATUS</strong></a><br/></td>
<td>Usado com o método <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview"><strong>IBrowserService2:: _UIActivateView</strong></a> para definir o estado de uma exibição de navegador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_cancel_request"><strong>SYNCMGR_CANCEL_REQUEST</strong></a><br/></td>
<td>Descreve uma solicitação pelo usuário para cancelar uma sincronização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_conflict_item_type"><strong>SYNCMGR_CONFLICT_ITEM_TYPE</strong></a><br/></td>
<td>Descreve o tipo de item de conflito.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_control_flags"><strong>SYNCMGR_CONTROL_FLAGS</strong></a><br/></td>
<td>Especifica como uma operação solicitada em determinados métodos de <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> deve ser executada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_flags"><strong>SYNCMGR_EVENT_FLAGS</strong></a><br/></td>
<td>Especifica sinalizadores para um evento de sincronização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_level"><strong>SYNCMGR_EVENT_LEVEL</strong></a><br/></td>
<td>Especifica o tipo de evento que está sendo relatado para a central de sincronização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_capabilities"><strong>SYNCMGR_HANDLER_CAPABILITIES</strong></a><br/></td>
<td>Especifica os recursos de um manipulador em relação às ações que podem ser executadas em relação a ele.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_policies"><strong>SYNCMGR_HANDLER_POLICIES</strong></a><br/></td>
<td>Enumera as políticas especificadas por um manipulador de sincronização que se desvia da política padrão.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_type"><strong>SYNCMGR_HANDLER_TYPE</strong></a><br/></td>
<td>Especifica o tipo de um manipulador. Usado por <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype"><strong>ISyncMgrHandlerInfo:: GetType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_capabilities"><strong>SYNCMGR_ITEM_CAPABILITIES</strong></a><br/></td>
<td>Especifica as ações que podem ser executadas em um item.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_policies"><strong>SYNCMGR_ITEM_POLICIES</strong></a><br/></td>
<td>Especifica as políticas de um item para controlar como elas podem ser habilitadas ou desabilitadas pela política de grupo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_choice"><strong>SYNCMGR_PRESENTER_CHOICE</strong></a><br/></td>
<td>Descreve a opção que um usuário faz sobre uma resolução de conflitos do Gerenciador de sincronização. Usado por <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_next_step"><strong>SYNCMGR_PRESENTER_NEXT_STEP</strong></a><br/></td>
<td>Descreve a próxima etapa que deve ocorrer na resolução de conflitos do Gerenciador de sincronização. Usado por <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_progress_status"><strong>SYNCMGR_PROGRESS_STATUS</strong></a><br/></td>
<td>Especifica o status atual do progresso de um processo de sincronização. Usado por <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress"><strong>ISyncMgrSyncCallback:: ReportProgress</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_abilities"><strong>SYNCMGR_RESOLUTION_ABILITIES</strong></a><br/></td>
<td>Indica as habilidades e a atividade de resolução de conflitos a seguir. Usado com <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities"><strong>ISyncMgrResolutionHandler:: QueryAbilities</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_feedback"><strong>SYNCMGR_RESOLUTION_FEEDBACK</strong></a><br/></td>
<td>Descreve Gerenciador de Sincronização comentários de resolução. Usado por <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_sync_control_flags"><strong>SYNCMGR_SYNC_CONTROL_FLAGS</strong></a><br/></td>
<td>Indica os sinalizadores usados por <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl:: StartHandlerSync</strong></a> e <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl:: StartItemSync</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a><br/></td>
<td>Os valores de enumeração <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a> são usados no método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize"><strong>ISyncMgrSynchronize:: Initialize</strong></a> para indicar como o evento de sincronização foi iniciado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrhandlerflags"><strong>SYNCMGRHANDLERFLAGS</strong></a><br/></td>
<td>Usado na estrutura <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a> como sinalizadores que se aplicam ao manipulador atual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a><br/></td>
<td>O valor de enumeração <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a> especifica como o Gerenciador de sincronização deve ser invocado no método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems"><strong>ISyncMgrSynchronizeInvoke:: UpdateItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgritemflags"><strong>SYNCMGRITEMFLAGS</strong></a><br/></td>
<td>Especifica informações para o item atual na estrutura <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a><br/></td>
<td>Os valores de enumeração <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a> especificam um nível de erro para uso no método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback:: LogError</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a><br/></td>
<td>Os valores de enumeração <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a> são usados em métodos da interface <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> para identificar eventos para os quais o manipulador está registrado para ser notificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrstatus"><strong>SYNCMGRSTATUS</strong></a><br/></td>
<td>Usado no método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setitemstatus"><strong>ISyncMgrSynchronize:: SetItemStatus</strong></a> para especificar o status atualizado para o item.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags"><strong>THUMBBUTTONFLAGS</strong></a><br/></td>
<td>Usado pelo <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>ThumbButton</strong></a> para controlar Estados e comportamentos específicos do botão.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask"><strong>THUMBBUTTONMASK</strong></a><br/></td>
<td>Usado pela estrutura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>ThumbButton</strong></a> para especificar quais membros dessa estrutura contêm dados válidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/ne-thumbnailstreamcache-thumbnailstreamcacheoptions"><strong>ThumbnailStreamCacheOptions</strong></a><br/></td>
<td>Define as opções de cache usadas pela interface <a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags"><strong>TRANSFER_SOURCE_FLAGS</strong></a><br/></td>
<td>Usado por métodos das interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> para controlar suas operações de arquivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a><br/></td>
<td>O <a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a> valores enumerados são usados com a função <a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TRANSLATEURL</strong></a> para determinar como ele será executado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-undock_reason"><strong>UNDOCK_REASON</strong></a><br/></td>
<td>Valores que indicam o motivo pelo qual uma janela de aplicativo de acessibilidade encaixada foi desencaixada. Usado por <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservicecallback-undocked"><strong>IAccessibilityDockingServiceCallback:: Undocked</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-url_scheme"><strong>URL_SCHEME</strong></a><br/></td>
<td>Usado para especificar esquemas de URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>O <a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a> valores enumerados são usados com <a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLASSOCIATIONDIALOG</strong></a> para determinar como ele é executado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpcolorflags"><strong>VPCOLORFLAGS</strong></a><br/></td>
<td>Especifica o uso de uma cor. Usado pelos métodos <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpwatermarkflags"><strong>VPWATERMARKFLAGS</strong></a><br/></td>
<td>Especifica sinalizadores de marca d' água. Usado por <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ivisualproperties-setwatermark"><strong>IVisualProperties:: setwatermark</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 
