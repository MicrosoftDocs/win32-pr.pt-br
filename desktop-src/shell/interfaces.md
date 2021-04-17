---
description: Esta seção descreve as interfaces de shell do Windows.
title: 'Interfaces de Shell '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 05223970-14f5-44c2-937b-07826b8aecf9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 23bd87e86ba9e30ce443616920326bf37aba6d2c
ms.sourcegitcommit: 9a614d8ce23dcca88873148683d9ec7d38be57b9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2020
ms.locfileid: "104368983"
---
# <a name="shell-interfaces"></a>Interfaces de Shell 

Esta seção descreve as interfaces de shell do Windows.

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
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iaccessibleobject"><strong>IAccessibleobject</strong></a><br/></td>
<td>Expõe um método que pode ser usado por um aplicativo de acessibilidade.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)"><strong>IAccessibilityDockingService</strong></a><br/></td>
<td>Encaixa uma única janela de aplicativo de acessibilidade na parte inferior de uma tela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh448547(v=vs.85)"><strong>IAccessibilityDockingServiceCallback</strong></a><br/></td>
<td>Informa um aplicativo de acessibilidade de que sua janela foi desencaixada.<br/></td>
</tr>
<tr class="even">
<td><a href="iaclcustommru.md"><strong>IACLCustomMRU</strong></a><br/></td>
<td>Expõe métodos que são usados para inicializar uma lista de MRU (usada mais recentemente) para um objeto de conclusão automática.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a><br/></td>
<td>Expõe um método que melhora a eficiência de <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>preenchimento automático</strong></a> quando as cadeias de caracteres candidatas são organizadas em uma hierarquia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2"><strong>IACList2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a> para permitir que os clientes de um objeto de preenchimento automático recuperem e definam sinalizadores de opção.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a><br/></td>
<td>Representa a classe base abstrata da qual as operações baseadas em progresso podem ser herdadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogressdialog"><strong>IActionProgressDialog</strong></a><br/></td>
<td>Expõe métodos que inicializam e param uma caixa de diálogo de progresso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager"><strong>IApplicationActivationManager</strong></a><br/></td>
<td>Fornece métodos que ativam aplicativos da Windows Store para as <a href="/previous-versions/windows/apps/hh464906(v=win.10)">extensões</a>de inicialização, arquivo e protocolo. Normalmente, você usará essa interface em depuradores e ferramentas de design.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a><br/></td>
<td>Expõe métodos que consultam e definem aplicativos padrão para <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>tipos de associação</strong></a>de arquivo específicos e protocolos em um <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>nível de associação</strong></a>específico. <br/>
<blockquote>
[!Note]<br />
A partir do Windows 8, a única funcionalidade dessa interface com suporte é <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault"><strong>QueryCurrentDefault</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui"><strong>IApplicationAssociationRegistrationUI</strong></a><br/></td>
<td>Expõe um método que inicia uma caixa de diálogo de associação avançada por meio da qual o usuário pode personalizar suas associações.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings"><strong>IApplicationDesignModeSettings</strong></a><br/></td>
<td>Permite que os aplicativos da ferramenta de desenvolvimento falsifiquem dinamicamente os Estados do sistema e do usuário, como a resolução de vídeo nativa, o fator de escala do dispositivo e o estado de exibição do aplicativo, com a finalidade de testar os aplicativos da Windows Store em execução no modo de design para uma ampla gama de fatores forma sem a necessidade de hardware real. Também permite o teste de alterações em estado normalmente controlado pelo usuário para testar aplicativos da Windows Store em vários cenários.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2"><strong>IApplicationDesignModeSettings2</strong></a><br/></td>
<td>Permite que os aplicativos da ferramenta de desenvolvimento controlem dinamicamente os Estados do sistema e do usuário, como a resolução de vídeo nativa, o fator de escala do dispositivo e o layout da exibição do aplicativo, relatados aos aplicativos da Windows Store com a finalidade de testar os aplicativos da Windows Store em execução no modo de design para uma ampla gama de fatores forma sem a necessidade de hardware real. Também permite o teste de alterações em estado normalmente controlado pelo usuário para testar aplicativos da Windows Store em vários cenários.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations"><strong>IApplicationDestinations</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo remova um ou todos os destinos das categorias <strong>recentes</strong> ou <strong>frequentes</strong> em uma lista de atalhos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists"><strong>IApplicationDocumentLists</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo recupere o conteúdo das categorias <strong>recentes</strong> ou <strong>frequentes</strong> em uma lista de atalhos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher"><strong>IAppPublisher</strong></a><br/></td>
<td>Expõe métodos para publicar aplicativos por meio de <strong>Adicionar ou remover programas</strong> no painel de controle. Essa é a interface principal implementada para essa finalidade.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility"><strong>IAppVisibility</strong></a><br/></td>
<td>Fornece a funcionalidade para determinar se a exibição está mostrando aplicativos da Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents"><strong>IAppVisibilityEvents</strong></a><br/></td>
<td>Permite que os aplicativos recebam notificações de alterações de estado em uma exibição e de alterações na visibilidade da tela inicial.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a><br/></td>
<td>Expõe métodos para operações com uma caixa de diálogo ou menu de associação de arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker"><strong>IAssocHandlerInvoker</strong></a><br/></td>
<td>Expõe métodos que invocam um manipulador de aplicativo associado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute"><strong>IAttachmentExecute</strong></a><br/></td>
<td>Expõe métodos que funcionam com aplicativos cliente para apresentar um ambiente de usuário que fornece download seguro e troca de arquivos por email e anexos de mensagens.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a><br/></td>
<td>Exposto pelo objeto de preenchimento automático (CLSID_AutoComplete). Essa interface permite que os aplicativos inicializem, habilitem e desabilitem o objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete2"><strong>IAutoComplete2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a>. Essa interface permite que os clientes do objeto de preenchimento automático recuperem e definam várias opções que controlam como a conclusão automática Opera.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iautocompletedropdown"><strong>IAutoCompleteDropDown</strong></a><br/></td>
<td>Expõe métodos que permitem que os clientes redefinam ou consultem o estado de exibição da lista suspensa preenchimento automático, que contém as conclusões possíveis para uma cadeia de caracteres inserida pelo usuário em um controle de edição.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ibandhost"><strong>IBandHost</strong></a><br/></td>
<td>Expõe métodos que criam e destruim bandas e especificam sua disponibilidade.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite"><strong>IBandSite</strong></a><br/></td>
<td>Expõe métodos que controlam objetos de banda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ibrowserframeoptions"><strong>IBrowserFrameOptions</strong></a><br/></td>
<td>Permite que um navegador ou host pergunte ao <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> que tipo de comportamento de exibição é suportado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategorizer"><strong>ICategorizer</strong></a><br/></td>
<td>Expõe métodos que são usados para obter informações sobre listas de identificadores de itens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategoryprovider"><strong>ICategoryProvider</strong></a><br/></td>
<td>Expõe uma lista de categorizadores registrados em um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburn"><strong>ICDBurn</strong></a><br/></td>
<td>Expõe métodos que determinam se um sistema tem hardware para gravação no CD, a letra da unidade de um dispositivo gravador de CD e inicia programaticamente uma sessão de gravação em CD. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a><br/></td>
<td>Expõe métodos que habilitam a inspeção e a manipulação de colunas no modo de exibição detalhes do Windows Explorer. Cada coluna é referenciada por uma estrutura <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> , que nomeia uma propriedade.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a><br/></td>
<td>Exposto pelas caixas de diálogo de arquivo comum a serem usadas quando hospedam um navegador de Shell. Se houver suporte, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a> expõe métodos que permitem que uma exibição de shell manipule vários casos que exigem um comportamento diferente em uma caixa de diálogo do que em uma exibição de shell normal. Você Obtém um ponteiro de interface <strong>ICommDlgBrowser</strong> chamando <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> no objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a><br/></td>
<td>Estende os recursos do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a>. Essa interface é exposta pelas caixas de diálogo de arquivo comuns quando hospedam um navegador de Shell. Um ponteiro para <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a> pode ser obtido chamando <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> no objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icommdlgbrowser3"><strong>ICommDlgBrowser3</strong></a><br/></td>
<td>Estende os recursos de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>e usados pelas caixas de diálogo comuns de arquivo quando eles hospedam um navegador de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-icomputerinfochangenotify"><strong>IComputerInfoChangeNotify</strong></a><br/></td>
<td>Essa interface pode estar ausente em versões posteriores do Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a><br/></td>
<td>Expõe métodos para conectar e desconectar objetos <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>IContactManagerInterop</strong></a><br/></td>
<td>Habilita o acesso a métodos <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>ContactManager</strong></a> em um aplicativo que gerencia várias janelas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a><br/></td>
<td>Expõe métodos que criam ou mesclam um menu de atalho associado a um objeto Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a><br/></td>
<td>Expõe métodos que criam ou mesclam um menu de atalho (contexto) associado a um objeto Shell. Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> adicionando um método que permite que os objetos de cliente manipulem mensagens associadas a itens de menu extraídos pelo proprietário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3"><strong>IContextMenu3</strong></a><br/></td>
<td>Expõe métodos que criam ou mesclam um menu de atalho associado a um objeto Shell. Permite que os objetos de cliente manipulem mensagens associadas a itens de menu desenhados pelo proprietário e estende o <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a> aceitando um valor de retorno dessa manipulação de mensagens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb"><strong>IContextMenuCB</strong></a><br/></td>
<td>Expõe um método que habilita o retorno de chamada de um menu de contexto. Por exemplo, para adicionar um ícone de escudo a um <strong>MenuItem</strong> que requer elevação.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb776063(v=vs.85)"><strong>IControlMarkup</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)"><strong>ICopyHook</strong></a><br/></td>
<td>Expõe um método que cria um <em>manipulador de vínculo de cópia</em>. Um manipulador de cabo de cópia é uma extensão de shell que determina se uma pasta ou um objeto de impressora do shell pode ser movido, copiado, renomeado ou excluído. O Shell chama o método <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)"><strong>ICopyHook:: CopyCallback</strong></a> antes de executar uma dessas operações.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a><br/></td>
<td>Expõe um método que cria um objeto de uma classe especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> para permitir que o chamador altere alguns parâmetros do processo que está sendo criado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs"><strong>ICreateProcessInputs</strong></a><br/></td>
<td>Usado pela interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a> para alterar alguns parâmetros do processo que está sendo criado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovider"><strong>ICredentialProvider</strong></a><br/></td>
<td>Expõe métodos usados na instalação e na manipulação de um provedor de credenciais. Todos os provedores de credenciais devem implementar essa interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a><br/></td>
<td>Expõe métodos que permitem a manipulação de uma credencial.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredential2"><strong>ICredentialProviderCredential2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a> adicionando um método que recupera o Sid (identificador de segurança) de um usuário. A credencial é associada a esse usuário e pode ser agrupada no bloco do usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a><br/></td>
<td>Fornece um mecanismo de retorno de chamada assíncrono usado por uma credencial para notificá-lo de eventos de alteração de estado ou texto na IU de logon ou na interface do usuário da credencial.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialevents2"><strong>ICredentialProviderCredentialEvents2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a> adicionando métodos que habilitam a atualização em lotes de campos na interface do usuário do logotipo ou da IU de credenciais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions"><strong>ICredentialProviderCredentialWithFieldOptions</strong></a><br/></td>
<td>Fornece um método que permite que a estrutura do provedor de credenciais determine se você fez uma personalização para a opção de um campo em uma interface de usuário de logon ou credencial.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderevents"><strong>ICredentialProviderEvents</strong></a><br/></td>
<td>Fornece um mecanismo de retorno de chamada assíncrono usado por um provedor de credenciais para notificá-lo de alterações na lista de credenciais ou em seus campos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderfilter"><strong>ICredentialProviderFilter</strong></a><br/></td>
<td>Usado para filtrar dinamicamente os provedores de credenciais com base nas informações disponíveis em tempo de execução.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidersetuserarray"><strong>ICredentialProviderSetUserArray</strong></a><br/></td>
<td>Fornece um método que permite que um provedor de credenciais receba o conjunto de usuários que será mostrado na interface do usuário de logon ou credencial.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruser"><strong>ICredentialProviderUser</strong></a><br/></td>
<td>Fornece métodos usados para recuperar determinadas propriedades de um usuário individual incluído em uma interface de usuário de logon ou credencial.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruserarray"><strong>ICredentialProviderUserArray</strong></a><br/></td>
<td>Representa o conjunto de usuários que aparecerão na interface do usuário de logon ou credencial. Essas informações permitem que o provedor de credenciais enumere o conjunto para recuperar informações de propriedade sobre cada usuário para preencher campos ou filtrar o conjunto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem"><strong>ICurrentItem</strong></a><br/></td>
<td>Obtido chamando <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> para um item. Se o item representar um instantâneo de um item em um momento anterior, essa interface obterá a versão atual do item.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory"><strong>ICurrentWorkingDirectory</strong></a><br/></td>
<td>Expõe métodos que permitem que um cliente recupere ou defina o diretório de trabalho atual de um objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist"><strong>ICustomDestinationList</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo forneça uma lista de atalhos personalizada, incluindo destinos e tarefas, para exibição na barra de tarefas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability"><strong>IDataObjectAsyncCapability</strong></a><br/></td>
<td>Habilita interfaces que geralmente são síncronas para funcionar de forma assíncrona. <br/>
<blockquote>
[!Note]<br />
Essa interface é a versão atual renomeada de <a href="/previous-versions//bb776309(v=vs.85)"><strong>IAsyncOperation</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider"><strong>IDataObjectprovider</strong></a><br/></td>
<td>Fornece métodos que permitem definir ou recuperar a <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>interface IDataObject</strong></a>de um objeto <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage?view=winrt-19041">DataPackage</a> , que o DataPackage usa para dar suporte à interoperabilidade. O objeto DataPackage é usado por um aplicativo para fornecer dados a outro aplicativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop"><strong>IDataTransferManagerInterop</strong></a><br/></td>
<td>Habilita o acesso a métodos <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataTransferManager"><strong>Datatransfermanager</strong></a> em um aplicativo da Windows Store que gerencia várias janelas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a><br/></td>
<td>Expõe métodos para definir ícones padrão associados a um objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize"><strong>IDefaultFolderMenuInitialize</strong></a><br/></td>
<td>Fornece métodos usados para obter e definir informações do menu de atalho. Essas informações são as mesmas fornecidas para <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a> por meio da estrutura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-idelayedpropertystorefactory"><strong>IDelayedPropertyStoreFactory</strong></a><br/></td>
<td>Expõe um método para criar um objeto <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> especificado em circunstâncias em que o acesso à propriedade é potencialmente lento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder"><strong>IDelegateFolder</strong></a><br/></td>
<td>Expõe um método pelo qual uma pasta delegada recebe a interface <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> necessária para alocar e liberar IDs de item.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegateitem"><strong>IDelegateItem</strong></a><br/></td>
<td>Usado para obter a representação subjacente imediatamente do caminho de um item.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idesktopgadget"><strong>IDesktopGadget</strong></a><br/></td>
<td>Expõe um método que permite a adição programática de um gadget instalado à área de trabalho do usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper"><strong>IDesktopWallpaper</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory"><strong>IDestinationStreamFactory</strong></a><br/></td>
<td>Expõe um método para copiar manualmente um fluxo ou arquivo antes de aplicar as alterações às propriedades.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem"><strong>IDisplayItem</strong></a><br/></td>
<td>Expõe métodos que localizam uma versão do item atual a ser usado para obter propriedades de exibição, como o nome do item, que será exibido na interface do usuário. Usado pelas caixas de diálogo do mecanismo de cópia para fornecer à interface do usuário um item apropriado a ser exibido. Se nenhuma outra versão puder ser encontrada, o item atual será usado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a><br/></td>
<td>Expõe métodos que notificam o objeto de janela de encaixe das alterações, incluindo exibição, ocultação e remoção iminente. Essa interface é implementada por objetos de janela que podem ser encaixados dentro do espaço de borda de uma janela do Windows Explorer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe"><strong>IDockingWindowFrame</strong></a><br/></td>
<td>Expõe métodos que dão suporte à adição de objetos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> a um quadro. Implementado pelo navegador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite"><strong>IDockingWindowSite</strong></a><br/></td>
<td>Expõe métodos que gerenciam o espaço de borda para um ou mais objetos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> . Essa interface é implementada pelo navegador e é semelhante à interface <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow"><strong>IOleInPlaceUIWindow</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a><br/></td>
<td>Exposto pelo shell para permitir que um aplicativo especifique a imagem que será exibida durante uma operação de arrastar e soltar do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idragsourcehelper2"><strong>IDragSourceHelper2</strong></a><br/></td>
<td>Expõe um método que adiciona funcionalidade a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a>. Esse método define as características de uma operação de arrastar e soltar em um objeto <strong>IDragSourceHelper</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper"><strong>IDropTargetHelper</strong></a><br/></td>
<td>Expõe métodos que permitem que os destinos de soltar exibam uma imagem de arrastar enquanto a imagem está sobre a janela de destino.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idynamichwhandler"><strong>IDynamicHWHandler</strong></a><br/></td>
<td>Chamado pela reprodução automática. Expõe métodos que obtêm informações dinâmicas sobre um manipulador registrado antes de exibi-lo para o usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers"><strong>IEnumAssocHandlers</strong></a><br/></td>
<td>Expõe um método que permite a enumeração de uma coleção de manipuladores associada a extensões de nome de arquivo específicas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumerableview"><strong>IEnumerableView</strong></a><br/></td>
<td>Expõe métodos que enumeram o conteúdo de uma exibição e recebem notificações do retorno de chamada após a conclusão da enumeração. Essa interface permite que os clientes de uma exibição tentem compartilhar a lista de conteúdo da pasta do modo de exibição.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand"><strong>IEnumExplorerCommand</strong></a><br/></td>
<td>Fornecido por um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a>. Essa interface contém a enumeração de comandos a serem colocados na barra de comandos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a><br/></td>
<td>Um enumerador OLE padrão usado por um cliente para determinar os objetos de pesquisa disponíveis para uma pasta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist"><strong>IEnumFullIDList</strong></a><br/></td>
<td>Expõe um conjunto padrão de métodos que enumeram os ponteiros para PIDLs (listas de identificadores de item) dos itens em uma pasta do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a><br/></td>
<td>Expõe um conjunto padrão de métodos usados para enumerar o PIDLs dos itens em uma pasta do Shell. Quando o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: EnumObjects</strong></a> de uma pasta é chamado, ele cria um objeto de enumeração e passa um ponteiro para a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a> do objeto de volta para o aplicativo de chamada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects"><strong>IEnumObjects</strong></a><br/></td>
<td>Expõe métodos para enumerar objetos desconhecidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps"><strong>IEnumPublishedApps</strong></a><br/></td>
<td>Expõe métodos que enumeram aplicativos publicados para adicionar ou remover programas no painel de controle. O objeto expondo essa interface é solicitado por meio de <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-iapppublisher-enumapps"><strong>IAppPublisher:: EnumApps</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumreadycallback"><strong>IEnumReadyCallback</strong></a><br/></td>
<td>Expõe métodos que permitem ao modo de exibição notificar o implementador quando a enumeração for concluída. A exibição chama esse método para informar ao implementador que a enumeração pode ser recuperada por meio de <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents"><strong>IEnumerableView:: CreateEnumIDListFromContents</strong></a>. O retorno de chamada permite que o implementador compartilhe a enumeração de exibições.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources"><strong>IEnumResources</strong></a><br/></td>
<td>Expõe métodos de enumeração de recursos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a><br/></td>
<td>Expõe a enumeração de interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> . Normalmente, essa interface é obtida chamando o método <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrconflict"><strong>IEnumSyncMgrConflict</strong></a><br/></td>
<td>Expõe métodos de enumeração de conflito.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrevents"><strong>IEnumSyncMgrEvents</strong></a><br/></td>
<td>Expõe métodos de enumeração de eventos de sincronização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems"><strong>IEnumSyncMgrSyncItems</strong></a><br/></td>
<td>Expõe métodos que enumeram os objetos de item de sincronização gerenciados pelo manipulador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a><br/></td>
<td>Expõe métodos que definem um determinado Estado ou parâmetro relacionados ao verbo de comando, bem como um método para invocar esse verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment"><strong>IExecuteCommandApplicationHostEnvironment</strong></a><br/></td>
<td>Fornece um método único que permite a um aplicativo determinar se seu host está no modo de área de trabalho ou de imersão.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost"><strong>IExecuteCommandHost</strong></a><br/></td>
<td>Fornece um método que permite que um manipulador de verbo de shell baseado em <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a>consulte o modo de interface do usuário do componente de host do qual o aplicativo foi invocado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> é um objeto de navegador que pode ser navegado ou que pode hospedar uma exibição de um objeto de dados. Como um objeto de navegador repleto de recursos, ele também dá suporte a um log de viagem automático.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents"><strong>IExplorerBrowserEvents</strong></a><br/></td>
<td>Expõe métodos para notificação de navegação do navegador do Explorer e eventos de criação de exibição.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a><br/></td>
<td>Expõe métodos que obtêm a aparência do comando, enumeram subcomandos ou invocam o comando.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a><br/></td>
<td>Expõe métodos para criar comandos do Explorer e enumeradores de comando.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a><br/></td>
<td>Expõe um único método que permite a recuperação do estado do comando.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a><br/></td>
<td>Usado no Windows Explorer por uma implementação <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> para dar sugestões à exibição sobre quais painéis estão visíveis. Além disso, um host <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> pode usar essa interface para fornecer informações sobre a visibilidade do painel. O host deve implementar <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> com <strong>SID_EXPLORERPANEVISIBILITY</strong> como a ID do serviço. O host deve estar na cadeia de sites. <br/> A implementação de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> é recuperada da pasta do Shell. A pasta do Shell, por sua vez, é recuperada da exibição. Uma extensão de namespace pode optar por fornecer uma exibição personalizada (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>) em vez de usar o objeto de exibição de pasta do sistema (DefView). Nesse caso, a implementação de <strong>IShellView</strong> deve incluir uma implementação de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView:: GetFolder</strong></a> para retornar o objeto <strong>IExplorerPaneVisibility</strong> .<br/> Uma extensão de namespace pode fornecer uma exibição personalizada implementando a própria <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> em vez de usar o DefView (objeto de exibição de pasta do sistema). Nesse caso, a implementação de <strong>IShellView</strong> deve incluir uma implementação de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView:: GetFolder</strong></a> para fazer uso de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona"><strong>IExtractIcon</strong></a><br/></td>
<td>Expõe métodos que permitem que um cliente recupere o ícone associado a um dos objetos em uma pasta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a><br/></td>
<td>Expõe métodos que solicitam uma imagem em miniatura de uma pasta do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2"><strong>IExtractImage2</strong></a><br/></td>
<td>Estende os recursos do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a><br/></td>
<td>Expõe métodos que inicializam, mostram e obtêm resultados da caixa de diálogo de arquivo comum.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialog2"><strong>IFileDialog2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> fornecendo métodos que permitem que o chamador nomeie um local restrito e específico que pode ser navegado na caixa de diálogo arquivo comum, bem como para especificar texto alternativo a ser exibido como um rótulo no botão <strong>Cancelar</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents"><strong>IFileDialogControlEvents</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo seja notificado sobre eventos relacionados a controles que o aplicativo adicionou a uma caixa de diálogo de arquivo comum.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo adicione controles a uma caixa de diálogo de arquivo comum.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents"><strong>IFileDialogEvents</strong></a><br/></td>
<td>Expõe métodos que permitem a notificação de eventos em uma caixa de diálogo de arquivo comum.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse"><strong>IFileIsInUse</strong></a><br/></td>
<td>Expõe métodos que podem ser chamados para obter informações sobre ou fechar um arquivo que está sendo usado por outro aplicativo. Quando um aplicativo tenta acessar um arquivo e encontra esse arquivo já em uso, ele pode usar os métodos dessa interface para reunir informações a serem apresentadas ao usuário em uma caixa de diálogo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog"><strong>IFileOpenDialog</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> adicionando métodos específicos à caixa de diálogo aberta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a><br/></td>
<td>Expõe métodos para copiar, mover, renomear, criar e excluir itens de Shell, bem como métodos para fornecer diálogos de progresso e erro. Essa interface substitui a função <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink"><strong>IFileOperationProgressSink</strong></a><br/></td>
<td>Expõe métodos que fornecem um sistema de notificação avançado usado por chamadores de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> para monitorar os detalhes das operações que eles executam por meio dessa interface.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog"><strong>IFileSaveDialog</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> adicionando métodos específicos à caixa de diálogo salvar, que incluem aqueles que fornecem suporte para a coleção de metadados a serem persistidos com o arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler"><strong>IFileSyncMergeHandler</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a><br/></td>
<td>Expõe métodos que armazenam informações do sistema de arquivos para otimizar chamadas para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a>, que armazena informações do sistema de arquivos para otimizar chamadas para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>. Essa interface adiciona o conjunto de capacidade ou obtém a ID do arquivo ou o identificador de classe de junção (CLSID).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/schema-library-iconreference"><strong>IFileViewer</strong></a><br/></td>
<td>Expõe métodos que designam uma interface que permite que um visualizador de arquivos registrado seja notificado quando ele deve mostrar ou imprimir um arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite"><strong>IFileViewerSite</strong></a><br/></td>
<td>Expõe métodos que designam uma interface que permite que um visualizador de arquivos recupere o identificador para a janela fixada atual ou defina uma nova janela fixada. A janela fixada é a janela na qual o Visualizador de arquivos atual exibe um arquivo. Quando o usuário seleciona um novo arquivo a ser exibido, o Shell direciona o Visualizador de arquivos para exibir o novo arquivo na janela fixa em vez de criar uma nova janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter"><strong>IFolderFilter</strong></a><br/></td>
<td>Exposto por um cliente para especificar como filtrar a enumeração de uma pasta do Shell por um aplicativo de servidor.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite"><strong>IFolderFilterSite</strong></a><br/></td>
<td>Exportado por um host para permitir que os clientes especifiquem como filtrar uma enumeração de pasta do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a><br/></td>
<td>Expõe métodos que recuperam informações sobre as opções de exibição de uma pasta, selecionam itens especificados nessa pasta e definem o modo de exibição da pasta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a><br/></td>
<td>Expõe métodos que recuperam informações sobre as opções de exibição de uma pasta, selecionam itens especificados nessa pasta e definem o modo de exibição da pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewhost"><strong>IFolderViewHost</strong></a><br/></td>
<td>Expõe um método que hospeda um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a> em uma janela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a><br/></td>
<td>Expõe métodos que permitem o controle das opções de exibição de pasta específicas para as exibições do Windows 7 e posteriores.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderviewsettings"><strong>IFolderViewSettings</strong></a><br/></td>
<td>Expõe métodos para obter as configurações de exibição de pasta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane"><strong>IFrameworkInputPane</strong></a><br/></td>
<td>Fornece métodos que permitem que os aplicativos sejam informados sobre alterações de estado e localização para o painel de entrada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler"><strong>IFrameworkInputPaneHandler</strong></a><br/></td>
<td>Permite que um aplicativo seja notificado quando o painel de entrada (o teclado ou painel de manuscritos na tela) está sendo exibido ou oculto. Isso permite que a janela do aplicativo ajuste sua exibição para que nenhuma área de entrada (como uma caixa de texto) seja obscurecida pelo painel de entrada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo"><strong>IHandlerInfo</strong></a><br/></td>
<td>Fornece métodos que fornecem informações sobre o manipulador para métodos da interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup"><strong>IHomeGroup</strong></a><br/></td>
<td>Expõe métodos que determinam o status de associação do grupo doméstico de um computador e exibem o assistente de compartilhamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a><br/></td>
<td>Chamado pela reprodução automática para implementar a manipulação de tipos de mídia registrados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler2"><strong>IHWEventHandler2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a> para endereçar a elevação de controle de conta de usuário (UAC) para manipuladores de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname"><strong>IIdentityname</strong></a><br/></td>
<td>Expõe métodos para comparar dois itens para ver se eles são os mesmos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iimagerecompress"><strong>IImageRecompress</strong></a><br/></td>
<td>Expõe um método que recompacta imagens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a><br/></td>
<td>Expõe um único método usado para inicializar objetos que implementam <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> ou <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> com o nome de comando especificado pelo aplicativo e suas propriedades registradas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl/nn-shobjidl-iinitializenetworkfolder"><strong>IInitializeNetworkFolder</strong></a><br/></td>
<td>Expõe um método que inicializa a fonte de dados de rede CLSID_NetworkPlaces conforme especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithbindctx"><strong>IInitializeWithBindCtx</strong></a><br/></td>
<td>Expõe um método que inicializa um manipulador, como um manipulador de propriedades, um manipulador de miniaturas ou um Gerenciador de visualização, com um contexto de associação.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile"><strong>IInitializeWithFile</strong></a><br/></td>
<td>Expõe um método para inicializar um manipulador, como um manipulador de propriedades, um manipulador de miniaturas ou um Gerenciador de visualização, com um caminho de arquivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem"><strong>IInitializeWithItem</strong></a><br/></td>
<td>Expõe um método usado para inicializar um manipulador, como um manipulador de propriedades, um manipulador de miniaturas ou um Gerenciador de visualização, com um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore"><strong>IInitializeWithPropertyStore</strong></a><br/></td>
<td>Expõe um método que inicializa um manipulador, como um manipulador de propriedades, um manipulador de miniaturas ou um Gerenciador de visualização, com um repositório de propriedades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a><br/></td>
<td>Expõe um método que inicializa um manipulador, como um manipulador de propriedades, um manipulador de miniaturas ou um Gerenciador de visualização, com um fluxo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow"><strong>IInitializeWithWindow</strong></a><br/></td>
<td>Expõe um método pelo qual um cliente pode fornecer uma janela de proprietário para um objeto de Windows Runtime usado em um aplicativo de área de trabalho.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a><br/></td>
<td>Expõe métodos que alteram a ativação da interface do usuário e aceleradores de processo para um objeto de entrada de usuários contido no Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject2"><strong>IInputObject2</strong></a><br/></td>
<td>Expõe um método que estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a> manipulando aceleradores globais.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite"><strong>IInputObjectSite</strong></a><br/></td>
<td>Expõe um método que é usado para comunicar alterações de foco para um objeto de entrada de usuário contido no Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration"><strong>IInputPanelConfiguration</strong></a><br/></td>
<td>Fornece funcionalidade para aplicativos de desktop para aceitar o mecanismo de controle de foco usado em aplicativos da Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration"><strong>IInputPanelInvocationConfiguration</strong></a><br/></td>
<td>Permite que os aplicativos da Windows Store recusem o comportamento de invocação automática.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iiocancelinformation"><strong>IIOCancelInformation</strong></a><br/></td>
<td>Expõe métodos para postar uma mensagem de janela de cancelamento no thread do processo a partir da caixa de diálogo de progresso. <br/> Essa interface permite que a caixa de diálogo de progresso poste uma mensagem de thread por meio de <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> para o thread de trabalho para cancelar suas operações. O thread de trabalho deve verificar periodicamente a fila de mensagens por meio de <a href="/windows/desktop/api/winuser/nf-winuser-getmessage"><strong>GetMessage</strong></a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea"><strong>PeekMessage</strong></a> ou <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex"><strong>MsgWaitForMultipleObjectsEx</strong></a>.<br/> O método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation"><strong>IIOCancelInformation:: SetCancelInformation</strong></a> informa à caixa de diálogo de progresso qual ID de thread e em qual mensagem <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> quando o usuário clica em <strong>Cancelar</strong>. Uma ID de thread &quot; igual &quot; a zero desabilita a operação de envio para a mensagem de cancelamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits"><strong>IItemNameLimits</strong></a><br/></td>
<td>Recupera uma lista de caracteres válidos e inválidos ou o comprimento máximo de um nome no namespace. Use essa interface para análise e conversão de validação.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder"><strong>IKnownFolder</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo recupere informações sobre a categoria, o tipo, o GUID, o valor de PIDL, os recursos de redirecionamento e a definição de uma pasta conhecida. Ele fornece um método para o retrival do objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> de uma pasta conhecida. Ele também fornece métodos para obter ou definir o caminho da pasta conhecida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a><br/></td>
<td>Expõe métodos que criam, enumeram ou gerenciam pastas conhecidas existentes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid"><strong>ILaunchSourceAppUserModelId</strong></a><br/></td>
<td>Fornece um método para recuperar um <a href="appids.md">AppUserModelId</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference</strong></a><br/></td>
<td>Fornece métodos para recuperar informações sobre o aplicativo de origem.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor"><strong>ILaunchTargetMonitor</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference"><strong>ILaunchTargetViewSizePreference</strong></a><br/></td>
<td>Fornece um método para recuperar o tamanho de exibição preferencial para uma nova janela de aplicativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/shell-extensibility-bumper"><strong>IMarkupCallback</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a> pode ser alterado ou indisponível.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow"><strong>IModalWindow</strong></a><br/></td>
<td>Expõe um método que representa uma janela modal. Essa interface é usada no assistente do Windows XP Passport.<br/></td>
</tr>
<tr class="odd">
<td><a href="imultimonitordockingsite.md"><strong>IMultiMonitorDockingSite</strong></a><br/></td>
<td>Implementado pelo navegador. Expõe métodos que gerenciam qual monitor contém a barra de tarefas do Windows em um sistema de vários monitores. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-inamedpropertybag"><strong>INamedPropertyBag</strong></a><br/></td>
<td>Expõe métodos que fornecem um objeto com um recipiente de propriedades especificado no qual o objeto pode salvar suas propriedades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-inamedpropertystore"><strong>INamedPropertyStore</strong></a><br/></td>
<td>Expõe métodos que obtêm e definem propriedades nomeadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreeaccessible"><strong>INameSpaceTreeAccessible</strong></a><br/></td>
<td>Expõe métodos que executam ações de acessibilidade em um item de Shell de um controle de árvore de namespace.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a><br/></td>
<td>Expõe métodos usados para exibir e manipular nós em uma árvore de itens de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> fornecendo métodos que obtêm e definem os estilos de exibição dos controles TreeView para uso com itens de namespace do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a><br/></td>
<td>Expõe métodos que permitem ao usuário desenhar um controle de árvore de namespace personalizado e seus itens.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontroldrophandler"><strong>INameSpaceTreeControlDropHandler</strong></a><br/></td>
<td>Expõe métodos de manipulador para arrastar e soltar. Usado pelo controle de árvore de namespace para notificar o cliente sobre qualquer operação de arrastar e soltar que esteja acontecendo no controle. Fornece uma maneira para um cliente interceptar uma operação DROP e executar sua própria ação ou para retornar o efeito de soltar desejado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolevents"><strong>INameSpaceTreeControlEvents</strong></a><br/></td>
<td>Expõe métodos para manipular eventos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a><br/></td>
<td>Expõe um único método que recupera o status do suporte à filtragem <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System. IsPinnedToNameSpaceTree</a> de uma pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a><br/></td>
<td>Expõe métodos que orientam um namespace de um determinado nó raiz. A profundidade da movimentação é especificada e uma matriz opcional é retornada contendo as IDs de todos os nós percorridos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a><br/></td>
<td>Uma interface de retorno de chamada expondo métodos usados com <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a>. Depois de executar uma movimentação com <strong>INamespaceWalk</strong>, um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> que representa os nós movimentados é passado para os métodos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> . O que esses métodos fazem com as informações depende do objeto que está implementando-os.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb2"><strong>INamespaceWalkCB2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> com um método que é necessário para concluir uma movimentação de namespace. Esse método remove os dados coletados durante a movimentação. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewmenuclient"><strong>INewMenuClient</strong></a><br/></td>
<td>Expõe métodos que permitem a manipulação de itens em um menu do Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka"><strong>INewShortcutHook</strong></a><br/></td>
<td>Expõe métodos para criar um novo atalho da Internet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager"><strong>INewWindowManager</strong></a><br/></td>
<td>Expõe um método que determina se uma janela iniciada por outra janela deve ser exibida ou bloqueada, permitindo o controle das janelas pop-up.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica"><strong>INotifyReplica</strong></a><br/></td>
<td>Expõe um método que fornece um criador de objeto com os meios para notificar o objeto de que ele pode estar sujeito à reconciliação subsequente. O porta-arquivos Reconciler é responsável por implementar essa interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a><br/></td>
<td>Expõe métodos que permitem que os clientes acessem itens em uma coleção de objetos que dão suporte a <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection"><strong>IObjectCollection</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a> fornecendo métodos que permitem que os clientes adicionem e removam objetos que dão suporte a <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> em uma coleção.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider"><strong>IObjectProvider</strong></a><br/></td>
<td>Expõe um método para descobrir objetos que são nomeados com um <strong>GUID</strong> de outro objeto. Ao contrário de <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> , essa interface não delegará sua funcionalidade a outros objetos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid"><strong>IObjectWithAppUserModelID</strong></a><br/></td>
<td>Expõe métodos que permitem que os implementadores de um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a> personalizado forneçam acesso à sua APPUSERMODELID (ID de modelo de usuário) explícita do aplicativo. Essas informações são usadas para determinar se um determinado tipo de arquivo pode ser adicionado à lista de atalhos de um aplicativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithbackreferences"><strong>IObjectWithBackReferences</strong></a><br/></td>
<td>Fornece um método para interagir com referências backais mantidas por um objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent"><strong>IObjectWithCancelEvent</strong></a><br/></td>
<td>Fornece um chamador com um evento que será sinalizado pelo objeto chamado para indicar cancelamento de uma tarefa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a><br/></td>
<td>Expõe métodos que obtêm e definem modos de enumeração de um item analisado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid"><strong>IObjectWithProgID</strong></a><br/></td>
<td>Expõe métodos que fornecem acesso ao ProgID associado a um objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iobjectwithpropertykey"><strong>IObjectWithPropertyKey</strong></a><br/></td>
<td>Expõe métodos para obter e definir a chave de propriedade.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a><br/></td>
<td>Expõe métodos que obtêm ou definem os itens selecionados representados por uma matriz de itens de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr"><strong>IObjMgr</strong></a><br/></td>
<td>Expõe métodos que permitem que um cliente acrescente ou remova um objeto de uma coleção de objetos gerenciados por um objeto de servidor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel"><strong>IOpenControlPanel</strong></a><br/></td>
<td>Expõe métodos que recuperam o estado de exibição do painel de controle, o caminho de itens individuais do painel de controle e que abrem o próprio painel de controle ou um item individual do painel de controle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource"><strong>IOpenSearchSource</strong></a><br/></td>
<td>Expõe um método para obter resultados da pesquisa de uma fonte de dados OpenSearch personalizada do lado do cliente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog"><strong>IOperationsProgressDialog</strong></a><br/></td>
<td>Expõe métodos para obter, definir e consultar uma caixa de diálogo de progresso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ipackagedebugsettings"><strong>IPackageDebugSettings</strong></a><br/></td>
<td>Permite que os desenvolvedores do depurador controlem o ciclo de vida de um aplicativo da Windows Store, como suspender ou retomar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification"><strong>IPackageExecutionStateChangeNotification</strong></a><br/></td>
<td>Habilita o recebimento de notificações de alteração de estado do pacote durante a depuração do aplicativo da Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a><br/></td>
<td>Expõe métodos que obtêm e definem o pai e a ID filho do pai. Embora o <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> seja normalmente implementado em IShellItems, ele não é específico do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem"><strong>IParseAndCreateItem</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a><br/></td>
<td>Expõe um método que inicializa objetos de pasta do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a><br/></td>
<td>Expõe métodos que obtêm informações de objetos de pasta do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3"><strong>IPersistFolder3</strong></a><br/></td>
<td>Estende as interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a> , permitindo que um objeto de pasta implemente o tratamento não padrão de atalhos de pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist"><strong>IPersistIDList</strong></a><br/></td>
<td>Expõe métodos que são usados para persistir listas de identificadores de item.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage"><strong>IPersistSerializedPropStorage</strong></a><br/></td>
<td>Expõe métodos para persistir dados de armazenamento de propriedade serializados para uso posterior e para restaurar dados persistentes para uma nova instância do repositório de propriedades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage2"><strong>IPersistSerializedPropStorage2</strong></a><br/></td>
<td>Expõe métodos para persistir dados de armazenamento de propriedade serializados para uso posterior e para restaurar dados persistentes para uma nova instância do repositório de propriedades.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh707033(v=vs.85)"><strong>IPlaybackManager</strong></a><br/></td>
<td>Fornece métodos que permitem que aplicativos de mídia se comuniquem com o Gerenciador de reprodução do Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh707034(v=vs.85)"><strong>IPlaybackManagerEvents</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler"><strong>IPreviewHandler</strong></a><br/></td>
<td>Expõe métodos para a exibição de visualizações avançadas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe"><strong>IPreviewHandlerFrame</strong></a><br/></td>
<td>Permite que os gerenciadores de visualização transmitam atalhos de teclado para o host. Essa interface recupera uma lista de atalhos de teclado e direciona o host para manipular um atalho de teclado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals"><strong>IPreviewHandlerVisuals</strong></a><br/></td>
<td>Expõe métodos para aplicar informações de cor e fonte aos gerenciadores de visualização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewitem"><strong>IPreviewItem</strong></a><br/></td>
<td>Identifica um item que será mostrado no painel de visualização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipreviousversionsinfo"><strong>IPreviousVersionsInfo</strong></a><br/></td>
<td>Expõe um método que verifica as versões anteriores de arquivos ou pastas do servidor, armazenadas para a finalidade da reversão pela tecnologia de <em>cópias de sombra</em> fornecida com o Windows Server 2003.<br/></td>
</tr>
<tr class="odd">
<td><a href="iprivateidentitymanager.md"><strong>IPrivateIdentityManager</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="iprivateidentitymanager2.md"><strong>IPrivateIdentityManager2</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice"><strong>IProfferService</strong></a><br/></td>
<td>Expõe um mecanismo geral para que os objetos ofereçam serviços a outros objetos no mesmo host.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog"><strong>IProgressDialog</strong></a><br/></td>
<td>Expõe métodos que fornecem opções para um aplicativo exibir uma caixa de diálogo de progresso. Essa interface é exportada pelo objeto da caixa de diálogo de progresso (CLSID_ProgressDialog). Esse objeto é uma maneira genérica de mostrar ao usuário como uma operação está progredindo. Normalmente, ele é usado ao excluir, carregar, copiar, mover ou baixar um grande número de arquivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a><br/></td>
<td>Expõe métodos que representam aplicativos para adicionar ou remover programas no painel de controle. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp2"><strong>IPublishedApp2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a> fornecendo um método de instalação adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a><br/></td>
<td>Expõe métodos para trabalhar com o assistente de impressão online, o assistente de publicação na Web e o assistente para adicionar local de rede. No Windows Vista, o <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a> não dá mais suporte ao assistente de publicação na Web ou ao assistente de impressão online.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a><br/></td>
<td>Expõe métodos que simplificam o processo de recuperação de informações armazenadas no registro em associação com a definição de um tipo de arquivo ou protocolo e sua associação a um aplicativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>IQueryCancelAutoPlay</strong></a><br/></td>
<td>Expõe um método que substitui programaticamente a <a href="autorun2k-intro.md">reprodução automática</a> ou <a href="autoplay.md">autorun</a>. Isso permite que você personalize o local e o tipo de conteúdo que é iniciado quando a mídia é inserida.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycodepage"><strong>IQueryCodePage</strong></a><br/></td>
<td>Obtém e define o valor numérico (identificador de página de código) da página de código ANSI.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a><br/></td>
<td>Expõe um método que fornece um mecanismo simples e padrão para que os objetos consultem um cliente para obter permissão para continuar uma operação. Os clientes de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>, por exemplo, devem passar uma implementação de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a> para o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show"><strong>IUserNotification:: show</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iquerycontinuewithstatus"><strong>IQueryContinueWithStatus</strong></a><br/></td>
<td>Expõe métodos que fornecem um mecanismo padrão para que os provedores de credenciais chamem <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue"><strong>QueryContinue</strong></a> enquanto tentam se conectar à rede para determinar se eles devem continuar essas tentativas. Os provedores de credenciais também podem usar essa interface para exibir mensagens ao usuário ao tentar estabelecer uma conexão de rede.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo"><strong>IQueryInfo</strong></a><br/></td>
<td>Expõe os métodos que o Shell usa para recuperar informações de dicas de informações e sinalizadores de um item que reside em uma implementação de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . Dicas de informações geralmente são exibidas dentro de um controle <a href="/windows/desktop/Controls/tooltip-controls">ToolTip</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem"><strong>IRelatedItem</strong></a><br/></td>
<td>Expõe métodos que derivam itens relacionados com relações específicas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer"><strong>IRemoteComputer</strong></a><br/></td>
<td>Expõe um método que enumera ou Inicializa uma extensão de namespace quando é invocado em um objeto remoto. Essa interface é usada, por exemplo, para inicializar a pasta virtual impressoras remotas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink"><strong>IResolveShellLink</strong></a><br/></td>
<td>Expõe um método que permite a um aplicativo solicitar que um objeto de pasta do Shell resolva um link para um de seus itens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a><br/></td>
<td>Expõe métodos que contêm itens de um objeto de dados.<br/> Um <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a> é uma pasta que pode armazenar itens de todos no namespace e representá-los para o usuário em uma única pasta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask"><strong>IRunnableTask</strong></a><br/></td>
<td>Uma interface de thread livre que pode ser exposta por um objeto para permitir que as operações sejam executadas em um thread em segundo plano. Por exemplo, se o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation"><strong>IExtractImage:: getLocation</strong></a> retornar E_PENDING, o aplicativo de chamada poderá extrair a imagem em um thread em segundo plano.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-isearchboxinfo"><strong>ISearchBoxInfo</strong></a><br/></td>
<td>Expõe métodos que permitem que o chamador recupere informações inseridas em uma caixa de pesquisa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext"><strong>ISearchContext</strong></a><br/></td>
<td>Expõe métodos que canalizam informações de personalização para os ganchos de pesquisa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory"><strong>ISearchFolderItemFactory</strong></a><br/></td>
<td>Expõe métodos que criam e modificam pastas de pesquisa. Os métodos set são chamados primeiro para configurar os parâmetros da pesquisa. Quando não for chamado, os valores padrão serão usados em seu lugar. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist"><strong>ISearchFolderItemFactory:: GetIDList</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem"><strong>ISearchFolderItemFactory:: GetShellItem</strong></a> retornam as duas formas da pesquisa especificada por esses parâmetros. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-isharedbitmap"><strong>ISharedBitmap</strong></a><br/></td>
<td>Expõe métodos com eficiência de memória para acessar bitmaps. Essa interface é usada como um wrapper fino em objetos HBITMAP, permitindo que esses objetos sejam consultados e protegidos de ter seus dados subjacentes alterados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a><br/></td>
<td>Expõe métodos que definem e recuperam informações sobre as configurações de compartilhamento padrão de um computador para a pasta <strong>Users</strong> ( <code>C:\Users</code> ) ou <strong>Public</strong> ( <code>C:\Users\Public</code> ). Também expõe um conjunto de métodos que permitem o controle do compartilhamento de impressora.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ishellapp"><strong>IShellApp</strong></a><br/></td>
<td>Expõe métodos que fornecem informações gerais sobre um aplicativo para o aplicativo Adicionar/remover programas. Você não pode usá-lo fora do aplicativo Adicionar/remover programas. As informações fornecidas por essa interface incluem uma lista de ações de gerenciamento com suporte e se o aplicativo está instalado no momento. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a><br/></td>
<td>Implementado por hosts de exibições do Shell (objetos que implementam <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>). Expõe métodos que fornecem serviços para a exibição que está hospedando e outros objetos que são executados no contexto da janela do Explorer. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellchangenotify"><strong>IShellChangeNotify</strong></a><br/></td>
<td>Expõe um método que notifica uma extensão de namespace de shell quando a ID de um item é alterada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a><br/></td>
<td>Exposto por pastas do Shell para fornecer informações detalhadas sobre os itens em uma pasta. Essas são as mesmas informações exibidas pelo Windows Explorer quando a exibição da pasta é definida como detalhes. Para sistemas Windows 2000 e posteriores, o <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a> é substituído por <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit"><strong>IShellExtInit</strong></a><br/></td>
<td>Expõe um método que inicializa extensões de Shell para folhas de propriedades, menus de atalho e manipuladores de arrastar e soltar (extensões que adicionam itens a menus de atalho durante operações de arrastar e soltar não padrão).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a><br/></td>
<td>Exposto por todos os objetos de pasta de namespace do Shell, seus métodos são usados para gerenciar pastas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a><br/></td>
<td>Estende os recursos do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>. Seus métodos fornecem uma variedade de informações sobre o conteúdo de uma pasta do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfoldersearchable.md"><strong>IShellFolderSearchable</strong></a><br/></td>
<td>Expõe métodos que permitem que uma extensão de shell forneça um namespace pesquisável.<br/></td>
</tr>
<tr class="even">
<td><a href="ishellfoldersearchablecallback.md"><strong>IShellFolderSearchableCallback</strong></a><br/></td>
<td>Expõe rotinas de retorno de chamada para monitorar o processo de pesquisa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>IShellFolderViewCB</strong></a><br/></td>
<td>Expõe um método que permite a comunicação entre o Windows Explorer e uma exibição de pasta implementada usando o objeto de exibição de pasta do sistema (o objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> retornado por meio de <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a>) para que o modo de exibição de pasta possa ser notificado de eventos e modificar sua exibição de acordo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual"><strong>IShellFolderViewDual</strong></a><br/></td>
<td>Expõe métodos que modificam a exibição e selecionam itens na pasta atual. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual2"><strong>IShellFolderViewDual2</strong></a><br/></td>
<td>Expõe métodos que modificam a exibição e selecionam itens na pasta atual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual3"><strong>IShellFolderViewDual3</strong></a><br/></td>
<td>Expõe métodos que modificam o modo de exibição de pasta atual.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfolderviewtype.md"><strong>IShellFolderViewType</strong></a><br/></td>
<td>Expõe métodos que permitem que uma pasta do Shell dê suporte a exibições diferentes em seu conteúdo (layouts hierárquicos diferentes de seus dados).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellicon"><strong>IShellIcon</strong></a><br/></td>
<td>Expõe um método que obtém um índice de ícone para um objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay"><strong>IShellIconOverlay</strong></a><br/></td>
<td>Expõe métodos que são usados por uma extensão de namespace para especificar sobreposições de ícone para os objetos que ele contém.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier"><strong>IShellIconOverlayIdentifier</strong></a><br/></td>
<td>Expõe métodos que manipulam toda a comunicação entre manipuladores de sobreposição de ícone e o Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedataabort"><strong>IShellImageDataAbort</strong></a><br/></td>
<td>Expõe um único método usado para anular processos de <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedatafactory"><strong>IShellImageDataFactory</strong></a><br/></td>
<td>Expõe métodos que criam instâncias <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> com base em várias fontes de imagem.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a><br/></td>
<td>Expõe métodos que recuperam informações sobre um item de Shell. <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> são as representações preferenciais de itens em qualquer código novo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> com métodos que recuperam vários valores de Propriedade do item. <strong>IShellItem</strong> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> são as representações preferenciais de itens em qualquer código novo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray"><strong>IShellItemArray</strong></a><br/></td>
<td>Expõe métodos que criam e manipulam matrizes de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>itens de shell</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter"><strong>IShellItemFilter</strong></a><br/></td>
<td>Exposto por um cliente para especificar como filtrar a enumeração de um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>item de shell</strong></a> por um aplicativo de servidor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory"><strong>IShellItemImageFactory</strong></a><br/></td>
<td>Expõe um método para retornar ícones ou miniaturas de itens de Shell. Se nenhuma miniatura ou ícone estiver disponível para o item solicitado, um ícone por classe poderá ser fornecido a partir do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources"><strong>IShellItemResources</strong></a><br/></td>
<td>Expõe métodos para manipular e consultar recursos do item do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary"><strong>IShellLibrary</strong></a><br/></td>
<td>Expõe métodos para criar e gerenciar bibliotecas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a><br/></td>
<td>Expõe métodos que criam, modificam e resolvem links do Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo anexe blocos de dados extras a um <a href="/windows/desktop/shell/links">link do Shell</a>. Esses métodos adicionam, copiam ou removem blocos de dados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a><br/></td>
<td>Expõe métodos que interagem com menus do Shell, como o menu <strong>Iniciar</strong> e o menu <strong>favoritos</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback"><strong>IShellMenuCallback</strong></a><br/></td>
<td>Uma interface de retorno de chamada que expõe um método que recebe mensagens de uma faixa de menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext"><strong>IShellPropSheetExt</strong></a><br/></td>
<td>Expõe métodos que permitem que um manipulador de folha de propriedades adicione ou substitua páginas na folha de propriedades exibida para um objeto de arquivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ishellrundll"><strong>IShellRunDll</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a><br/></td>
<td>Expõe métodos que apresentam uma exibição no Windows Explorer ou nas janelas de pastas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a><br/></td>
<td>Estende os recursos do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ishellview3"><strong>IShellView3</strong></a><br/></td>
<td>Estende os recursos do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> fornecendo um método para substituir <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2:: CreateViewWindow2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a><br/></td>
<td>Fornece acesso à coleção de janelas abertas do Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istartmenupinnedlist"><strong>IStartMenuPinnedList</strong></a><br/></td>
<td>Expõe um método que desafixa um atalho de aplicativo do menu <strong>Iniciar</strong> ou da barra de tarefas.<br/></td>
</tr>
<tr class="odd">
<td><a href="nn-shobjidl-istorageprovidercopyhook.md"><strong>IStorageProviderCopyHook</strong></a><br/></td>
<td>Expõe um método que determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler"><strong>IStorageProviderHandler</strong></a><br/></td>
<td>Recupera o <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a> associado a um arquivo ou pasta específica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a><br/></td>
<td>Fornece uma coleção de propriedades associadas a um arquivo ou pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamasync"><strong>IStreamAsync</strong></a><br/></td>
<td>Expõe métodos para gerenciar entrada/outpout (e/s) para um fluxo assíncrono. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamunbufferedinfo"><strong>IStreamUnbufferedInfo</strong></a><br/></td>
<td>Expõe um método que determina o tamanho do setor como um auxílio ao alinhamento de bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager"><strong>ISuspensionDependencyManager</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflict"><strong>ISyncMgrConflict</strong></a><br/></td>
<td>Expõe métodos que fornecem informações sobre um conflito recuperado de um repositório de conflitos e permite que o conflito seja resolvido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a><br/></td>
<td>Expõe um método que obtém a lista de ID de conflito para um objeto de conflito.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictitems"><strong>ISyncMgrConflictItems</strong></a><br/></td>
<td>Expõe métodos que obtêm dados de item de conflito e contagem de itens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a><br/></td>
<td>Expõe um método que apresenta um conflito ao usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems"><strong>ISyncMgrConflictResolutionItems</strong></a><br/></td>
<td>Expõe métodos que obtêm informações de item e contagem de itens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo"><strong>ISyncMgrConflictResolveInfo</strong></a><br/></td>
<td>Expõe métodos que obtêm e definem informações sobre a resolução de conflitos do Gerenciador de sincronização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictstore"><strong>ISyncMgrConflictStore</strong></a><br/></td>
<td>Expõe métodos que permitem que um manipulador forneça conflitos que aparecem na pasta conflitos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo ou manipulador inicie ou interrompa uma sincronização, notifique a central de sincronização de alterações no conjunto de manipuladores ou itens ou notifique alterações em valores de propriedade.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a><br/></td>
<td>Expõe métodos que enumeram por meio de uma matriz de estruturas <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> . Cada uma dessas estruturas fornece informações sobre um item que pode ser sincronizado. <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> tem os mesmos métodos de todas as interfaces de enumerador padrão: avançar, ignorar, redefinir e clonar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrevent"><strong>ISyncMgrEvent</strong></a><br/></td>
<td>Expõe métodos que recuperam dados de um repositório de eventos. Um repositório de eventos permite que a central de sincronização obtenha um enumerador de todos os eventos na loja, bem como recupere eventos individuais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventlinkuioperation"><strong>ISyncMgrEventLinkUIOperation</strong></a><br/></td>
<td>Fornece um método que é chamado quando links de eventos são clicados na pasta de resultados de sincronização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventstore"><strong>ISyncMgrEventStore</strong></a><br/></td>
<td>Expõe métodos que permitem que um manipulador forneça seu próprio repositório de eventos e gerencie seus próprios eventos de sincronização, em vez de usar o armazenamento de eventos da central de sincronização padrão. Esses eventos são exibidos na pasta resultados da sincronização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler"><strong>ISyncMgrHandler</strong></a><br/></td>
<td>Expõe métodos que compõem a interface primária implementada por um manipulador de sincronização. A central de sincronização cria uma instância do manipulador por meio desta interface para obter propriedades, enumerar itens de sincronização e modificar estado. A central de sincronização cria uma instância separada do manipulador em um thread separado para executar uma sincronização ou uma operação de interface do usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlercollection"><strong>ISyncMgrHandlerCollection</strong></a><br/></td>
<td>Expõe métodos que fornecem um enumerador de IDs de manipulador de sincronização e instanciam esses manipuladores de sincronização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo"><strong>ISyncMgrHandlerInfo</strong></a><br/></td>
<td>Expõe métodos que permitem que um manipulador forneça informações de propriedade e estado para a central de sincronização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a><br/></td>
<td>Expõe métodos para que um aplicativo possa ser registrado no Gerenciador de sincronização. Isso pode ser obtido por meio da interface <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> ou registrando-se diretamente no registro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a><br/></td>
<td>Expõe métodos que gerenciam conflitos de sincronização. Implemente essa interface para construir um manipulador de conflito de sincronização. A interface do usuário de resolução de conflitos chamará essa interface para resolver o conflito apresentado ao usuário. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation"><strong>ISyncMgrScheduleWizardUIOperation</strong></a><br/></td>
<td>Expõe um método que permite que um manipulador exiba o assistente de agendamento de sincronização para o manipulador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsessioncreator"><strong>ISyncMgrSessionCreator</strong></a><br/></td>
<td>Expõe um único método pelo qual um manipulador ou aplicativo externo pode notificar a central de sincronização que a sincronização começou, bem como relatar o progresso e os eventos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynccallback"><strong>ISyncMgrSyncCallback</strong></a><br/></td>
<td>Expõe métodos que permitem a um processo de sincronização relatar progresso e eventos para a central de sincronização, ou para consultar se o processo foi cancelado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize"><strong>ISyncMgrSynchronize</strong></a><br/></td>
<td>Expõe métodos que permitem que o aplicativo ou serviço registrado receba notificações do Gerenciador de sincronização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback"><strong>ISyncMgrSynchronizeCallback</strong></a><br/></td>
<td>Expõe métodos que gerenciam o processo de sincronização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke"><strong>ISyncMgrSynchronizeInvoke</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo registrado invoque o Gerenciador de sincronização para atualizar itens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem"><strong>ISyncMgrSyncItem</strong></a><br/></td>
<td>Expõe métodos que agem e recuperam informações de um único item de sincronização, permitindo que os manipuladores gerenciem itens de sincronização como objetos independentes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer"><strong>ISyncMgrSyncItemContainer</strong></a><br/></td>
<td>Expõe métodos que fornecem informações aos manipuladores sobre os itens que eles contêm.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo"><strong>ISyncMgrSyncItemInfo</strong></a><br/></td>
<td>Expõe métodos que fornecem informações de propriedade e estado para um único item de sincronização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncresult"><strong>ISyncMgrSyncResult</strong></a><br/></td>
<td>Expõe um método que os aplicativos que chamam <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> podem usar para obter o resultado de uma chamada <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl:: StartHandlerSync</strong></a> ou <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl:: StartItemSync</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgruioperation"><strong>ISyncMgrUIOperation</strong></a><br/></td>
<td>Expõe um método pelo qual um manipulador de sincronização ou item de sincronização pode exibir um objeto de interface do usuário quando solicitado a fazê-lo pela central de sincronização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a><br/></td>
<td>Expõe métodos que controlam a barra de tarefas. Ele permite que você adicione, remova e ative dinamicamente itens na barra de tarefas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a> expondo um método para marcar uma janela como uma exibição de tela inteira.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a><br/></td>
<td>Estende o <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a> expondo métodos que dão suporte à funcionalidade de botão de barra de tarefas de inicialização e troca unificada adicionada no Windows 7. Essa funcionalidade inclui representações de miniatura e destinos de comutador com base em guias individuais em um aplicativo com guias, barras de ferramentas de miniatura, sobreposições de notificação e status e indicadores de progresso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4"><strong>ITaskbarList4</strong></a><br/></td>
<td>Estende o <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> fornecendo um método que permite ao chamador controlar dois valores de propriedade para a miniatura de guia e o recurso Peek.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailcache"><strong>IThumbnailCache</strong></a><br/></td>
<td>Expõe métodos para um cache de miniaturas do sistema que é compartilhado entre aplicativos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcacheprimer"><strong>IThumbnailCachePrimer</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ithumbnailhandlerfactory"><strong>IThumbnailHandlerFactory</strong></a><br/></td>
<td>Expõe um método para recuperar o manipulador de miniatura de um item. Implemente essa interface se desejar especificar qual extrator é usado para um IDList filho.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider"><strong>Manipuladordeminiaturai</strong></a><br/></td>
<td>Expõe um método para obter uma imagem em miniatura e deve ser implementado para manipuladores de miniatura. O objeto que implementa essa interface também deve implementar <a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailsettings"><strong>IThumbnailSettings</strong></a><br/></td>
<td>Fornece um método que permite que um provedor de miniatura determine o contexto do usuário de uma solicitação de miniatura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a><br/></td>
<td>Obtém ou define o fluxo de miniatura. Essa interface é somente para uso interno e só pode ser chamada pelo aplicativo photos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itrackshellmenu"><strong>ITrackShellMenu</strong></a><br/></td>
<td>Expõe métodos que estendem a interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a> fornecendo a capacidade de coordenar botões da barra de ferramentas com um menu, bem como exibir um menu pop-up.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Imagetranscode/nn-imagetranscode-itranscodeimage"><strong>ITranscodeImage</strong></a><br/></td>
<td>Expõe um método que permite a conversão para formatos de imagem JPEG ou bitmap (BMP) de qualquer tipo de imagem com suporte no Windows. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink"><strong>ITransferAdviseSink</strong></a><br/></td>
<td>Expõe métodos que dão suporte à coleta de status e informações de falha.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a><br/></td>
<td>Expõe métodos que criam um item de Shell de destino para uma operação de cópia ou movimentação. Essa interface é fornecida para permitir mais controle sobre as operações de arquivo, fornecendo um método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise"><strong>ITransferDestination:: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem"><strong>ITransferMediumItem</strong></a><br/></td>
<td>Usado por um mecanismo de cópia para obter o item no qual chamar <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> para retornar um ponteiro para interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> ou interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a>. Essas interfaces podem ser consultadas e enumeradas para operações de cópia, movimentação ou exclusão.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a><br/></td>
<td>Expõe métodos para manipular <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, incluindo copiar, mover, reciclar e outros. Essa interface é oferecida para fornecer mais controle sobre as operações de arquivo, fornecendo um método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise"><strong>ITransferSource:: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-itraydeskband"><strong>ITrayDeskBand</strong></a><br/></td>
<td>Expõe métodos que mostram, ocultam e consultam deskbands.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist"><strong>IUpdateIDList</strong></a><br/></td>
<td>Fornece um método para atualizar a <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> do filho de um objeto Folder.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook"><strong>IURLSearchHook</strong></a><br/></td>
<td>Expõe um método que é usado pelo navegador para converter o endereço de um protocolo de URL desconhecido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook2"><strong>IURLSearchHook2</strong></a><br/></td>
<td>Expõe um método que é usado pelo navegador para converter o endereço de um protocolo de URL desconhecido usando um objeto de contexto de pesquisa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iuseraccountchangecallback"><strong>IUserAccountChangeCallback</strong></a><br/></td>
<td>Expõe um método que é chamado quando a imagem que representa uma conta de usuário é alterada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a><br/></td>
<td>Expõe métodos que definem informações de notificação e, em seguida, exibem essa notificação para o usuário em um balão que aparece em conjunto com a área de notificação da barra de tarefas. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> difere de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a> somente em seu método <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>show</strong></a> , que adiciona um parâmetro adicional para uma interface de retorno de chamada para se comunicar com a notificação. Caso contrário, as duas interfaces são idênticas em forma e função. CLSID_UserNotification implementa ambas as versões do <strong>show</strong> como uma sobrecarga.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a><br/></td>
<td>Expõe métodos que definem informações de notificação e, em seguida, exibem essa notificação para o usuário em um balão que aparece em conjunto com a área de notificação da barra de tarefas. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> não herda de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>. <strong>IUserNotification2</strong> difere de <strong>IUserNotification</strong> somente em seu método <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>show</strong></a> , que adiciona um parâmetro adicional para uma interface de retorno de chamada para se comunicar com a notificação. Caso contrário, as duas interfaces são idênticas em forma e função. CLSID_UserNotification implementa ambas as versões do <strong>show</strong> como uma sobrecarga.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotificationcallback"><strong>IUserNotificationCallback</strong></a><br/></td>
<td>Expõe um método para o tratamento de um clique do mouse ou do menu de atalho em um balão de notificação. Usado com <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>IUserNotification2:: show</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusetobrowseitem"><strong>IUseToBrowseItem</strong></a><br/></td>
<td>Localiza o item que deve ser usado ao navegar para este item.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iviewstateidentityitem"><strong>IViewStateIdentityItem</strong></a><br/></td>
<td>Fornece um item de persistência canônica, um item para o qual as personalizações de exibição serão lembradas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager"><strong>IVirtualDesktopManager</strong></a><br/></td>
<td>Expõe métodos que permitem que um aplicativo interaja com grupos de janelas que formam espaços de trabalho virtuais.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a><br/></td>
<td>Expõe métodos que definem e obtêm propriedades visuais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwebwizardextension"><strong>IWebWizardExtension</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a> expondo métodos para definir a URL inicial da extensão do assistente e uma URL específica em caso de erro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a><br/></td>
<td>Usado por assistentes, como o assistente de publicação na Web e o assistente de ordenação de impressão online, que hospedam páginas de conteúdo do lado do servidor. Essa interface expõe métodos para especificar páginas de extensão com suporte e para navegar para dentro e fora dessas páginas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardsite"><strong>IWizardSite</strong></a><br/></td>
<td>Expõe os métodos usados por uma extensão de assistente para navegar pelas bordas entre si mesmo e o restante do assistente.<br/></td>
</tr>
<tr class="odd">
<td><a href="taskcompletionclient.md"><strong>TaskCompletionClient</strong></a><br/></td>
<td>Habilita a conclusão da tarefa. <br/></td>
</tr>
</tbody>
</table>



 

 

 