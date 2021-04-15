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
# <a name="adding-icons-previews-and-shortcut-menus"></a><span data-ttu-id="3ff26-103">Adicionando ícones, visualizações e menus de atalho</span><span class="sxs-lookup"><span data-stu-id="3ff26-103">Adding Icons, Previews and Shortcut Menus</span></span>

<span data-ttu-id="3ff26-104">Para garantir que seus dados sejam indexados e apresentados corretamente ao usuário durante as pesquisas, você precisa implementar armazenamentos de dados do Shell (também conhecidos como [extensões de namespace do Shell](../shell/nse-works.md)) e manipuladores de tipo de arquivo (também conhecidos como extensões de Shell, [manipuladores de extensão](../shell/handlers.md)ou manipuladores de extensão de Shell).</span><span class="sxs-lookup"><span data-stu-id="3ff26-104">To ensure that your data is indexed and presented correctly to the user during searches, you need to implement Shell data stores (also known as [Shell Namespace Extensions](../shell/nse-works.md)), and file type handlers (also known as Shell extensions, [extension handlers](../shell/handlers.md), or Shell extension handlers).</span></span>

<span data-ttu-id="3ff26-105">Este tópico descreve as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="3ff26-105">This topic describes the following interfaces:</span></span>

-   [<span data-ttu-id="3ff26-106">Implementando manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="3ff26-106">Implementing File Type Handlers</span></span>](#implementing-file-type-handlers)
    -   [<span data-ttu-id="3ff26-107">IPersist</span><span class="sxs-lookup"><span data-stu-id="3ff26-107">IPersist</span></span>](#ipersist)
    -   [<span data-ttu-id="3ff26-108">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="3ff26-108">IPersistFolder</span></span>](#ipersistfolder)
    -   [<span data-ttu-id="3ff26-109">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="3ff26-109">IShellFolder</span></span>](#ishellfolder)
    -   [<span data-ttu-id="3ff26-110">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="3ff26-110">IContextMenu</span></span>](#icontextmenu)
    -   [<span data-ttu-id="3ff26-111">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="3ff26-111">IExtractIcon</span></span>](#iextracticon)
    -   [<span data-ttu-id="3ff26-112">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="3ff26-112">IPreviewHandler</span></span>](#ipreviewhandler)
-   [<span data-ttu-id="3ff26-113">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="3ff26-113">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="3ff26-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ff26-114">Related topics</span></span>](#related-topics)

## <a name="implementing-file-type-handlers"></a><span data-ttu-id="3ff26-115">Implementando manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="3ff26-115">Implementing File Type Handlers</span></span>

<span data-ttu-id="3ff26-116">Essas extensões de shell ou manipuladores de tipo de arquivo fornecem aos seus usuários as seguintes experiências de Shell:</span><span class="sxs-lookup"><span data-stu-id="3ff26-116">These Shell extensions or file type handlers provide your users with the following Shell experiences:</span></span>

-   <span data-ttu-id="3ff26-117">O modo de exibição de resultados exibe um ícone específico para o tipo de item.</span><span class="sxs-lookup"><span data-stu-id="3ff26-117">The results view displays a specific icon for your item type.</span></span>
-   <span data-ttu-id="3ff26-118">A exibição de resultados exibe uma visualização do item quando o usuário seleciona o item.</span><span class="sxs-lookup"><span data-stu-id="3ff26-118">The results view displays a preview of the item when the user selects the item.</span></span>
-   <span data-ttu-id="3ff26-119">Os usuários podem clicar duas vezes em itens para iniciar eventos, como abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ff26-119">Users can double-click items to initiate events such as opening the file.</span></span>
-   <span data-ttu-id="3ff26-120">Os usuários podem clicar com o botão direito do mouse em itens para acessar um menu de atalho (contexto).</span><span class="sxs-lookup"><span data-stu-id="3ff26-120">Users can right-click items to access a shortcut (context) menu.</span></span>
-   <span data-ttu-id="3ff26-121">Os usuários podem arrastar e soltar itens.</span><span class="sxs-lookup"><span data-stu-id="3ff26-121">Users can drag-and-drop items.</span></span>

<span data-ttu-id="3ff26-122">Como todos os objetos COM (Component Object Model), os manipuladores de tipo de arquivo devem implementar uma interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) e uma fábrica de classes.</span><span class="sxs-lookup"><span data-stu-id="3ff26-122">Like all Component Object Model (COM) objects, file type handlers must implement an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a class factory.</span></span>

<span data-ttu-id="3ff26-123">No Windows XP ou anterior, os manipuladores também devem implementar:</span><span class="sxs-lookup"><span data-stu-id="3ff26-123">In Windows XP or earlier, handlers should also implement:</span></span>

-   <span data-ttu-id="3ff26-124">A [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="3ff26-124">Either [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span></span>
-   <span data-ttu-id="3ff26-125">Ou [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span><span class="sxs-lookup"><span data-stu-id="3ff26-125">Or [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span></span>

<span data-ttu-id="3ff26-126">No Windows Vista, a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e a [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) foram substituídas pelas três interfaces a seguir para que o Shell inicialize o manipulador:</span><span class="sxs-lookup"><span data-stu-id="3ff26-126">In Windows Vista, [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) were replaced by the following three interfaces for Shell to initialize the handler:</span></span>

-   [<span data-ttu-id="3ff26-127">Interface IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="3ff26-127">IInitializeWithStream Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="3ff26-128">Interface IInitializeWithItem</span><span class="sxs-lookup"><span data-stu-id="3ff26-128">IInitializeWithItem Interface</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="3ff26-129">Interface IInitializeWithFile</span><span class="sxs-lookup"><span data-stu-id="3ff26-129">IInitializeWithFile Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="3ff26-130">Para fornecer uma experiência de usuário razoável, você deve fornecer um armazenamento de dados do shell com seu manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3ff26-130">To provide a reasonable user experience you must provide a Shell data store with your protocol handler.</span></span> <span data-ttu-id="3ff26-131">Esse armazenamento de dados serve como a "fábrica" para manipuladores de ícone, manipuladores de menu de atalho, gerenciadores de visualização e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3ff26-131">That data store then serves as the "factory" for icon handlers, shortcut menu handlers, preview handlers, and so forth.</span></span> <span data-ttu-id="3ff26-132">As implementações mínimas da interface [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) e da [interface IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) são exigidas pela [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), e uma implementação mínima da interface IShellFolder é necessária para [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) e [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span><span class="sxs-lookup"><span data-stu-id="3ff26-132">Minimal implementations of [IPersist Interface](/windows/desktop/api/objidl/nn-objidl-ipersist) and [IPersistFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) are required by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), and a minimal implementation of IShellFolder Interface is required for the [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) and [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

> [!Note]  
> <span data-ttu-id="3ff26-133">O mesmo identificador de classe (CLSID) deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="3ff26-133">The same class identifier (CLSID) should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="3ff26-134">Para obter mais informações sobre como criar um armazenamento de dados do Shell para dar suporte a um manipulador de protocolo, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff26-134">For more information about creating a Shell data store to support a protocol handler, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

### <a name="ipersist"></a><span data-ttu-id="3ff26-135">IPersist</span><span class="sxs-lookup"><span data-stu-id="3ff26-135">IPersist</span></span>

<span data-ttu-id="3ff26-136">A interface **IPersist** define o método único **GetClassID**, que é projetado para fornecer o CLSID de um objeto que pode ser armazenado de forma persistente no sistema.</span><span class="sxs-lookup"><span data-stu-id="3ff26-136">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="3ff26-137">Método</span><span class="sxs-lookup"><span data-stu-id="3ff26-137">Method</span></span>     | <span data-ttu-id="3ff26-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ff26-138">Description</span></span>                                      |
|------------|--------------------------------------------------|
| <span data-ttu-id="3ff26-139">GetClassID</span><span class="sxs-lookup"><span data-stu-id="3ff26-139">GetClassID</span></span> | <span data-ttu-id="3ff26-140">Retorna o CLSID do objeto de armazenamento de dados do Shell</span><span class="sxs-lookup"><span data-stu-id="3ff26-140">Returns the CLSID of the Shell data store object</span></span> |



 

### <a name="ipersistfolder"></a><span data-ttu-id="3ff26-141">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="3ff26-141">IPersistFolder</span></span>

<span data-ttu-id="3ff26-142">A interface **IPersistFolder** é usada para inicializar objetos de pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="3ff26-142">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="3ff26-143">A implementação dessa interface, que é derivada de **IPersist**, é como a pasta é informada onde está no namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="3ff26-143">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span> <span data-ttu-id="3ff26-144">Você não usa essa interface diretamente.</span><span class="sxs-lookup"><span data-stu-id="3ff26-144">You do not use this interface directly.</span></span> <span data-ttu-id="3ff26-145">Ele é usado pela implementação do sistema de arquivos do [método IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) quando Inicializa um objeto de pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="3ff26-145">It is used by the file system implementation of [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) when it initializes a Shell folder object.</span></span>



| <span data-ttu-id="3ff26-146">Método</span><span class="sxs-lookup"><span data-stu-id="3ff26-146">Method</span></span>     | <span data-ttu-id="3ff26-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ff26-147">Description</span></span>                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff26-148">Inicializar</span><span class="sxs-lookup"><span data-stu-id="3ff26-148">Initialize</span></span> | <span data-ttu-id="3ff26-149">Instrui um objeto de pasta do Shell para se inicializar com base nas informações passadas e retorna S \_ OK</span><span class="sxs-lookup"><span data-stu-id="3ff26-149">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

### <a name="ishellfolder"></a><span data-ttu-id="3ff26-150">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="3ff26-150">IShellFolder</span></span>

<span data-ttu-id="3ff26-151">A interface de [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) é usada para gerenciar pastas e uma implementação parcial é necessária para que o ícone e interfaces de contexto implementadas para um manipulador de protocolo se comporte corretamente na interface do usuário dos resultados do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3ff26-151">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Search results user interface.</span></span> <span data-ttu-id="3ff26-152">A maior parte da funcionalidade necessária é exposta por meio do método **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="3ff26-152">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="3ff26-153">Esse método permite que um suplemento consulte as interfaces **IExtractIcon** e **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="3ff26-153">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="3ff26-154">A interface de [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) usa PIDLs em vez de URLs.</span><span class="sxs-lookup"><span data-stu-id="3ff26-154">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="3ff26-155">Em contraste com os requisitos de um armazenamento de dados do Shell completo, os suplementos podem usar uma estrutura IDL simples que contém apenas a URL.</span><span class="sxs-lookup"><span data-stu-id="3ff26-155">In contrast to the requirements of a complete Shell data store, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="3ff26-156">Os métodos a seguir da [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) devem ser implementados.</span><span class="sxs-lookup"><span data-stu-id="3ff26-156">The following methods of [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) must be implemented.</span></span> <span data-ttu-id="3ff26-157">Cinco desses métodos exigem implementação mínima.</span><span class="sxs-lookup"><span data-stu-id="3ff26-157">Five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="3ff26-158">Método</span><span class="sxs-lookup"><span data-stu-id="3ff26-158">Method</span></span>           | <span data-ttu-id="3ff26-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ff26-159">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff26-160">BindToObject</span><span class="sxs-lookup"><span data-stu-id="3ff26-160">BindToObject</span></span>     | <span data-ttu-id="3ff26-161">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3ff26-161">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ff26-162">BindToStorage</span><span class="sxs-lookup"><span data-stu-id="3ff26-162">BindToStorage</span></span>    | <span data-ttu-id="3ff26-163">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3ff26-163">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ff26-164">CreateViewObject</span><span class="sxs-lookup"><span data-stu-id="3ff26-164">CreateViewObject</span></span> | <span data-ttu-id="3ff26-165">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3ff26-165">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ff26-166">SetNameOf</span><span class="sxs-lookup"><span data-stu-id="3ff26-166">SetNameOf</span></span>        | <span data-ttu-id="3ff26-167">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3ff26-167">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ff26-168">ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="3ff26-168">ParseDisplayName</span></span> | <span data-ttu-id="3ff26-169">Converte uma URL para a estrutura PIDL</span><span class="sxs-lookup"><span data-stu-id="3ff26-169">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ff26-170">CompareIDs</span><span class="sxs-lookup"><span data-stu-id="3ff26-170">CompareIDs</span></span>       | <span data-ttu-id="3ff26-171">Compara dois valores de PIDL</span><span class="sxs-lookup"><span data-stu-id="3ff26-171">Compares two PIDL values</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3ff26-172">GetDisplayNameOf</span><span class="sxs-lookup"><span data-stu-id="3ff26-172">GetDisplayNameOf</span></span> | <span data-ttu-id="3ff26-173">Retorna a URL para um PIDL</span><span class="sxs-lookup"><span data-stu-id="3ff26-173">Returns the URL for a PIDL</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3ff26-174">GetUIObjectOf</span><span class="sxs-lookup"><span data-stu-id="3ff26-174">GetUIObjectOf</span></span>    | <span data-ttu-id="3ff26-175">Esse método é semelhante ao [método IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="3ff26-175">This method is similar to the [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="3ff26-176">Se um ícone for solicitado, o chamador solicitará o \_ IExtractIcon de IID; se um menu de atalho for solicitado, o chamador solicitará o IContextMenu de IID \_</span><span class="sxs-lookup"><span data-stu-id="3ff26-176">If an icon is requested, the caller requests the IID\_IExtractIcon; if a shortcut menu is requested, the caller requests the IID\_IContextMenu</span></span> |



 

<span data-ttu-id="3ff26-177">**IShellFolder** não é usado para enumerar pastas.</span><span class="sxs-lookup"><span data-stu-id="3ff26-177">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="3ff26-178">Isso significa que o nome de exibição de uma pasta será a URL física.</span><span class="sxs-lookup"><span data-stu-id="3ff26-178">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="3ff26-179">Isso pode ser alterado no futuro.</span><span class="sxs-lookup"><span data-stu-id="3ff26-179">This may change in the future.</span></span>

### <a name="icontextmenu"></a><span data-ttu-id="3ff26-180">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="3ff26-180">IContextMenu</span></span>

<span data-ttu-id="3ff26-181">Quando o Windows Search exibe os resultados para o usuário, o usuário pode clicar com o botão direito do mouse em um item e ver um menu de atalho definido pela sua interface **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="3ff26-181">When Windows Search displays results to the user, the user can right-click an item and see a shortcut menu defined by your **IContextMenu** interface.</span></span> <span data-ttu-id="3ff26-182">Os menus de atalho também são conhecidos como menus de contexto.</span><span class="sxs-lookup"><span data-stu-id="3ff26-182">Shortcut menus are also known as context menus.</span></span>

<span data-ttu-id="3ff26-183">A ação padrão no menu de contexto é a mesma ação executada quando o item é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="3ff26-183">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="3ff26-184">Sem as interfaces **IShellFolder** ou **IContextMenu** correspondentes para o item, o comportamento padrão de um evento de clique duplo é passar a URL como um argumento para a função de [função ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="3ff26-184">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the [ShellExecute Function](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function.</span></span>

<span data-ttu-id="3ff26-185">Consulte [criando manipuladores de menu de contexto](../shell/context-menu-handlers.md) para obter mais informações sobre como criar manipuladores de menu de atalho e [exemplos: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para o código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3ff26-185">Refer to [Creating Context Menu Handlers](../shell/context-menu-handlers.md) for more information on creating shortcut menu handlers, and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="iextracticon"></a><span data-ttu-id="3ff26-186">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="3ff26-186">IExtractIcon</span></span>

<span data-ttu-id="3ff26-187">**IExtractIcon** recupera um ícone para a interface do usuário do Windows Search com base na URL no PIDL fornecido pelo seu manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3ff26-187">**IExtractIcon** retrieves an icon for the Windows Search user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

<span data-ttu-id="3ff26-188">Consulte [criando manipuladores de ícone](../shell/how-to-create-icon-handlers.md) para obter mais informações sobre como criar manipuladores de ícone e [exemplo: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para o código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3ff26-188">Refer to [Creating Icon Handlers](../shell/how-to-create-icon-handlers.md) for more information on creating icon handlers and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="ipreviewhandler"></a><span data-ttu-id="3ff26-189">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="3ff26-189">IPreviewHandler</span></span>

<span data-ttu-id="3ff26-190">O [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renderiza uma visualização avançada de um item selecionado no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ff26-190">The [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renders a rich preview of a selected item in Windows Explorer.</span></span> <span data-ttu-id="3ff26-191">As visualizações estão disponíveis no Windows Search 4,0 ou no Windows Vista com o Windows Desktop Search 3. x.</span><span class="sxs-lookup"><span data-stu-id="3ff26-191">Previews are available in Windows Search 4.0, or in Windows Vista with Windows Desktop Search 3.x.</span></span>

<span data-ttu-id="3ff26-192">Para criar um Gerenciador de visualização personalizado:</span><span class="sxs-lookup"><span data-stu-id="3ff26-192">To create a custom preview handler:</span></span>

1.  <span data-ttu-id="3ff26-193">Implemente um [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) que aceite um [IStream](/windows/win32/api/objidl/nn-objidl-istream), seguindo as diretrizes fornecidas em [gerenciadores de visualização](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="3ff26-193">Implement an [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) that takes an [IStream](/windows/win32/api/objidl/nn-objidl-istream), following the guidelines provided in [Preview Handlers](../shell/preview-handlers.md).</span></span>
2.  <span data-ttu-id="3ff26-194">Registre seu Gerenciador de visualização:</span><span class="sxs-lookup"><span data-stu-id="3ff26-194">Register your preview handler:</span></span>

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

3.  <span data-ttu-id="3ff26-195">Conclua as duas etapas a seguir para implementar uma pasta do Shell para sua URL:</span><span class="sxs-lookup"><span data-stu-id="3ff26-195">Complete the following two steps to implement a Shell folder for your URL:</span></span>
    1.  <span data-ttu-id="3ff26-196">No [método IShellFolder:: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), manipule [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) e retorne sua associação para seus itens de Shell, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ff26-196">In [IShellFolder::GetUIObjectOf Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), handle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) and return your association for your Shell items, as shown in the following code sample.</span></span>

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  <span data-ttu-id="3ff26-197">Depois que o Shell consulta a pasta do Shell para que o fluxo de dados inicialize o Gerenciador de visualização, vá para o método de [método IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , manipule o \_ IStream IID e retorne um [IStream](/windows/win32/api/objidl/nn-objidl-istream) à sua URL.</span><span class="sxs-lookup"><span data-stu-id="3ff26-197">After the Shell queries your Shell folder for the data stream to initialize the preview handler, go to your [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) method, handle IID\_IStream and return an [IStream](/windows/win32/api/objidl/nn-objidl-istream) to your URL.</span></span>

<span data-ttu-id="3ff26-198">Para reutilizar um Gerenciador de visualização existente para o tipo de arquivo, siga estas duas etapas:</span><span class="sxs-lookup"><span data-stu-id="3ff26-198">To reuse an existing preview handler for your file type, follow these two steps:</span></span>

1.  <span data-ttu-id="3ff26-199">Registre esse Gerenciador de visualização para o tipo de arquivo usando o CLSID do Gerenciador de visualização existente no lugar de <seu \_ GUID do PreviewHandler \_>.</span><span class="sxs-lookup"><span data-stu-id="3ff26-199">Register that preview handler for your file type using the CLSID of the existing preview handler in place of <Your\_PreviewHandler\_GUID>.</span></span>
2.  <span data-ttu-id="3ff26-200">Implemente uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="3ff26-200">Implement a Shell folder.</span></span>

<span data-ttu-id="3ff26-201">Para obter mais informações sobre como criar gerenciadores de visualização, consulte [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) e [gerenciadores de visualização](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="3ff26-201">For more information on creating preview handlers, see [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ff26-202">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="3ff26-202">Additional Resources</span></span>

-   <span data-ttu-id="3ff26-203">Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ff26-203">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="3ff26-204">Para obter informações sobre como criar manipuladores, consulte [registrando extensões de shell](../shell/reg-shell-exts.md), [criando manipuladores de extensão de shell](../shell/handlers.md), menu de [contexto](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), extensões de [namespace de shell](../shell/nse-works.md) e [gerenciadores de visualização](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="3ff26-204">For information about creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell Namespace Extensions](../shell/nse-works.md) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ff26-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ff26-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3ff26-206">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="3ff26-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3ff26-207">Desenvolvendo manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ff26-207">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="3ff26-208">Noções básicas sobre manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ff26-208">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="3ff26-209">Notificando o índice das alterações</span><span class="sxs-lookup"><span data-stu-id="3ff26-209">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="3ff26-210">Exemplo de código: extensões de Shell para manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ff26-210">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="3ff26-211">Instalando e Registrando manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ff26-211">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="3ff26-212">Criando um conector de pesquisa para um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ff26-212">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="3ff26-213">Depuração de manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ff26-213">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
