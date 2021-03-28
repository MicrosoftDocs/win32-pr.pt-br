---
description: 'Um conjunto de chaves de cadeia de caracteres que são usadas com o método IBindCtx:: RegisterObjectParam para especificar um contexto de associação.'
title: Chaves de cadeia de caracteres de contexto de associação (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b1dcdb3b9199fede88d6f13949cc9276bde17b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968242"
---
# <a name="bind-context-string-keys"></a>Associar chaves de cadeia de caracteres de contexto

Um conjunto de chaves de cadeia de caracteres que são usadas com o método [**IBindCtx:: RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) para especificar um contexto de associação.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP SP2</strong>. Especifique esse contexto de associação para permitir que os clientes da fonte de dados substituam a política de letra da unidade oculta e habilite o acesso aos objetos de exibição para fontes de dados nas unidades bloqueadas.<br/> Usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/> O sistema oferece suporte a políticas controladas pelo administrador que ocultam letras de unidade especificadas para impedir que os usuários acessem essas unidades por meio do Windows Explorer. Quando essa política está ativa, o resultado é que os objetos de exibição e outros manipuladores criados com o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder:: CreateViewObject</strong></a> falharão quando chamados nas unidades bloqueadas pela política.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para fazer com que o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> use o objeto especificado pelo parâmetro <em>PBC</em> para criar o objeto de destino; Nesse caso, o objeto especificado pelo parâmetro <em>punk</em> na chamada <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> deve implementar a interface <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a> . <br/> Usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 7</strong>. Passado para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> com um valor <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> para controlar o modo de enumeração do item analisado. O valor de <strong>FOLDER_ENUM_MODE</strong> é passado no contexto de associação por meio de um objeto que implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a>. <br/> Os itens com diferentes modos de enumeração se comparam de maneira canônica (SHCIDS_CANONICALONLY), pois enumeram conjuntos diferentes de itens.<br/> Se um item não oferecer suporte ao modo de enumeração (porque ele não é uma pasta ou não fornece o modo de enumeração), ele será criado no modo de enumeração padrão.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 7</strong>. Passado para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> junto com <strong>STR_FILE_SYS_BIND_DATA</strong>. Isso força a análise simples, além de investigar Desktop.ini arquivos ao longo do caminho do qual obter uma cadeia de caracteres de nome localizada. Isso evita a investigação de pastas ao longo do caminho, que, em um caso de uma pasta que representa um servidor ou um compartilhamento, pode levar muito tempo e recursos. Desktop.ini arquivos são armazenados em cache em alguns locais, portanto, ele será, pelo menos, tão eficiente quanto a investigação de atributos de pastas e, em seguida, a investigação para o Desktop.ini se essa pasta deve transformar a UO Transp como somente leitura.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP SP2</strong>. Especifique esse contexto de associação para forçar um atalho de pasta a resolver o link que aponta para seu destino. <br/> Um atalho de pasta é um item de pasta que aponta para outro item de pasta no mesmo namespace, usando um link (atalho) para manter o IDList do destino. O link é resolvido para acompanhar o destino caso ele seja movido ou renomeado. Por exemplo, a pasta <strong>meus locais de rede</strong> do Windows XP e a pasta <strong>computador</strong> com Windows Vista podem conter atalhos de pasta criados com o assistente para <strong>Adicionar local de rede</strong> . Para melhorar o desempenho, o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> não resolve links para a pasta de rede por padrão.<br/> Usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP</strong>. Especifique esse contexto de associação para impedir uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> na pasta de <strong>área de trabalho</strong> de tratar caminhos relativos como relativos à área de trabalho; Nesse caso, a análise falha quando esse contexto de associação é especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para instruir um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> a não resolver o destino de link obtido ao usar o GUID de <strong>BHID_LinkTargetItem</strong> em <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP</strong>. Especifique esse contexto de associação para fornecer metadados de arquivo para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> , que é usado em vez de tentar recuperar os metadados do arquivo real. O objeto associado deve implementar <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a> e, opcionalmente, também pode implementar <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a>. Por padrão, o método <strong>IShellFolder::P arsedisplayname</strong> verifica se o arquivo existe e usa os metadados reais do arquivo para popular a lista de IDs.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido em Windows 8.1</strong>. Especifique esse contexto de associação para indicar que os dados fornecidos no contexto de associação de <strong>STR_FILE_SYS_FIND_DATA</strong> devem ser usados para criar uma lista de ItemId no formato do Windows 7.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 7</strong>. Especifique esse contexto de associação quando o manipulador estiver sendo recuperado no mesmo thread que a interface do usuário. Todas as atividades com uso intensivo de memória, como as que envolvem o acesso ao disco ou à rede, devem ser evitadas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação ao solicitar um manipulador de <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Esse valor é usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Consulte o sinalizador <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> para obter mais informações.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação ao solicitar um manipulador de <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Esse valor é usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Consulte o sinalizador <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> para obter mais informações.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação ao solicitar um manipulador de <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Esse valor é usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Consulte o sinalizador <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> para obter mais informações.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação ao solicitar um manipulador de <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Esse valor é usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Consulte o sinalizador <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> para obter mais informações.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 7</strong>. Especifique esse contexto de associação ao solicitar um manipulador de <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Esse valor é usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Consulte o sinalizador <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> para obter mais informações.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação ao solicitar um manipulador de <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Esse valor é usado com <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Consulte o sinalizador <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> para obter mais informações.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Somente Windows Vista.</strong> Especifique esse contexto de associação para fazer uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> que solicita a interface <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> de um objeto do sistema de arquivos para retornar um filtro de texto se nenhum outro filtro estiver disponível. Esse valor não é definido a partir do Windows 7.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Somente Windows Vista.</strong> Especifique esse contexto de associação para fazer uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> que solicita que a interface do <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> para um objeto do sistema de arquivos não retorne um filtro de fallback se nenhum filtro registrado for encontrado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para habilitar o carregamento do histórico de um fluxo para uma navegação interna quando o método <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory:: LOADHISTORY</strong></a> for chamado. Uma navegação interna é uma navegação dentro da mesma exibição.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 7</strong>. Especifique esse contexto de associação com STR_PARSE_PREFER_FOLDER_BROWSING quando o cliente quiser que os manipuladores de pasta do Shell da Internet gerem um IDList para qualquer URL válida se uma pasta do tipo DAV não puder ser criada para essa URL. A URL não tem verificação para existir; somente sua sintaxe é verificada e tem um manipulador de protocolo registrado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 7</strong>. Especifique esse contexto de associação para instruir as implementações de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: InitializeEx</strong></a> para armazenar em cache objetos auxiliares com uso intensivo de memória que podem existir em instanciações de itens de Shell em vez de recriar esses objetos sempre que um item de Shell for criado. O objeto associado é outro objeto de contexto de associação, inicialmente vazio. Isso deve resultar em um objeto de contexto de associação separado, que é acessado por meio de <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a> ou <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: register. objectparam</strong></a>. <br/> Um chamador deve optar por esse comportamento fornecendo esse parâmetro de contexto de associação ao chamar <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. Ao fazer isso, você otimiza o comportamento de associação a vários nomes de análise sucessivamente. O tempo de vida do objeto de contexto de associação deve abranger várias instâncias de itens de shell e seus contextos de ligação individuais.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para permitir que caracteres de nome de arquivo inválidos apareçam em nomes de arquivos. Por padrão, uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> rejeita caracteres ilegais em nomes de arquivo. Esse contexto de ligação é significativo apenas em conjunto com o contexto de associação STR_FILE_SYS_FIND_DATA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para habilitar uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> na pasta <strong>da área de trabalho</strong> para analisar URLs. Se esse contexto de associação for especificado, ele substituirá <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 7</strong>. Especifique este contexto de associação para instruir a implementação de uma fonte de dados de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para otimizar o comportamento de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. <br/> Normalmente, o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a> executa duas operações de ligação no nome a ser analisado: uma a e uma para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> e outra para criar o item de Shell. Quando há suporte para o contexto de associação de <strong>STR_PARSE_AND_CREATE_ITEM</strong> , a segunda associação é evitada criando o item de shell durante o <strong>IShellFolder::P arsedisplayname</strong> vincular e armazenar o item de shell por meio de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem:: SetItem</strong></a>. Em seguida, o <strong>SHCreateItemFromParsingName</strong> usa o item de shell armazenado em vez de criar um.<br/> Esse parâmetro se aplica ao último elemento do nome que é analisado. Por exemplo, no nome &quot;C:\Folder1\File.txt, os dados se aplicam a File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Somente Windows Vista.</strong> Especifique que, ao analisar uma URL, esse contexto de ligação não deve exigir que a URL exista antes de gerar um IDList para ela. Especifique esse contexto de associação junto com <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> quando o cliente desejar que os manipuladores de pasta do <strong>Shell de Internet</strong> gerem um IDList para a URL se uma pasta DAV não puder ser criada para a URL fornecida.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para passar o item original que está sendo analisado novamente quando esse item for armazenado como um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> que também implementa a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> . Antes do Windows 7, esse valor não foi definido em um arquivo de cabeçalho. Ele pode ser definido pelo chamador ou transmitido como seu valor de cadeia de caracteres de <strong>L &quot; ParseOriginalItem &quot; </strong>. A partir do Windows 7, o valor é definido em shlobj. h. Observe que esse é um cabeçalho diferente das outras constantes STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP</strong>. Especifique esse contexto de associação para habilitar uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> na pasta <strong>da área de trabalho</strong> para analisar URLs como se elas fossem pastas. Use este contexto de associação para associar a um servidor WebDAV.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para impedir uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> no formulário pasta <strong>da área de trabalho</strong> analisando URLs. Esse contexto de ligação pode ser substituído por <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para substituir o repositório de propriedades padrão usado pelo método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> e use o repositório de propriedades especificado como o parâmetro bind. Aplica-se a pastas delegadas.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP SP2</strong>. Especifique esse contexto de associação para habilitar uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> na pasta <strong>da área de trabalho</strong> para usar a &quot; &quot; notação Shell: prefix para acessar arquivos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para fazer uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para exibir a caixa de diálogo diagnóstico de rede se a análise de um caminho de rede falhar.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows Vista</strong>. Especifique esse contexto de associação para fazer uma chamada para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para ignorar a verificação do cache de compartilhamentos de rede e contatar o servidor de rede diretamente. As informações sobre compartilhamentos de rede são armazenadas em cache para melhorar o desempenho e <strong>IShellFolder::P arsedisplayname</strong> verifica esse cache por padrão.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP</strong>. Especifique este contexto de associação para passar Propriedades analisadas para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para um namespace delegate. O namespace pode usar as propriedades passadas em vez de tentar analisar o próprio nome.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Somente Windows Vista.</strong> Um contexto de associação de análise que é usado para passar um conjunto de propriedades e o nome do item ao chamar <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>. O objeto no contexto de associação implementa <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> e é recuperado chamando <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a>.<br/> DBFolder é uma fonte de dados do shell que representa os itens nos resultados da pesquisa e exibições baseadas em consulta. DBFolder recupera esses itens consultando o sistema de pesquisa do Windows. Os itens nos resultados da pesquisa são identificados por meio de um esquema de protocolo, por exemplo, &quot; arquivo: &quot; ou &quot; MAPI: &quot; . O DBFolder fornece o comportamento para esses itens delegando para fontes de dados do shell que são criadas para esses protocolos. Consulte <a href="/previous-versions/bb233544(v=msdn.10)">Developing Add-ins do manipulador de protocolo</a> para obter mais informações.<br/> Quando DBFolder Delega sua operação de análise para as fontes de dados do shell que dão suporte aos protocolos de pesquisa do Windows, esse contexto de ligação fornece acesso a valores que foram retornados no resultado da consulta para esse item. Isso inclui o seguinte:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System. ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System. ParsingPath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System. ItemPathDisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System. ItemNameDisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Esse contexto de ligação também pode ser usado para analisar um item DBFolder se um cliente tiver um conjunto de propriedades que definem o item. Nesse caso, um nome vazio deve ser passado para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>.<br/> Antes do Windows 7, esse valor não foi definido em um arquivo de cabeçalho. Ele pode ser definido pelo chamador ou passado como seu valor de cadeia de caracteres: <code>L&quot;ParseWithProperties&quot;</code> . A partir do Windows 7, o valor é definido em shlobj. h. Observe que esse é um cabeçalho diferente de onde as outras constantes de STR são definidas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows 8</strong>. Especifique esse contexto de associação para indicar que o parâmetro de contexto de associação é um recipiente de Propriedades (<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)"><strong>IPropertyBag</strong></a>) usado para passar valores variados no contexto de associação. Consulte a seção comentários para obter mais detalhes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduzido no Windows XP</strong>. Especifique esse contexto de associação para fazer chamadas para os métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> para ignorar uma extensão de namespace de shell específica durante a análise ou associação. O CLSID do namespace a ser ignorado é fornecido pelo método <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist:: GetClassID</strong></a> do parâmetro bind. <br/>
<blockquote>
[!Note]<br />
Introduzido no Windows 2000 SP3, esse valor foi definido em shlobj. h até o Windows XP, quando foi movido para ShObjIdl. h.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">Não usado.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Os contextos de ligação são usados para passar parâmetros opcionais para funções que têm um \* parâmetro IBindCtx. Esses parâmetros são expressos como objetos COM e podem implementar interfaces que são usadas para modelar os dados do parâmetro. Alguns contextos de ligação representam um valor booliano, onde **true** indica que um objeto que implementa apenas [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e false indica que nenhum objeto está presente.

[**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname), [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) e [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) usam um contexto de associação e você pode passá-los por meio desse contexto de ligação.

Alguns contextos de ligação são específicos de determinadas implementações de fonte de dados ou tipos de manipulador.

Os parâmetros de contexto de associação são definidos para uso com uma função ou um método específico.

Ao solicitar um repositório de propriedades por meio de [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), você pode especificar o equivalente de [**\_ padrão de GPS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) passando um parâmetro [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) nulo. Você também pode especificar o equivalente do GPS \_ ReadWrite passando um modo de STGM \_ ReadWrite \| STGM \_ exclusivo no contexto de associação.

O recipiente de propriedades especificado pelo objeto de contexto de associação do **\_ \_ parâmetro PROPERTYBAG do Str** contém valores adicionais que você pode acessar com os métodos [**IPropertyBag:: Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) e [**IPropertyBag:: Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85)) .



| Nome da propriedade                                 | Type     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_sinalizadores de \_ itens de enumeração Str \_                       | \_UI4 VT  | **Introduzido no Windows 8**. Especifica um valor de [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) a ser passado para [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) quando você chama [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) com **BHID \_ EnumItems**.                                                                                                                                                                                                                         |
| \_Associação explícita de análise de Str \_ \_ \_ bem-sucedida | BOOL do VT \_ | **Introduzido no Windows 7**. O método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) define essa propriedade para informar ao chamador que o IDList retornado foi associado ao [ProgID](fa-progids.md) especificado com a **\_ análise de Str \_ com \_ \_ ProgID explícito** ou o aplicativo especificado com a **\_ análise de Str \_ com \_ \_ ASSOCAPP explícita**. Quando **a \_ Associação explícita de análise de Str tiver \_ \_ \_ êxito** estiver ausente, o ProgID ou o aplicativo não foi associado ao IDList. |
| \_análise \_ de Str com \_ \_ ASSOCAPP explícito          | VT \_ BSTR | **Introduzido no Windows 7**. Especifique essa propriedade para fazer com que uma chamada para o método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) retorne um IDList associado ao manipulador de associação de tipo de arquivo para o aplicativo.                                                                                                                                                                                                                                          |
| \_análise \_ de Str com \_ \_ ProgID explícito            | VT \_ BSTR | **Introduzido no Windows 7**. Especifique essa propriedade para fazer com que uma chamada para o método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) retorne um IDList associado ao manipulador de associação de arquivo do [ProgID](fa-progids.md)fornecido.                                                                                                                                                                                                                          |



 

Consulte o [exemplo análise com parâmetros](samples-parsingwithparameters.md) para obter um exemplo do uso de valores de contexto de associação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 
