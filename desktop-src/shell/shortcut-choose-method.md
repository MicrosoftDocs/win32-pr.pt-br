---
description: 'Este tópico é organizado da seguinte maneira:'
title: Escolhendo um método de menu de atalho estático ou dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011329"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="b5ce2-103">Escolhendo um método de menu de atalho estático ou dinâmico</span><span class="sxs-lookup"><span data-stu-id="b5ce2-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="b5ce2-104">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b5ce2-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b5ce2-105">Escolher um método de verbo</span><span class="sxs-lookup"><span data-stu-id="b5ce2-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="b5ce2-106">Métodos de verbo estáticos</span><span class="sxs-lookup"><span data-stu-id="b5ce2-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="b5ce2-107">Métodos de verbo dinâmico preferenciais</span><span class="sxs-lookup"><span data-stu-id="b5ce2-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="b5ce2-108">Métodos de verbo dinâmico desencorajados</span><span class="sxs-lookup"><span data-stu-id="b5ce2-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="b5ce2-109">Estender um menu de atalho</span><span class="sxs-lookup"><span data-stu-id="b5ce2-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="b5ce2-110">Suporte para métodos de verbo por sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b5ce2-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="b5ce2-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5ce2-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="b5ce2-112">Escolher um método de verbo</span><span class="sxs-lookup"><span data-stu-id="b5ce2-112">Choose a Verb Method</span></span>

<span data-ttu-id="b5ce2-113">É altamente recomendável que você implemente um menu de atalho usando um dos métodos de verbo estáticos.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="b5ce2-114">Métodos de verbo estáticos</span><span class="sxs-lookup"><span data-stu-id="b5ce2-114">Static Verb Methods</span></span>

<span data-ttu-id="b5ce2-115">Verbos estáticos são os verbos mais simples de implementar, mas ainda fornecem funcionalidade avançada.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="b5ce2-116">Sempre escolha o método de menu de atalho mais simples que atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5ce2-117">Verbo estático</span><span class="sxs-lookup"><span data-stu-id="b5ce2-117">Static Verb</span></span></th>
<th><span data-ttu-id="b5ce2-118">Description</span><span class="sxs-lookup"><span data-stu-id="b5ce2-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5ce2-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> com parâmetros de linha de comando</span><span class="sxs-lookup"><span data-stu-id="b5ce2-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="b5ce2-120">Esse é o meio mais simples e mais familiar de implementar um verbo estático.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="b5ce2-121">Um processo é invocado por meio de uma chamada para a função <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> com os arquivos selecionados e os parâmetros opcionais passados como a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="b5ce2-122">Isso abre o arquivo ou a pasta.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="b5ce2-123">Esse método tem as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="b5ce2-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="b5ce2-124">O comprimento da linha de comando é limitado a 2000 caracteres, o que limita o número de itens que o verbo pode manipular.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="b5ce2-125">Só pode ser usado com itens do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="b5ce2-126">Não habilita a reutilização de um processo já em execução.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="b5ce2-127">Requer que um executável seja instalado para manipular o verbo.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5ce2-128"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="b5ce2-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="b5ce2-129">Uma ativação de verbo baseada em COM significa que dá suporte à ativação em proc ou fora do processo.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="b5ce2-130"><strong>DropTarget</strong> / O <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> também dá suporte à reutilização de um manipulador já em execução quando a interface <strong>IDropTarget</strong> é implementada por um servidor local.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="b5ce2-131">Ele também expressa perfeitamente os itens por meio do objeto de dados marshaled e fornece uma referência à chamada de cadeia de sites para que você possa interagir com o chamador por meio do <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5ce2-132">Windows 7 e posterior: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="b5ce2-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="b5ce2-133">O método de implementação mais direto.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-133">The most direct implementation method.</span></span> <span data-ttu-id="b5ce2-134">Como esse é um método Invoke baseado em COM (como DropTarget), essa interface dá suporte à ativação no proc e fora do processo.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="b5ce2-135">O verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>e, opcionalmente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="b5ce2-136">Os itens são passados diretamente como uma matriz de item de shell e mais dos parâmetros do chamador estão disponíveis para a implementação de verbo, incluindo o ponto de invocação, o estado do teclado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5ce2-137">Windows 7 e posterior:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="b5ce2-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="b5ce2-138">Habilita fontes de dados que fornecem seus comandos de módulo de comando por meio do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> para usar esses comandos como verbos em um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="b5ce2-139">Como essa interface dá suporte apenas à ativação em processo, é recomendável usar por fontes de dados do shell que precisam compartilhar a implementação entre comandos e menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="b5ce2-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) é um híbrido entre um verbo estático e o dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="b5ce2-141">**IExplorerCommand** foi declarado no Windows Vista, mas sua capacidade de implementar um verbo em um menu de atalho é nova no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="b5ce2-142">Para obter mais informações sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e consultas de Shell para atributos de associação de arquivo, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="b5ce2-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="b5ce2-143">Métodos de verbo dinâmico preferenciais</span><span class="sxs-lookup"><span data-stu-id="b5ce2-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="b5ce2-144">Os métodos de verbo dinâmico a seguir são preferenciais:</span><span class="sxs-lookup"><span data-stu-id="b5ce2-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="b5ce2-145">Tipo de verbo</span><span class="sxs-lookup"><span data-stu-id="b5ce2-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="b5ce2-146">Description</span><span class="sxs-lookup"><span data-stu-id="b5ce2-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ce2-147">Verbo estático (listado na tabela anterior) + sintaxe de consulta avançada (AQS)</span><span class="sxs-lookup"><span data-stu-id="b5ce2-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="b5ce2-148">Essa opção Obtém a visibilidade dinâmica de verbo.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b5ce2-149">Windows 7 e posterior: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="b5ce2-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="b5ce2-150">Essa opção permite uma implementação comum de verbos e comandos do Explorer que são exibidos no módulo de comando no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b5ce2-151">Windows 7 e posterior: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo estático</span><span class="sxs-lookup"><span data-stu-id="b5ce2-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="b5ce2-152">Essa opção também obtém visibilidade dinâmica de verbo.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="b5ce2-153">É um modelo híbrido em que um manipulador no processo simples é usado para calcular se um determinado verbo estático deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="b5ce2-154">Isso pode ser aplicado a todos os métodos de implementação de verbo estático para obter o comportamento dinâmico e minimizar a exposição da lógica em processo.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="b5ce2-155">O [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) tem a vantagem de executar em um thread em segundo plano e, assim, evita os bloqueios da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="b5ce2-156">É consideravelmente mais simples do que [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b5ce2-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="b5ce2-157">Métodos de verbo dinâmico desencorajados</span><span class="sxs-lookup"><span data-stu-id="b5ce2-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="b5ce2-158">O [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) é o mais potente, mas também o método mais complicado para implementar.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="b5ce2-159">Ele se baseia em objetos COM em processo que são executados no thread do chamador, que geralmente o Windows Explorer, mas pode ser qualquer aplicativo que hospede os itens.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="b5ce2-160">O **IContextMenu** dá suporte à visibilidade de verbo, ordenação e desenho personalizado.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="b5ce2-161">Alguns desses recursos foram adicionados aos recursos de verbo estático, como um ícone a ser associado a um comando e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) para lidar com a visibilidade.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="b5ce2-162">Se você precisar estender o menu de atalho para um tipo de arquivo registrando um verbo dinâmico para o tipo de arquivo, siga as instruções fornecidas em [Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="b5ce2-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="b5ce2-163">Estender um menu de atalho</span><span class="sxs-lookup"><span data-stu-id="b5ce2-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="b5ce2-164">Depois de escolher um método de verbo, você pode estender um menu de atalho para um tipo de arquivo registrando um verbo estático para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="b5ce2-165">Para obter mais informações, consulte [criando manipuladores de menu de contexto](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="b5ce2-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="b5ce2-166">Suporte para métodos de verbo por sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b5ce2-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="b5ce2-167">O suporte para métodos de invocação de verbo por sistema operacional está listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5ce2-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | <span data-ttu-id="b5ce2-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5ce2-168">Windows XP</span></span> | <span data-ttu-id="b5ce2-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5ce2-169">Windows Vista</span></span> | <span data-ttu-id="b5ce2-170">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="b5ce2-170">Windows 7 and beyond</span></span> |
| <span data-ttu-id="b5ce2-171">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="b5ce2-171">CreateProcess</span></span>        | <span data-ttu-id="b5ce2-172">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-172">X</span></span>          | <span data-ttu-id="b5ce2-173">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-173">X</span></span>             | <span data-ttu-id="b5ce2-174">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-174">X</span></span>                    |
| <span data-ttu-id="b5ce2-175">DDE</span><span class="sxs-lookup"><span data-stu-id="b5ce2-175">DDE</span></span>                  | <span data-ttu-id="b5ce2-176">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-176">X</span></span>          | <span data-ttu-id="b5ce2-177">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-177">X</span></span>             | <span data-ttu-id="b5ce2-178">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-178">X</span></span>                    |
| <span data-ttu-id="b5ce2-179">DropTarget</span><span class="sxs-lookup"><span data-stu-id="b5ce2-179">DropTarget</span></span>           | <span data-ttu-id="b5ce2-180">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-180">X</span></span>          | <span data-ttu-id="b5ce2-181">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-181">X</span></span>             | <span data-ttu-id="b5ce2-182">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-182">X</span></span>                    |
| <span data-ttu-id="b5ce2-183">ExecuteCommand</span><span class="sxs-lookup"><span data-stu-id="b5ce2-183">ExecuteCommand</span></span>       |            | <span data-ttu-id="b5ce2-184">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-184">X</span></span>             | <span data-ttu-id="b5ce2-185">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-185">X</span></span>                    |
| <span data-ttu-id="b5ce2-186">ExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="b5ce2-186">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="b5ce2-187">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-187">X</span></span>                    |
| <span data-ttu-id="b5ce2-188">ExplorerCommandState</span><span class="sxs-lookup"><span data-stu-id="b5ce2-188">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="b5ce2-189">X</span><span class="sxs-lookup"><span data-stu-id="b5ce2-189">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="b5ce2-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5ce2-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5ce2-191">Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla</span><span class="sxs-lookup"><span data-stu-id="b5ce2-191">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="b5ce2-192">Criando manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="b5ce2-192">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="b5ce2-193">Personalizando um menu de atalho usando verbos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="b5ce2-193">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="b5ce2-194">Menus de atalho (contexto) e manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="b5ce2-194">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="b5ce2-195">Referência do menu de atalho</span><span class="sxs-lookup"><span data-stu-id="b5ce2-195">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="b5ce2-196">Verbos e associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="b5ce2-196">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
