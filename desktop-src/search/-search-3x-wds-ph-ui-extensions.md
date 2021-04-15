---
description: Para garantir que seus dados sejam indexados e apresentados corretamente ao usuário durante as pesquisas, você precisa implementar armazenamentos de dados do Shell (também conhecidos como extensões de namespace do Shell) e manipuladores de tipo de arquivo (também conhecidos como extensões de Shell, manipuladores de extensão ou manipuladores de extensão de Shell).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Adicionando ícones, visualizações e menus de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501482"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a>Adicionando ícones, visualizações e menus de atalho

Para garantir que seus dados sejam indexados e apresentados corretamente ao usuário durante as pesquisas, você precisa implementar armazenamentos de dados do Shell (também conhecidos como [extensões de namespace do Shell](../shell/nse-works.md)) e manipuladores de tipo de arquivo (também conhecidos como extensões de Shell, [manipuladores de extensão](../shell/handlers.md)ou manipuladores de extensão de Shell).

Este tópico descreve as seguintes interfaces:

-   [Implementando manipuladores de tipo de arquivo](#implementing-file-type-handlers)
    -   [IPersist](#ipersist)
    -   [IPersistFolder](#ipersistfolder)
    -   [IShellFolder](#ishellfolder)
    -   [IContextMenu](#icontextmenu)
    -   [IExtractIcon](#iextracticon)
    -   [IPreviewHandler](#ipreviewhandler)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="implementing-file-type-handlers"></a>Implementando manipuladores de tipo de arquivo

Essas extensões de shell ou manipuladores de tipo de arquivo fornecem aos seus usuários as seguintes experiências de Shell:

-   O modo de exibição de resultados exibe um ícone específico para o tipo de item.
-   A exibição de resultados exibe uma visualização do item quando o usuário seleciona o item.
-   Os usuários podem clicar duas vezes em itens para iniciar eventos, como abrir o arquivo.
-   Os usuários podem clicar com o botão direito do mouse em itens para acessar um menu de atalho (contexto).
-   Os usuários podem arrastar e soltar itens.

Como todos os objetos COM (Component Object Model), os manipuladores de tipo de arquivo devem implementar uma interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) e uma fábrica de classes.

No Windows XP ou anterior, os manipuladores também devem implementar:

-   A [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   Ou [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

No Windows Vista, a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e a [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) foram substituídas pelas três interfaces a seguir para que o Shell inicialize o manipulador:

-   [Interface IInitializeWithStream](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [Interface IInitializeWithItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [Interface IInitializeWithFile](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

Para fornecer uma experiência de usuário razoável, você deve fornecer um armazenamento de dados do shell com seu manipulador de protocolo. Esse armazenamento de dados serve como a "fábrica" para manipuladores de ícone, manipuladores de menu de atalho, gerenciadores de visualização e assim por diante. As implementações mínimas da interface [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) e da [interface IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) são exigidas pela [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), e uma implementação mínima da interface IShellFolder é necessária para [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) e [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

> [!Note]  
> O mesmo identificador de classe (CLSID) deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.

 

Para obter mais informações sobre como criar um armazenamento de dados do Shell para dar suporte a um manipulador de protocolo, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="ipersist"></a>IPersist

A interface **IPersist** define o método único **GetClassID**, que é projetado para fornecer o CLSID de um objeto que pode ser armazenado de forma persistente no sistema.



| Método     | Descrição                                      |
|------------|--------------------------------------------------|
| GetClassID | Retorna o CLSID do objeto de armazenamento de dados do Shell |



 

### <a name="ipersistfolder"></a>IPersistFolder

A interface **IPersistFolder** é usada para inicializar objetos de pasta do Shell. A implementação dessa interface, que é derivada de **IPersist**, é como a pasta é informada onde está no namespace do Shell. Você não usa essa interface diretamente. Ele é usado pela implementação do sistema de arquivos do [método IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) quando Inicializa um objeto de pasta do Shell.



| Método     | Descrição                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| Inicializar | Instrui um objeto de pasta do Shell para se inicializar com base nas informações passadas e retorna S \_ OK |



 

### <a name="ishellfolder"></a>IShellFolder

A interface de [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) é usada para gerenciar pastas e uma implementação parcial é necessária para que o ícone e interfaces de contexto implementadas para um manipulador de protocolo se comporte corretamente na interface do usuário dos resultados do Windows Search. A maior parte da funcionalidade necessária é exposta por meio do método **GetUIObjectOf** . Esse método permite que um suplemento consulte as interfaces **IExtractIcon** e **IContextMenu** .

A interface de [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) usa PIDLs em vez de URLs. Em contraste com os requisitos de um armazenamento de dados do Shell completo, os suplementos podem usar uma estrutura IDL simples que contém apenas a URL.

Os métodos a seguir da [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) devem ser implementados. Cinco desses métodos exigem implementação mínima.



| Método           | Descrição                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject     | Retorna E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| BindToStorage    | Retorna E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| CreateViewObject | Retorna E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| SetNameOf        | Retorna E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| ParseDisplayName | Converte uma URL para a estrutura PIDL                                                                                                                                                                                                                                          |
| CompareIDs       | Compara dois valores de PIDL                                                                                                                                                                                                                                                      |
| GetDisplayNameOf | Retorna a URL para um PIDL                                                                                                                                                                                                                                                    |
| GetUIObjectOf    | Esse método é semelhante ao [método IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Se um ícone for solicitado, o chamador solicitará o \_ IExtractIcon de IID; se um menu de atalho for solicitado, o chamador solicitará o IContextMenu de IID \_ |



 

**IShellFolder** não é usado para enumerar pastas. Isso significa que o nome de exibição de uma pasta será a URL física. Isso pode ser alterado no futuro.

### <a name="icontextmenu"></a>IContextMenu

Quando o Windows Search exibe os resultados para o usuário, o usuário pode clicar com o botão direito do mouse em um item e ver um menu de atalho definido pela sua interface **IContextMenu** . Os menus de atalho também são conhecidos como menus de contexto.

A ação padrão no menu de contexto é a mesma ação executada quando o item é clicado duas vezes. Sem as interfaces **IShellFolder** ou **IContextMenu** correspondentes para o item, o comportamento padrão de um evento de clique duplo é passar a URL como um argumento para a função de [função ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .

Consulte [criando manipuladores de menu de contexto](../shell/context-menu-handlers.md) para obter mais informações sobre como criar manipuladores de menu de atalho e [exemplos: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para o código de exemplo.

### <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** recupera um ícone para a interface do usuário do Windows Search com base na URL no PIDL fornecido pelo seu manipulador de protocolo.

Consulte [criando manipuladores de ícone](../shell/how-to-create-icon-handlers.md) para obter mais informações sobre como criar manipuladores de ícone e [exemplo: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para o código de exemplo.

### <a name="ipreviewhandler"></a>IPreviewHandler

O [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renderiza uma visualização avançada de um item selecionado no Windows Explorer. As visualizações estão disponíveis no Windows Search 4,0 ou no Windows Vista com o Windows Desktop Search 3. x.

Para criar um Gerenciador de visualização personalizado:

1.  Implemente um [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) que aceite um [IStream](/windows/win32/api/objidl/nn-objidl-istream), seguindo as diretrizes fornecidas em [gerenciadores de visualização](../shell/preview-handlers.md).
2.  Registre seu Gerenciador de visualização:

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  Conclua as duas etapas a seguir para implementar uma pasta do Shell para sua URL:
    1.  No [método IShellFolder:: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), manipule [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) e retorne sua associação para seus itens de Shell, conforme mostrado no exemplo de código a seguir.

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  Depois que o Shell consulta a pasta do Shell para que o fluxo de dados inicialize o Gerenciador de visualização, vá para o método de [método IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , manipule o \_ IStream IID e retorne um [IStream](/windows/win32/api/objidl/nn-objidl-istream) à sua URL.

Para reutilizar um Gerenciador de visualização existente para o tipo de arquivo, siga estas duas etapas:

1.  Registre esse Gerenciador de visualização para o tipo de arquivo usando o CLSID do Gerenciador de visualização existente no lugar de <seu \_ GUID do PreviewHandler \_>.
2.  Implemente uma pasta do Shell.

Para obter mais informações sobre como criar gerenciadores de visualização, consulte [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) e [gerenciadores de visualização](../shell/preview-handlers.md).

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
-   Para obter informações sobre como criar manipuladores, consulte [registrando extensões de shell](../shell/reg-shell-exts.md), [criando manipuladores de extensão de shell](../shell/handlers.md), menu de [contexto](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), extensões de [namespace de shell](../shell/nse-works.md) e [gerenciadores de visualização](../shell/preview-handlers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Noções básicas sobre manipuladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Notificando o índice das alterações](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Exemplo de código: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalando e Registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Criando um conector de pesquisa para um manipulador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Depuração de manipuladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
