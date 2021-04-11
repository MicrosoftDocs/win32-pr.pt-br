---
title: Adicionando ícones e menus de contexto com extensões de Shell
description: Você pode melhorar a experiência de seus usuários com o Microsoft Windows Desktop Search (WDS) e o manipulador de protocolo implementando extensões de Shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "104161801"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a><span data-ttu-id="c16b6-103">Adicionando ícones e menus de contexto com extensões de Shell</span><span class="sxs-lookup"><span data-stu-id="c16b6-103">Adding Icons and Context Menus with Shell Extensions</span></span>

> [!NOTE]
> <span data-ttu-id="c16b6-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c16b6-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c16b6-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c16b6-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="c16b6-106">Você pode melhorar a experiência de seus usuários com o Microsoft Windows Desktop Search (WDS) e o manipulador de protocolo implementando extensões de Shell.</span><span class="sxs-lookup"><span data-stu-id="c16b6-106">You can improve your users' experience with Microsoft Windows Desktop Search (WDS) and your protocol handler by implementing Shell extensions.</span></span> <span data-ttu-id="c16b6-107">Sem a extensão adicional, o manipulador de protocolo que você criar não incluirá as seguintes experiências de usuário:</span><span class="sxs-lookup"><span data-stu-id="c16b6-107">Without further extension, the protocol handler you create will not include the following user experiences:</span></span>

-   <span data-ttu-id="c16b6-108">O WDS não exibirá ícones específicos para seus resultados.</span><span class="sxs-lookup"><span data-stu-id="c16b6-108">WDS will not display specific icons for your results.</span></span>
-   <span data-ttu-id="c16b6-109">Quando os usuários clicam duas vezes em um item, a interface do usuário não responderá ao evento.</span><span class="sxs-lookup"><span data-stu-id="c16b6-109">When users double-click an item, the user interface will not respond to the event.</span></span>
-   <span data-ttu-id="c16b6-110">Quando os usuários clicam com o botão direito do mouse em um item, o menu de contexto não oferece suporte a nenhuma operação para o item.</span><span class="sxs-lookup"><span data-stu-id="c16b6-110">When users right-click an item, the context menu will not support any operations for the item.</span></span>

<span data-ttu-id="c16b6-111">As implementações mínimas de **IPersist** e **IPersistFolder** são exigidas pelo **IShellFolder** e uma implementação mínima de **IShellFolder** é necessária para **IContextMenu** e **IExtractIcon**, as duas interfaces que fornecem uma experiência de usuário mais direta.</span><span class="sxs-lookup"><span data-stu-id="c16b6-111">Minimal implementations of **IPersist** and **IPersistFolder** are required by **IShellFolder**, and a minimal implementation of **IShellFolder** is required for **IContextMenu** and **IExtractIcon**, the two interfaces that provide a more seamless user experience.</span></span>

 

## <a name="ipersist"></a><span data-ttu-id="c16b6-112">IPersist</span><span class="sxs-lookup"><span data-stu-id="c16b6-112">IPersist</span></span>

<span data-ttu-id="c16b6-113">A interface **IPersist** define o método único **GetClassID**, que é projetado para fornecer o CLSID de um objeto que pode ser armazenado de forma persistente no sistema.</span><span class="sxs-lookup"><span data-stu-id="c16b6-113">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="c16b6-114">Método</span><span class="sxs-lookup"><span data-stu-id="c16b6-114">Method</span></span>       | <span data-ttu-id="c16b6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c16b6-115">Description</span></span>                                 |
|--------------|---------------------------------------------|
| <span data-ttu-id="c16b6-116">GetClassID ()</span><span class="sxs-lookup"><span data-stu-id="c16b6-116">GetClassID()</span></span> | <span data-ttu-id="c16b6-117">Retorna a ClassID do manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c16b6-117">Returns the ClassID of the protocol handler</span></span> |



 

> [!Note]
>
> <span data-ttu-id="c16b6-118">O mesmo CLSID deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="c16b6-118">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

 

## <a name="ipersistfolder"></a><span data-ttu-id="c16b6-119">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="c16b6-119">IPersistFolder</span></span>

<span data-ttu-id="c16b6-120">A interface **IPersistFolder** é usada para inicializar objetos de pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="c16b6-120">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="c16b6-121">A implementação dessa interface, que é derivada de **IPersist**, é como a pasta é informada onde está no namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="c16b6-121">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span>



| <span data-ttu-id="c16b6-122">Método</span><span class="sxs-lookup"><span data-stu-id="c16b6-122">Method</span></span>       | <span data-ttu-id="c16b6-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="c16b6-123">Description</span></span>                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16b6-124">Initialize ()</span><span class="sxs-lookup"><span data-stu-id="c16b6-124">Initialize()</span></span> | <span data-ttu-id="c16b6-125">Instrui um objeto de pasta do Shell para se inicializar com base nas informações passadas e retorna S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c16b6-125">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

> [!Note]
>
> <span data-ttu-id="c16b6-126">O mesmo CLSID deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="c16b6-126">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="c16b6-127">Você não usa essa interface diretamente.</span><span class="sxs-lookup"><span data-stu-id="c16b6-127">You do not use this interface directly.</span></span> <span data-ttu-id="c16b6-128">Ele é usado pela implementação do sistema de arquivos da interface IShellFolder:: BindToObject quando Inicializa um objeto de pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="c16b6-128">It is used by the file system implementation of the IShellFolder::BindToObject interface when it initializes a Shell folder object.</span></span>

 

## <a name="ishellfolder"></a><span data-ttu-id="c16b6-129">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="c16b6-129">IShellFolder</span></span>

<span data-ttu-id="c16b6-130">A interface **IShellFolder** é usada para gerenciar pastas e uma implementação parcial é necessária para que o ícone e as interfaces de contexto implementadas para um manipulador de protocolo se comporte corretamente na interface de usuário dos resultados do Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="c16b6-130">The **IShellFolder** interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Desktop Search results user interface.</span></span> <span data-ttu-id="c16b6-131">A maior parte da funcionalidade necessária é exposta por meio do método **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="c16b6-131">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="c16b6-132">Esse método permite que um suplemento consulte as interfaces **IExtractIcon** e **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="c16b6-132">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="c16b6-133">A interface **IShellFolder** usa PIDLs em vez de URLs.</span><span class="sxs-lookup"><span data-stu-id="c16b6-133">The **IShellFolder** interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="c16b6-134">Ao contrário dos requisitos de uma extensão de namespace completa, os suplementos podem usar uma estrutura IDL simples que contém apenas a URL.</span><span class="sxs-lookup"><span data-stu-id="c16b6-134">In contrast to the requirements of a complete Namespace extension, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="c16b6-135">Os métodos a seguir de **IShellFolder** devem ser implementados.</span><span class="sxs-lookup"><span data-stu-id="c16b6-135">The following methods of **IShellFolder** must be implemented.</span></span> <span data-ttu-id="c16b6-136">Observe que cinco desses métodos exigem implementação mínima.</span><span class="sxs-lookup"><span data-stu-id="c16b6-136">Note that five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="c16b6-137">Método</span><span class="sxs-lookup"><span data-stu-id="c16b6-137">Method</span></span>             | <span data-ttu-id="c16b6-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="c16b6-138">Description</span></span>                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16b6-139">BindToObject()</span><span class="sxs-lookup"><span data-stu-id="c16b6-139">BindToObject()</span></span>     | <span data-ttu-id="c16b6-140">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c16b6-140">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c16b6-141">BindToStorage()</span><span class="sxs-lookup"><span data-stu-id="c16b6-141">BindToStorage()</span></span>    | <span data-ttu-id="c16b6-142">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c16b6-142">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c16b6-143">CreateViewObject ()</span><span class="sxs-lookup"><span data-stu-id="c16b6-143">CreateViewObject()</span></span> | <span data-ttu-id="c16b6-144">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c16b6-144">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c16b6-145">SetNameOf()</span><span class="sxs-lookup"><span data-stu-id="c16b6-145">SetNameOf()</span></span>        | <span data-ttu-id="c16b6-146">Retorna E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c16b6-146">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c16b6-147">ParseDisplayName()</span><span class="sxs-lookup"><span data-stu-id="c16b6-147">ParseDisplayName()</span></span> | <span data-ttu-id="c16b6-148">Converte uma URL para a estrutura PIDL</span><span class="sxs-lookup"><span data-stu-id="c16b6-148">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c16b6-149">CompareIDs()</span><span class="sxs-lookup"><span data-stu-id="c16b6-149">CompareIDs()</span></span>       | <span data-ttu-id="c16b6-150">Compara dois valores de PIDL</span><span class="sxs-lookup"><span data-stu-id="c16b6-150">Compares two PIDL values</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="c16b6-151">GetDisplayNameOf()</span><span class="sxs-lookup"><span data-stu-id="c16b6-151">GetDisplayNameOf()</span></span> | <span data-ttu-id="c16b6-152">Retorna a URL para um PIDL</span><span class="sxs-lookup"><span data-stu-id="c16b6-152">Returns the URL for a PIDL</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="c16b6-153">GetUIObjectOf()</span><span class="sxs-lookup"><span data-stu-id="c16b6-153">GetUIObjectOf()</span></span>    | <span data-ttu-id="c16b6-154">Esse método é semelhante ao método OLE COM QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="c16b6-154">This method is similar to the OLE COM QueryInterface method.</span></span> <span data-ttu-id="c16b6-155">Se um ícone for solicitado, o chamador solicitará o \_ IExtractIcon de IID; se um menu de contexto for solicitado, o chamador solicitará o IContextMenu de IID \_ .</span><span class="sxs-lookup"><span data-stu-id="c16b6-155">If an icon is requested, the caller requests the IID\_IExtractIcon; if a context menu is requested, the caller requests the IID\_IContextMenu.</span></span> |



 

> [!Note]
>
> <span data-ttu-id="c16b6-156">O mesmo CLSID deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="c16b6-156">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="c16b6-157">**IShellFolder** não é usado para enumerar pastas.</span><span class="sxs-lookup"><span data-stu-id="c16b6-157">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="c16b6-158">Isso significa que o nome de exibição de uma pasta será a URL física.</span><span class="sxs-lookup"><span data-stu-id="c16b6-158">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="c16b6-159">Isso pode ser alterado no futuro.</span><span class="sxs-lookup"><span data-stu-id="c16b6-159">This may change in the future.</span></span>

 

## <a name="icontextmenu"></a><span data-ttu-id="c16b6-160">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="c16b6-160">IContextMenu</span></span>

<span data-ttu-id="c16b6-161">Quando o WDS exibe os resultados para o usuário, o usuário pode clicar com o botão direito do mouse em um item e ver um menu de contexto definido pela sua interface **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="c16b6-161">When WDS displays results to the user, the user can right-click an item and see a context menu defined by your **IContextMenu** interface.</span></span>

<span data-ttu-id="c16b6-162">A ação padrão no menu de contexto é a mesma ação executada quando o item é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="c16b6-162">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="c16b6-163">Sem as interfaces **IShellFolder** ou **IContextMenu** correspondentes para o item, o comportamento padrão de um evento de clique duplo é passar a URL como um argumento para a função ShellExecute.</span><span class="sxs-lookup"><span data-stu-id="c16b6-163">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the ShellExecute function.</span></span>

 

## <a name="iextracticon"></a><span data-ttu-id="c16b6-164">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="c16b6-164">IExtractIcon</span></span>

<span data-ttu-id="c16b6-165">**IExtractIcon** recupera um ícone para a interface do usuário do WDS com base na URL no PIDL fornecido pelo seu manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c16b6-165">**IExtractIcon** retrieves an icon for the WDS user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

 

## <a name="code-sample"></a><span data-ttu-id="c16b6-166">Exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c16b6-166">Code Sample</span></span>

<span data-ttu-id="c16b6-167">O [código de exemplo da interface do usuário do manipulador de protocolo personalizado](-search-2x-wds-ph-ui-samplecode.md) demonstra uma implementação de **IShellFolder** e interfaces de suporte e inclui suporte para manipular o PIDLs.</span><span class="sxs-lookup"><span data-stu-id="c16b6-167">The [Custom Protocol Handler User Interface Sample Code](-search-2x-wds-ph-ui-samplecode.md) demonstrates an implementation of **IShellFolder** and supporting interfaces and includes support for manipulating the PIDLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c16b6-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c16b6-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c16b6-169">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c16b6-169">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c16b6-170">Código de exemplo da interface do usuário do manipulador de protocolo personalizado</span><span class="sxs-lookup"><span data-stu-id="c16b6-170">Custom Protocol Handler User Interface Sample Code</span></span>](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="c16b6-171">Instalando e Registrando manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="c16b6-171">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




