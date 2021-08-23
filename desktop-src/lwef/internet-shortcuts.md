---
title: Atalhos da Internet
description: O objeto de atalho da Internet é usado para criar atalhos de área de trabalho para sites da Internet.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Objetos de atalho da Internet
- Controles do WebBrowser
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aba53c320ed740fe7d91a2425b4d47d66e28d78aa35e4ce893efeed12380c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749404"
---
# <a name="internet-shortcuts"></a>Atalhos da Internet

O objeto de atalho da Internet é usado para criar atalhos de área de trabalho para sites da Internet. Como os atalhos para itens no sistema de arquivos, os atalhos da Internet assumem a forma de um ícone na área de trabalho. Quando o usuário clica no ícone, o navegador é iniciado e exibe o site associado ao atalho.

Os tópicos a seguir são discutidos.

-   [Criando atalhos da Internet](#creating-internet-shortcuts)
    -   [Criando um atalho da Internet de um controle WebBrowser](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Criando um atalho da Internet a partir de uma URL](#creating-an-internet-shortcut-from-a-url)
-   [acessando a propriedade Armazenamento](#accessing-property-storage)
-   [Interfaces](#interfaces)
    -   [Interfaces OLE](#ole-interfaces)
    -   [Interfaces do Shell](#shell-interfaces)
-   [Funções](#functions)
    -   [Funções do utilitário de atalho da Internet](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Criando atalhos da Internet

Você pode criar um atalho da Internet usando um controle WebBrowser ou com a URL da página.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Criando um atalho da Internet de um controle WebBrowser

Se o seu aplicativo hospedar um controle WebBrowser, você poderá usar o objeto de atalho da Internet para criar atalhos da seguinte maneira.

1.  Crie uma instância do objeto de atalho da Internet com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), usando um identificador de classe (CLSID) de CLSID \_ InternetShortcut.
2.  Passe o ponteiro para a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) do WebBrowser para o objeto de atalho da Internet com [IObjectWithSite:: SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).
3.  Chame o método [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) do objeto de atalho da Internet quando desejar criar um atalho para a página que está sendo exibida pelo controle WebBrowser.

Um atalho será criado no local especificado em [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). Esse local permite que o controle WebBrowser Restaure seu estado, o que inclui a tarefa de carregar os documentos corretos em conjuntos de quadros.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Criando um atalho da Internet a partir de uma URL

Você também pode criar um atalho da Internet se tiver a URL da página à qual deseja vincular.

1.  Crie uma instância do objeto de atalho da Internet com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), usando um CLSID de CLSID \_ InternetShortcut.
2.  Use o método [IUniformResourceLocator:: SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) para definir a URL no atalho.
3.  Use o método [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o arquivo de atalho em um local desejado.

## <a name="accessing-property-storage"></a>acessando a propriedade Armazenamento

O objeto de atalho da Internet contém várias propriedades que você pode acessar por meio da interface [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) do objeto com o procedimento a seguir.

1.  Obtenha a interface [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) chamando [QUERYINTERFACE](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) com IPropertySetStorage IID \_ .
2.  Acesse o conjunto de armazenamento de propriedade de atalho da Internet chamando [IPropertySetStorage:: Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) com FMTID \_ Intshcut ou FMTID \_ InternetSite para obter a interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) .
3.  Leia as informações de armazenamento de propriedade com [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) passando a ID de propriedade apropriada.

Com a [versão 4,70 ou superior](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) do Shell32.dll, você também pode recuperar a interface [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) chamando [**IShellFolder:: BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) com o parâmetro *PIDL* definido como o. O arquivo de URL e o parâmetro *riid* definido como IID \_ IPropertySetStorage.

As IDs de propriedade a seguir podem ser solicitadas para FMTID \_ Intshcut.



| PROPID               | Tipo de variante | Descrição                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ é \_ URL         | LPWStr do VT \_   | URL para a qual o atalho leva             |
| PID \_ é \_ nome        | LPWStr do VT \_   | Nome do atalho da Internet               |
| PID \_ é \_ WORKINGDIR  | LPWStr do VT \_   | Diretório de trabalho para o atalho          |
| PID \_ é \_ tecla de atalho      | \_UI2 VT      | Tecla de atalho para o atalhos                     |
| PID \_ é \_ SHOWCMD     | \_I4 VT       | Mostrar comando para o atalho                   |
| PID \_ é \_ ICONINDEX   | \_I4 VT       | Índice do ícone                           |
| PID \_ é \_ IconFile    | LPWStr do VT \_   | Arquivo que contém o ícone                 |
| PID \_ é \_ whatsnew    | LPWStr do VT \_   | Texto de novidades                             |
| PID \_ é \_ autor      | LPWStr do VT \_   | Autor                                      |
| PID \_ é \_ Descrição | LPWStr do VT \_   | Texto de descrição do site                    |
| PID \_ é \_ Comentário     | LPWStr do VT \_   | Comentário anotado do usuário                      |
| o PID \_ está em \_ roaming      | BOOL do VT \_     | True quando o atalho estiver em roaming pela primeira vez |



 

As IDs de propriedade a seguir podem ser solicitadas para FMTID \_ InternetSite.



| PROPID                     | Tipo de variante | Descrição                                       |
|----------------------------|--------------|---------------------------------------------------|
| DTI \_ INTSITE \_ whatsnew     | LPWStr do VT \_   | Texto de novidades                                   |
| autor do PID \_ INTSITE \_       | LPWStr do VT \_   | Autor                                            |
| DTI \_ INTSITE \_ LASTVISIT    | FILETIME do VT \_ | Hora em que o site foi visitado pela última vez                        |
| DTI \_ INTSITE \_ LASTMOD      | FILETIME do VT \_ | Hora em que o site foi modificado pela última vez                       |
| DTI \_ INTSITE \_ VISITCOUNT   | \_UI4 VT      | Número de vezes que o usuário visitou                  |
| Descrição da PID \_ INTSITE \_  | LPWStr do VT \_   | Texto de descrição do site                          |
| PID \_ INTSITE \_ COMMENT      | VT \_ LPWSTR   | Comentário anotado pelo usuário                            |
| SINALIZADORES \_ PID INTSITE \_        | VT \_ UI4      | Indica o uso de sinalizadores PIDISF \_ (veja abaixo)       |
| PID \_ INTSITE \_ CONTENTLEN   | N/D          | Sem suporte no momento                           |
| PID \_ INTSITE \_ CONTENTCODE  | N/D          | Sem suporte no momento                           |
| PID \_ INTSITE \_ RECURSE      | N/D          | Sem suporte no momento                           |
| PID \_ INTSITE \_ WATCH        | N/D          | Sem suporte no momento                           |
| ASSINATURA \_ PID \_ INTSITE | VT \_ UI8      | Valor SUBSCRIPTIONCOOKIE para o gerenciador de assinaturas |
| PID \_ INTSITE \_ URL          | VT \_ LPWSTR   | URL para a qual o atalho leva                   |
| PID \_ INTSITE \_ TITLE        | VT \_ LPWSTR   | Título                                             |
| PID \_ INTSITE \_ CODEPAGE     | VT \_ UI4      | Página de código do documento                          |
| PID \_ INTSITE \_ TRACKING     | N/D          | Sem suporte no momento                           |
| ÍCONE \_ DE INTSITE DO \_ PIDINDEX    | VT \_ I4       | Índice do ícone                                 |
| PID \_ INTSITE \_ ICONFILE     | VT \_ LPWSTR   | Arquivo que contém o ícone                       |
| PID \_ INTSITE \_ ROAMED       | VT \_ UI4      | A entrada foi adicionada devido a roaming                |



 

A seguir estão os sinalizadores de site da Internet.



| Sinalizador                    | Descrição                                |
|-------------------------|--------------------------------------------|
| PIDISF \_ RECENTLYCHANGED | Indica que um site foi alterado recentemente |
| PIDISF \_ CACHEDSTICKY    | Sem suporte no momento                    |
| PIDISF \_ CACHEIMAGES     | Sem suporte no momento                    |
| PIDISF \_ FOLLOWALLLINKS  | Sem suporte no momento                    |



 

Os valores a seguir são usados para o histórico de roaming da Internet.



| Valor de PID \_ INTSITE \_ ROAMED         | Descrição                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor não definido ou PIDISR \_ \_ ATUALIZADO \_ | Essa entrada de cache não foi modificada pelo roaming.                                                                                                                       |
| PIDISR \_ PRECISA \_ ADICIONAR                    | Essa entrada de cache foi adicionada ao cache por roaming. De configurar o PIDISR \_ COMO ATUALIZADO quando o processamento da entrada for \_ \_ concluído.                                                   |
| O PIDISR \_ PRECISA DE \_ ATUALIZAÇÃO                 | Essa entrada de cache já existia no computador local, mas foi atualizada por roaming. De configurar o PIDISR \_ COMO ATUALIZADO quando o processamento da entrada for \_ \_ concluído.                 |
| O PIDISR \_ PRECISA DE \_ EXCLUSÃO                 | O roaming detectou que essa entrada de cache deve ser excluída. Por exemplo, o usuário pode ter limpado seu histórico do navegador. Exclua a entrada usando DeleteUrlCacheEntry. |



 

## <a name="interfaces"></a>Interfaces

O objeto de atalho da Internet expõe várias interfaces.

### <a name="ole-interfaces"></a>Interfaces OLE

-   [Idataobject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [Ipersistfile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [Ipersiststream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [Iobjectwithsite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Interfaces de shell

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**IExtractIcon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**INewShortcutHook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**IShellExtInit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**IQueryInfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Funções

Há várias funções de utilitário que podem ser usadas com o objeto de atalho da Internet.

### <a name="internet-shortcut-utility-functions"></a>Funções do utilitário de atalho da Internet

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MIMEAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 