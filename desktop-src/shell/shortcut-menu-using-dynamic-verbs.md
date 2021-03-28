---
description: Os manipuladores de menu de atalho também são conhecidos como manipuladores de menu de contexto ou manipuladores de verbo. Um manipulador de menu de atalho é um tipo de manipulador de tipo de arquivo.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalizando um menu de atalho usando verbos dinâmicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968058"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a><span data-ttu-id="01905-104">Personalizando um menu de atalho usando verbos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="01905-104">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>

<span data-ttu-id="01905-105">Os manipuladores de menu de atalho também são conhecidos como manipuladores de menu de contexto ou manipuladores de verbo.</span><span class="sxs-lookup"><span data-stu-id="01905-105">Shortcut menu handlers are also known as context menu handlers or verb handlers.</span></span> <span data-ttu-id="01905-106">Um manipulador de menu de atalho é um tipo de manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="01905-106">A shortcut menu handler is a type of file type handler.</span></span>

<span data-ttu-id="01905-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="01905-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="01905-108">Sobre verbos estáticos e dinâmicos</span><span class="sxs-lookup"><span data-stu-id="01905-108">About Static and Dynamic Verbs</span></span>](#about-static-and-dynamic-verbs)
-   [<span data-ttu-id="01905-109">Como os manipuladores de menu de atalho funcionam com verbos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="01905-109">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [<span data-ttu-id="01905-110">Evitando colisões devido a nomes de verbo não qualificados</span><span class="sxs-lookup"><span data-stu-id="01905-110">Avoiding Collisions Due to Unqualified Verb Names</span></span>](#avoiding-collisions-due-to-unqualified-verb-names)
-   [<span data-ttu-id="01905-111">Registrando um manipulador de menu de atalho com um verbo dinâmico</span><span class="sxs-lookup"><span data-stu-id="01905-111">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [<span data-ttu-id="01905-112">Implementando a interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="01905-112">Implementing the IContextMenu Interface</span></span>](#implementing-the-icontextmenu-interface)
    -   [<span data-ttu-id="01905-113">Método IContextMenu:: GetCommandString</span><span class="sxs-lookup"><span data-stu-id="01905-113">IContextMenu::GetCommandString Method</span></span>](#icontextmenugetcommandstring-method)
    -   [<span data-ttu-id="01905-114">Método IContextMenu:: InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="01905-114">IContextMenu::InvokeCommand Method</span></span>](#icontextmenuinvokecommand-method)
    -   [<span data-ttu-id="01905-115">Método IContextMenu:: QueryContextMenu</span><span class="sxs-lookup"><span data-stu-id="01905-115">IContextMenu::QueryContextMenu Method</span></span>](#icontextmenuquerycontextmenu-method)
-   [<span data-ttu-id="01905-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01905-116">Related topics</span></span>](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a><span data-ttu-id="01905-117">Sobre verbos estáticos e dinâmicos</span><span class="sxs-lookup"><span data-stu-id="01905-117">About Static and Dynamic Verbs</span></span>

<span data-ttu-id="01905-118">Recomendamos que você implemente um menu de atalho usando um dos métodos de verbo estáticos.</span><span class="sxs-lookup"><span data-stu-id="01905-118">We strongly encourage you to implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="01905-119">Recomendamos que você siga as instruções fornecidas na seção "Personalizando um menu de atalho usando verbos estáticos" de [criando manipuladores de menu de contexto](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01905-119">We recommend that you follow the instructions provided in the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="01905-120">Para obter um comportamento dinâmico para verbos estáticos no Windows 7 e posterior, consulte "obtendo comportamento dinâmico para verbos estáticos" na [criação de manipuladores de menu de contexto](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01905-120">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="01905-121">Para obter detalhes sobre a implementação de verbo estático e quais verbos dinâmicos evitar, consulte [escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="01905-121">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>

<span data-ttu-id="01905-122">Se você precisar estender o menu de atalho para um tipo de arquivo registrando um verbo dinâmico para o tipo de arquivo, siga as instruções fornecidas mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="01905-122">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided later in this topic.</span></span>

> [!Note]  
> <span data-ttu-id="01905-123">Há considerações especiais para o Windows de 64 bits ao registrar manipuladores que funcionam no contexto de aplicativos de 32 bits: quando os verbos do shell são invocados no contexto de um aplicativo de 32 bits, o subsistema WOW64 redireciona o acesso ao sistema de arquivos para alguns caminhos.</span><span class="sxs-lookup"><span data-stu-id="01905-123">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="01905-124">Se o manipulador. exe for armazenado em um desses caminhos, ele não estará acessível neste contexto.</span><span class="sxs-lookup"><span data-stu-id="01905-124">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="01905-125">Portanto, como uma solução alternativa, armazene seu. exe em um caminho que não seja redirecionado ou armazene uma versão de stub do seu. exe que inicia a versão real.</span><span class="sxs-lookup"><span data-stu-id="01905-125">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a><span data-ttu-id="01905-126">Como os manipuladores de menu de atalho funcionam com verbos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="01905-126">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>

<span data-ttu-id="01905-127">Além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), os manipuladores de menu de atalho exportam as seguintes interfaces adicionais para lidar com as mensagens necessárias para implementar os itens de menu desenhados pelo proprietário:</span><span class="sxs-lookup"><span data-stu-id="01905-127">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), shortcut menu handlers export the following additional interfaces to handle the messaging needed to implement owner-drawn menu items:</span></span>

-   <span data-ttu-id="01905-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="01905-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (mandatory)</span></span>
-   <span data-ttu-id="01905-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="01905-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (mandatory)</span></span>
-   <span data-ttu-id="01905-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (opcional)</span><span class="sxs-lookup"><span data-stu-id="01905-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span></span>
-   <span data-ttu-id="01905-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (opcional)</span><span class="sxs-lookup"><span data-stu-id="01905-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span></span>

<span data-ttu-id="01905-132">Para obter mais informações sobre itens de menu de desenho proprietário, consulte a seção *criando Owner-Drawn itens de menu* em [usando menus](../menurc/using-menus.md).</span><span class="sxs-lookup"><span data-stu-id="01905-132">For more information on owner-drawn menu items, see the *Creating Owner-Drawn Menu Items* section in [Using Menus](../menurc/using-menus.md).</span></span>

<span data-ttu-id="01905-133">O Shell usa a interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para inicializar o manipulador.</span><span class="sxs-lookup"><span data-stu-id="01905-133">Shell uses the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface to initialize the handler.</span></span> <span data-ttu-id="01905-134">Quando o Shell chama [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), ele passa um objeto de dados com o nome do objeto e um ponteiro para uma PIDL (lista de identificadores de item) da pasta que contém o arquivo.</span><span class="sxs-lookup"><span data-stu-id="01905-134">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name and a pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="01905-135">O parâmetro *hkeyProgID* é o local do registro sob o qual o identificador do menu de atalho é registrado.</span><span class="sxs-lookup"><span data-stu-id="01905-135">The *hkeyProgID* parameter is the registry location under which the shortcut menu handle is registered.</span></span> <span data-ttu-id="01905-136">O método **IShellExtInit:: Initialize** deve extrair o nome do arquivo do objeto de dados e armazenar o nome e o ponteiro da pasta para uma PIDL (lista de identificadores de item) para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="01905-136">The **IShellExtInit::Initialize** method must extract the file name from the data object and store the name and the folder's pointer to an item identifier list (PIDL) for later use.</span></span> <span data-ttu-id="01905-137">Para obter mais informações sobre a inicialização do manipulador, consulte [implementando IShellExtInit](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01905-137">For more information on handler initialization, see [Implementing IShellExtInit](handlers.md).</span></span>

<span data-ttu-id="01905-138">Quando os verbos são apresentados em um menu de atalho, eles são descobertos primeiro, apresentados ao usuário e finalmente invocados.</span><span class="sxs-lookup"><span data-stu-id="01905-138">When verbs are presented in a shortcut menu, they are first discovered, then presented to the user, and finally invoked.</span></span> <span data-ttu-id="01905-139">A lista a seguir descreve essas três etapas mais detalhadamente:</span><span class="sxs-lookup"><span data-stu-id="01905-139">The following list describes these three steps in more detail:</span></span>

1.  <span data-ttu-id="01905-140">O Shell chama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que retorna um conjunto de verbos que podem ser baseados no estado dos itens ou do sistema.</span><span class="sxs-lookup"><span data-stu-id="01905-140">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which returns a set of verbs that can be based on the state of the items or the system.</span></span>
2.  <span data-ttu-id="01905-141">O sistema passa um identificador **HMENU** que o método pode usar para adicionar itens ao menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="01905-141">The system passes in an **HMENU** handle that the method can use to add items to the shortcut menu.</span></span>
3.  <span data-ttu-id="01905-142">Se o usuário clicar em um dos itens do manipulador, o Shell chamará [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="01905-142">If the user clicks one of the handler's items, the Shell calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span> <span data-ttu-id="01905-143">O manipulador pode então executar o comando apropriado.</span><span class="sxs-lookup"><span data-stu-id="01905-143">The handler can then execute the appropriate command.</span></span>

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a><span data-ttu-id="01905-144">Evitando colisões devido a nomes de verbo não qualificados</span><span class="sxs-lookup"><span data-stu-id="01905-144">Avoiding Collisions Due to Unqualified Verb Names</span></span>

<span data-ttu-id="01905-145">Como os verbos são registrados por tipo, o mesmo nome de verbo pode ser usado para verbos em itens diferentes.</span><span class="sxs-lookup"><span data-stu-id="01905-145">Because verbs are registered per type, the same verb name can be used for verbs on different items.</span></span> <span data-ttu-id="01905-146">Isso permite que os aplicativos façam referência a verbos comuns independentes do tipo de item.</span><span class="sxs-lookup"><span data-stu-id="01905-146">Doing so enables applications to refer to common verbs independent of the item type.</span></span> <span data-ttu-id="01905-147">Embora essa funcionalidade seja útil, o uso de nomes não qualificados pode resultar em colisões com vários fornecedores independentes de software (ISVs) que escolhem o mesmo nome de verbo.</span><span class="sxs-lookup"><span data-stu-id="01905-147">While this functionality is useful, the use of unqualified names can result in collisions with multiple independent software vendors (ISVs) that choose the same verb name.</span></span> <span data-ttu-id="01905-148">Para evitar isso, sempre Prefixe os verbos com o nome do ISV da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="01905-148">To avoid this, always prefix verbs with the ISV name as follows:</span></span>

`ISV_Name.verb`

<span data-ttu-id="01905-149">Sempre use um ProgID específico do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01905-149">Always use an application specific ProgID.</span></span> <span data-ttu-id="01905-150">A adoção da Convenção de mapeamento da extensão de nome de arquivo para um ProgID fornecido pelo ISV evita colisões em potencial.</span><span class="sxs-lookup"><span data-stu-id="01905-150">Adopting the convention of mapping the file name extension to an ISV provided ProgID avoids potential collisions.</span></span> <span data-ttu-id="01905-151">No entanto, como alguns tipos de item não usam esse mapeamento, há uma necessidade de nomes exclusivos de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="01905-151">However, because some item types do not use this mapping, there is a need for vendor-unique names.</span></span> <span data-ttu-id="01905-152">Ao adicionar um verbo a um ProgID existente que pode já ter esse verbo registrado, você deve primeiro remover a chave do registro do verbo antigo antes de adicionar seu próprio verbo.</span><span class="sxs-lookup"><span data-stu-id="01905-152">When adding a verb to an existing ProgID that might already have that verb registered, you must first remove the registry key for the old verb before adding your own verb.</span></span> <span data-ttu-id="01905-153">Você deve fazer isso para evitar a mesclagem das informações de verbo dos dois verbos.</span><span class="sxs-lookup"><span data-stu-id="01905-153">You must do so to avoid merging the verb information from the two verbs.</span></span> <span data-ttu-id="01905-154">A falha em fazer isso resulta em um comportamento imprevisível.</span><span class="sxs-lookup"><span data-stu-id="01905-154">Failure to do so results in unpredictable behavior.</span></span>

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a><span data-ttu-id="01905-155">Registrando um manipulador de menu de atalho com um verbo dinâmico</span><span class="sxs-lookup"><span data-stu-id="01905-155">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>

<span data-ttu-id="01905-156">Os manipuladores de menu de atalho são associados a um tipo de arquivo ou a uma pasta.</span><span class="sxs-lookup"><span data-stu-id="01905-156">Shortcut menu handlers are associated with either a file type or a folder.</span></span> <span data-ttu-id="01905-157">Para tipos de arquivo, o manipulador é registrado na subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="01905-157">For file types, the handler is registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="01905-158">Para associar um manipulador de menu de atalho a um tipo de arquivo ou uma pasta, primeiro crie uma subchave na subchave **ContextMenuHandlers** .</span><span class="sxs-lookup"><span data-stu-id="01905-158">To associate a shortcut menu handler with either a file type or a folder, first create a subkey under the **ContextMenuHandlers** subkey.</span></span> <span data-ttu-id="01905-159">Nomeie a subchave para o manipulador e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador.</span><span class="sxs-lookup"><span data-stu-id="01905-159">Name the subkey for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="01905-160">Em seguida, para associar um manipulador de menu de atalho a diferentes tipos de pastas, registre o manipulador da mesma maneira que você faria para um tipo de arquivo, mas sob a subchave *FolderType* , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="01905-160">Then to associate a shortcut menu handler with different kinds of folders, register the handler the same way you would for a file type, but under the *FolderType* subkey as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="01905-161">Para obter mais informações sobre a quais tipos de pasta você pode registrar manipuladores, consulte [Registrando manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01905-161">For more information about about which folder types you can register handlers for, see [Registering Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="01905-162">Se um tipo de arquivo tiver um menu de atalho associado a ele, clicar duas vezes em um objeto normalmente iniciará o comando padrão e o método [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) do manipulador não será chamado.</span><span class="sxs-lookup"><span data-stu-id="01905-162">If a file type has a shortcut menu associated with it, then double-clicking an object normally launches the default command, and the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method is not called.</span></span> <span data-ttu-id="01905-163">Para especificar que o método **IContextMenu:: QueryContextMenu** do manipulador deve ser chamado quando um objeto for clicado duas vezes, crie uma subchave na subchave **CLSID** do manipulador, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="01905-163">To specify that the handler's **IContextMenu::QueryContextMenu** method should be called when an object is double-clicked, create a subkey under the handler's **CLSID** subkey as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

<span data-ttu-id="01905-164">Quando um objeto associado ao manipulador é clicado duas vezes, [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) é chamado com o **sinalizador \_ DefaultOnly CMF** definido no parâmetro *uFlags* .</span><span class="sxs-lookup"><span data-stu-id="01905-164">When an object associated with the handler is double-clicked, [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) is called with the **CMF\_DEFAULTONLY** flag set in the *uFlags* parameter.</span></span>

<span data-ttu-id="01905-165">Os manipuladores de menu de atalho devem definir a subchave **MayChangeDefaultMenu** somente se talvez precisem alterar o verbo padrão do menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="01905-165">Shortcut menu handlers should set the **MayChangeDefaultMenu** subkey only if they might need to change the shortcut menu's default verb.</span></span> <span data-ttu-id="01905-166">Definir essa subchave força o sistema a carregar a DLL do manipulador quando um item associado é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="01905-166">Setting this subkey forces the system to load the handler's DLL when an associated item is double-clicked.</span></span> <span data-ttu-id="01905-167">Se o seu manipulador não alterar o verbo padrão, você não deverá definir essa subchave porque fazer isso faz com que o sistema carregue sua DLL desnecessariamente.</span><span class="sxs-lookup"><span data-stu-id="01905-167">If your handler does not change the default verb, you should not set this subkey because doing so causes the system to load your DLL unnecessarily.</span></span>

<span data-ttu-id="01905-168">O exemplo a seguir ilustra as entradas do registro que habilitam um manipulador de menu de atalho para um tipo de arquivo. MYP.</span><span class="sxs-lookup"><span data-stu-id="01905-168">The following example illustrates registry entries that enable a shortcut menu handler for an .myp file type.</span></span> <span data-ttu-id="01905-169">A subchave **CLSID** do manipulador inclui uma subchave **MayChangeDefaultMenu** para garantir que o manipulador seja chamado quando o usuário clicar duas vezes em um objeto relacionado.</span><span class="sxs-lookup"><span data-stu-id="01905-169">The handler's **CLSID** subkey includes a **MayChangeDefaultMenu** subkey to guarantee that the handler is called when the user double-clicks a related object.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a><span data-ttu-id="01905-170">Implementando a interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="01905-170">Implementing the IContextMenu Interface</span></span>

<span data-ttu-id="01905-171">O [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) é o mais potente, mas também o método mais complicado para implementar.</span><span class="sxs-lookup"><span data-stu-id="01905-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="01905-172">É altamente recomendável que você implemente um verbo usando um dos métodos de verbo estáticos.</span><span class="sxs-lookup"><span data-stu-id="01905-172">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="01905-173">Para obter mais informações, consulte [escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="01905-173">For more information, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span> <span data-ttu-id="01905-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tem três métodos, **GetCommandString**, **InvokeCommand** e **QueryContextMenu**, que são discutidos aqui em detalhes.</span><span class="sxs-lookup"><span data-stu-id="01905-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, **GetCommandString**, **InvokeCommand**, and **QueryContextMenu**, which are discussed here in detail.</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="01905-175">Método IContextMenu:: GetCommandString</span><span class="sxs-lookup"><span data-stu-id="01905-175">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="01905-176">O método [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) do manipulador é usado para retornar o nome canônico de um verbo.</span><span class="sxs-lookup"><span data-stu-id="01905-176">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="01905-177">Esse método é opcional.</span><span class="sxs-lookup"><span data-stu-id="01905-177">This method is optional.</span></span> <span data-ttu-id="01905-178">No Windows XP e em versões anteriores do Windows, quando o Windows Explorer tem uma barra de status, esse método é usado para recuperar o texto de ajuda que é exibido na barra de status de um item de menu.</span><span class="sxs-lookup"><span data-stu-id="01905-178">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="01905-179">O parâmetro *idCmd* contém o deslocamento do identificador do comando que foi definido quando [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="01905-179">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="01905-180">Se uma cadeia de caracteres de ajuda for solicitada, *uFlags* será definido como **GCS \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="01905-180">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="01905-181">Copie a cadeia de caracteres de ajuda para o buffer *pszName* , convertê-lo em um **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="01905-181">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="01905-182">A cadeia de caracteres de verbo é solicitada definindo *uFlags* para **GCS \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="01905-182">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="01905-183">Copie a cadeia de caracteres apropriada para *pszName*, assim como com a cadeia de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="01905-183">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="01905-184">Os sinalizadores do **\_ VALIDATEW** de **\_ validação de GCS** e GCS não são usados pelos manipuladores de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="01905-184">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="01905-185">O exemplo a seguir mostra uma implementação simples de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde ao exemplo [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornecido na seção do [método IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method) deste tópico.</span><span class="sxs-lookup"><span data-stu-id="01905-185">The following example shows a simple implementation of [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](#icontextmenuquerycontextmenu-method) section of this topic.</span></span> <span data-ttu-id="01905-186">Como o manipulador adiciona apenas um item de menu, há apenas um conjunto de cadeias de caracteres que podem ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="01905-186">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="01905-187">O método testa se *idCmd* é válido e, se for, retorna a cadeia de caracteres solicitada.</span><span class="sxs-lookup"><span data-stu-id="01905-187">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="01905-188">A função [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) é usada para copiar a cadeia de caracteres solicitada para *pszName* para garantir que a cadeia de caracteres copiada não exceda o tamanho do buffer especificado por *cchName*.</span><span class="sxs-lookup"><span data-stu-id="01905-188">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="01905-189">Este exemplo só implementa suporte para os valores Unicode de *uFlags*, pois apenas aqueles foram usados no Windows Explorer desde o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="01905-189">This example only implements support for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="01905-190">Método IContextMenu:: InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="01905-190">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="01905-191">Esse método é chamado quando um usuário clica em um item de menu para instruir o manipulador a executar o comando associado.</span><span class="sxs-lookup"><span data-stu-id="01905-191">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="01905-192">O parâmetro *Pici* aponta para uma estrutura que contém as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="01905-192">The *pici* parameter points to a structure that contains the information required.</span></span>

<span data-ttu-id="01905-193">Embora *Pici* seja declarado em shlobj. h como uma estrutura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , na prática geralmente aponta para uma estrutura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="01905-193">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="01905-194">Essa estrutura é uma versão estendida do **CMINVOKECOMMANDINFO** e tem vários membros adicionais que possibilitam a passagem de cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="01905-194">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="01905-195">Verifique o membro **cbSize** de *Pici* para determinar qual estrutura foi passada.</span><span class="sxs-lookup"><span data-stu-id="01905-195">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="01905-196">Se for uma estrutura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e o membro **fMask** tiver o sinalizador **\_ \_ Unicode de máscara CMIC** definido, converta *Pici* para **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="01905-196">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="01905-197">Isso permite que seu aplicativo use as informações de Unicode contidas nos últimos cinco membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="01905-197">This enables your application to use the Unicode information contained in the last five members of the structure.</span></span>

<span data-ttu-id="01905-198">O membro **lpVerb** ou **lpVerbW** da estrutura é usado para identificar o comando a ser executado.</span><span class="sxs-lookup"><span data-stu-id="01905-198">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="01905-199">Os comandos são identificados de uma das duas maneiras a seguir:</span><span class="sxs-lookup"><span data-stu-id="01905-199">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="01905-200">Pela cadeia de caracteres de verbo do comando</span><span class="sxs-lookup"><span data-stu-id="01905-200">By the command's verb string</span></span>
-   <span data-ttu-id="01905-201">Pelo deslocamento do identificador do comando</span><span class="sxs-lookup"><span data-stu-id="01905-201">By the command's identifier offset</span></span>

<span data-ttu-id="01905-202">Para distinguir entre esses dois casos, verifique a palavra de ordem superior de **lpVerb** para o caso ANSI ou **lpVerbW** para o caso Unicode.</span><span class="sxs-lookup"><span data-stu-id="01905-202">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="01905-203">Se a palavra de ordem superior for diferente de zero, **lpVerb** ou **lpVerbW** manterá uma cadeia de caracteres de verbo.</span><span class="sxs-lookup"><span data-stu-id="01905-203">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="01905-204">Se a palavra de ordem superior for zero, o deslocamento de comando estará na palavra de ordem inferior de **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="01905-204">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="01905-205">O exemplo a seguir mostra uma implementação simples de [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde aos exemplos de [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) fornecidos antes e depois desta seção.</span><span class="sxs-lookup"><span data-stu-id="01905-205">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="01905-206">O método determina primeiro qual estrutura está sendo passada.</span><span class="sxs-lookup"><span data-stu-id="01905-206">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="01905-207">Em seguida, ele determina se o comando é identificado por seu deslocamento ou seu verbo.</span><span class="sxs-lookup"><span data-stu-id="01905-207">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="01905-208">Se **lpVerb** ou **lpVerbW** mantiver um verbo ou um deslocamento válido, o método exibirá uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="01905-208">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="01905-209">Método IContextMenu:: QueryContextMenu</span><span class="sxs-lookup"><span data-stu-id="01905-209">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="01905-210">O Shell chama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar o manipulador de menu de atalho para adicionar seus itens de menu ao menu.</span><span class="sxs-lookup"><span data-stu-id="01905-210">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="01905-211">Ele passa o identificador **HMENU** no parâmetro *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="01905-211">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="01905-212">O parâmetro *indexMenu* é definido como o índice a ser usado para o primeiro item de menu a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="01905-212">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="01905-213">Todos os itens de menu que são adicionados pelo manipulador devem ter identificadores que se enquadram entre os valores nos parâmetros *idCmdFirst* e *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="01905-213">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="01905-214">Normalmente, o primeiro identificador de comando é definido como *idCmdFirst*, que é incrementado em um (1) para cada comando adicional.</span><span class="sxs-lookup"><span data-stu-id="01905-214">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="01905-215">Essa prática ajuda a evitar exceder o *idCmdLast* e maximiza o número de identificadores disponíveis caso o Shell chame mais de um manipulador.</span><span class="sxs-lookup"><span data-stu-id="01905-215">This practice helps you avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="01905-216">Um *deslocamento de comando* do identificador de item é a diferença entre o identificador e o valor em *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="01905-216">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="01905-217">Armazene o deslocamento de cada item que seu manipulador adiciona ao menu de atalho porque o Shell pode usá-lo para identificar o item se ele posteriormente chamar [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ou [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="01905-217">Store the offset of each item that your handler adds to the shortcut menu because the Shell might use it to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="01905-218">Você também deve atribuir um [verbo](launch.md) a cada comando que adicionar.</span><span class="sxs-lookup"><span data-stu-id="01905-218">You should also assign a [verb](launch.md) to each command you add.</span></span> <span data-ttu-id="01905-219">Um verbo é uma cadeia de caracteres que pode ser usada em vez do deslocamento para identificar o comando quando [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é chamado.</span><span class="sxs-lookup"><span data-stu-id="01905-219">A verb is a string that can be used instead of the offset to identify the command when [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="01905-220">Ele também é usado por funções como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para executar comandos de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="01905-220">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="01905-221">Há três sinalizadores que podem ser passados por meio do parâmetro *uFlags* que são relevantes para manipuladores de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="01905-221">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="01905-222">Eles são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01905-222">They are described in the following table.</span></span>



| <span data-ttu-id="01905-223">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="01905-223">Flag</span></span>             | <span data-ttu-id="01905-224">Descrição</span><span class="sxs-lookup"><span data-stu-id="01905-224">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01905-225">\_somente CMF</span><span class="sxs-lookup"><span data-stu-id="01905-225">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="01905-226">O usuário selecionou o comando padrão, normalmente clicando duas vezes no objeto.</span><span class="sxs-lookup"><span data-stu-id="01905-226">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="01905-227">[**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve retornar o controle para o shell sem modificar o menu.</span><span class="sxs-lookup"><span data-stu-id="01905-227">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="01905-228">CMF \_ padrão</span><span class="sxs-lookup"><span data-stu-id="01905-228">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="01905-229">Nenhum item no menu deve ser o item padrão.</span><span class="sxs-lookup"><span data-stu-id="01905-229">No item in the menu should be the default item.</span></span> <span data-ttu-id="01905-230">O método deve adicionar seus comandos ao menu.</span><span class="sxs-lookup"><span data-stu-id="01905-230">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="01905-231">CMF \_ normal</span><span class="sxs-lookup"><span data-stu-id="01905-231">CMF\_NORMAL</span></span>      | <span data-ttu-id="01905-232">O menu de atalho será exibido normalmente.</span><span class="sxs-lookup"><span data-stu-id="01905-232">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="01905-233">O método deve adicionar seus comandos ao menu.</span><span class="sxs-lookup"><span data-stu-id="01905-233">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="01905-234">Use [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) ou [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para adicionar itens de menu à lista.</span><span class="sxs-lookup"><span data-stu-id="01905-234">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="01905-235">Em seguida, retorne um valor **HRESULT** com a severidade definida como **\_ êxito de severidade**.</span><span class="sxs-lookup"><span data-stu-id="01905-235">Then return an **HRESULT** value with the severity set to **SEVERITY\_SUCCESS**.</span></span> <span data-ttu-id="01905-236">Defina o valor do código para o deslocamento do maior identificador de comando que foi atribuído, além de um (1).</span><span class="sxs-lookup"><span data-stu-id="01905-236">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="01905-237">Por exemplo, suponha que *idCmdFirst* seja definido como 5 e você adicione três itens ao menu com identificadores de comando de 5, 7 e 8.</span><span class="sxs-lookup"><span data-stu-id="01905-237">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="01905-238">O valor de retorno deve ser `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .</span><span class="sxs-lookup"><span data-stu-id="01905-238">The return value should be `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)`.</span></span>

<span data-ttu-id="01905-239">O exemplo a seguir mostra uma implementação simples de [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que insere um único comando.</span><span class="sxs-lookup"><span data-stu-id="01905-239">The following example shows a simple implementation of [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="01905-240">O deslocamento do identificador para o comando é \_ tela de IDM, que é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="01905-240">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="01905-241">As variáveis **m \_ pszVerb** e **m \_ pwszVerb** são variáveis privadas usadas para armazenar a cadeia de caracteres verbo independente de idioma associada nos formatos ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="01905-241">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



<span data-ttu-id="01905-242">Para outras tarefas de implementação de verbo, consulte [criando manipuladores de menu de contexto](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01905-242">For other verb implementation tasks, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="01905-243">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01905-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01905-244">Menus de atalho (contexto) e manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="01905-244">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="01905-245">Verbos e associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="01905-245">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="01905-246">Escolhendo um verbo estático ou dinâmico para o menu de atalho</span><span class="sxs-lookup"><span data-stu-id="01905-246">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="01905-247">Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla</span><span class="sxs-lookup"><span data-stu-id="01905-247">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="01905-248">Criando manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="01905-248">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="01905-249">Referência do menu de atalho</span><span class="sxs-lookup"><span data-stu-id="01905-249">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
