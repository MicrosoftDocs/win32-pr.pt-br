---
description: Você pode registrar uma lista de propriedades de exibição de conteúdo exclusiva e um padrão de layout para o tipo de arquivo ou item.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registrar um conjunto de exibição de conteúdo de propriedades e padrão de layout para um tipo de arquivo ou item
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104297809"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a><span data-ttu-id="b9861-103">Como registrar um conjunto exclusivo de exibição de conteúdo de propriedades e padrão de layout para o tipo de arquivo ou item</span><span class="sxs-lookup"><span data-stu-id="b9861-103">How to Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item</span></span>

<span data-ttu-id="b9861-104">Você pode registrar uma lista de propriedades de exibição de conteúdo exclusiva e um padrão de layout para o tipo de arquivo ou item.</span><span class="sxs-lookup"><span data-stu-id="b9861-104">You can register a unique Content view property list and layout pattern for the file type or item.</span></span> <span data-ttu-id="b9861-105">Se o tipo de arquivo ou o item também estiver associado a um tipo, o registro de exibição de conteúdo específico do tipo de arquivo ou item substituirá o registro de tipo.</span><span class="sxs-lookup"><span data-stu-id="b9861-105">If your file type or item is also associated with a Kind, the specific Content view registration of the file type or item will override the Kind registration.</span></span> <span data-ttu-id="b9861-106">Isso pode ser útil se as propriedades mais importantes para esse item forem diferentes de outros itens do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="b9861-106">This might be useful if the most important properties for this item are different from other items of the same Kind.</span></span> <span data-ttu-id="b9861-107">Se você não associar o tipo de arquivo ou o item a um tipo de item ou registrar diretamente a exibição de conteúdo, o sistema usará as informações de exibição de conteúdo padrão (armazenadas em uma chave de registro referenciada pelo último elemento na matriz de associação de todos os itens, HKEY \_ classes \_ root \\ \* )</span><span class="sxs-lookup"><span data-stu-id="b9861-107">If you do not associate your file type or item with an item Kind or directly register the Content view, the system uses the default Content view information (stored in a registry key referenced by the last element in all items' association array, HKEY\_CLASSES\_ROOT\\\*)</span></span>

<span data-ttu-id="b9861-108">Antes de registrar uma lista de propriedades Personalizada para o tipo de arquivo, você deve entender o modo de resultado da pesquisa e o modo de procura e os padrões de layout disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="b9861-108">Before registering a custom property list for your file type, you should understand the Search Result mode and Browse mode, and the layout patterns that are available to you.</span></span>

## <a name="instructions"></a><span data-ttu-id="b9861-109">Instruções</span><span class="sxs-lookup"><span data-stu-id="b9861-109">Instructions</span></span>

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a><span data-ttu-id="b9861-110">Etapa 1: Noções básicas sobre o modo de resultado de pesquisa e o modo de procura</span><span class="sxs-lookup"><span data-stu-id="b9861-110">Step 1: Understanding the Search Result Mode and Browse Mode</span></span>

<span data-ttu-id="b9861-111">A exibição de conteúdo requer a definição de um padrão de layout e um conjunto de listas de propriedades para um item em um conjunto de resultados da pesquisa (modo de resultado da pesquisa) e ao navegar até um local do Shell (modo de procura).</span><span class="sxs-lookup"><span data-stu-id="b9861-111">Content view requires defining a layout pattern and set of property lists for an item in a set of search results (Search result mode), and when browsing to a Shell location (Browse mode).</span></span> <span data-ttu-id="b9861-112">Você pode usar os mesmos valores para resultado da pesquisa e procurar, como `Kind.Music` faz.</span><span class="sxs-lookup"><span data-stu-id="b9861-112">You can use the same values for Search result and Browse, as `Kind.Music` does.</span></span> <span data-ttu-id="b9861-113">Como alternativa, você pode definir uma lista de propriedades e/ou padrão de layout diferente como `Kind.Document` o faz.</span><span class="sxs-lookup"><span data-stu-id="b9861-113">Alternatively, you can define a different property list and/or layout pattern as `Kind.Document` does.</span></span>

<span data-ttu-id="b9861-114">No caso do `Kind.Document` , os usuários geralmente pesquisam palavras no texto do documento.</span><span class="sxs-lookup"><span data-stu-id="b9861-114">In the case of `Kind.Document`, users often search for words in the text of the document.</span></span> <span data-ttu-id="b9861-115">Portanto, incluir mais texto de exemplo no resultado da pesquisa pode ser a melhor opção.</span><span class="sxs-lookup"><span data-stu-id="b9861-115">Therefore, including more sample text in the search result might be the best choice.</span></span> <span data-ttu-id="b9861-116">O exemplo a seguir ilustra a exibição de conteúdo de navegação de `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="b9861-116">The following example illustrates the Browse Content view of `Kind.Document`.</span></span>

![procurar exibição de conteúdo de kind.document](images/content-view/browsecontentviewkinddocument.png)

<span data-ttu-id="b9861-118">Como os usuários raramente procuram texto específico ao procurar documentos, otimizar sua escolha de propriedades e layout para ajustar mais resultados da pesquisa na tela pode ser a melhor opção.</span><span class="sxs-lookup"><span data-stu-id="b9861-118">Because users are rarely looking for particular text when browsing for documents, optimizing your choice of properties and layout to fit more search results on the screen might be the best choice.</span></span> <span data-ttu-id="b9861-119">A captura de tela a seguir ilustra a exibição de conteúdo de pesquisa do `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="b9861-119">The following screen shot illustrates the Search Content view of `Kind.Document`.</span></span>

### <a name="step-2-understanding-layout-patterns"></a><span data-ttu-id="b9861-120">Etapa 2: Noções básicas sobre padrões de layout</span><span class="sxs-lookup"><span data-stu-id="b9861-120">Step 2: Understanding Layout Patterns</span></span>

<span data-ttu-id="b9861-121">Há quatro padrões de layout: alfa, beta, gama e Delta.</span><span class="sxs-lookup"><span data-stu-id="b9861-121">There are four layout patterns: Alpha, Beta, Gamma, and Delta.</span></span>

<span data-ttu-id="b9861-122">**Layout alfa**</span><span class="sxs-lookup"><span data-stu-id="b9861-122">**Alpha layout**</span></span>

<span data-ttu-id="b9861-123">O padrão de layout alfa é otimizado para os resultados da pesquisa de documentos que contêm trechos.</span><span class="sxs-lookup"><span data-stu-id="b9861-123">The Alpha layout pattern is optimized for document search results that contain excerpts.</span></span> <span data-ttu-id="b9861-124">Ele tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="b9861-124">It has the following specifications:</span></span>

-   <span data-ttu-id="b9861-125">Linhas: 4</span><span class="sxs-lookup"><span data-stu-id="b9861-125">Rows: 4</span></span>
-   <span data-ttu-id="b9861-126">Propriedades: 7</span><span class="sxs-lookup"><span data-stu-id="b9861-126">Properties: 7</span></span>
-   <span data-ttu-id="b9861-127">Layout alfa quando o item tem 350 pixels ou mais de espaço horizontal, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9861-127">Alpha layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![padrão de layout alfa](images/content-view/layout1.png)

-   <span data-ttu-id="b9861-129">A ilustração a seguir mostra o layout alfa quando o item tem 350 pixels ou mais de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-129">The following illustration shows the Alpha layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagrama que mostra um exemplo de layout alfa](images/content-view/alphaviewmore.png)

-   <span data-ttu-id="b9861-131">A ilustração a seguir mostra o layout alfa quando o item tem menos de 350 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-131">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Captura de tela que mostra um exemplo de layout alfa no Microsoft Word.](images/content-view/layout2.png)

-   <span data-ttu-id="b9861-133">A ilustração a seguir mostra o layout alfa quando o item tem menos de 350 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-133">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![exemplo de layout alfa](images/content-view/alphaviewless.png)

<span data-ttu-id="b9861-135">**Layout beta**</span><span class="sxs-lookup"><span data-stu-id="b9861-135">**Beta Layout**</span></span>

<span data-ttu-id="b9861-136">O padrão de layout beta é otimizado para resultados de pesquisa de documentos de email que contêm trechos.</span><span class="sxs-lookup"><span data-stu-id="b9861-136">The Beta layout pattern is optimized for email document search results that contain excerpts.</span></span> <span data-ttu-id="b9861-137">Ele tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="b9861-137">It has the following specifications:</span></span>

-   <span data-ttu-id="b9861-138">Linhas: 4</span><span class="sxs-lookup"><span data-stu-id="b9861-138">Rows: 4</span></span>
-   <span data-ttu-id="b9861-139">Propriedades: 5</span><span class="sxs-lookup"><span data-stu-id="b9861-139">Properties: 5</span></span>
-   <span data-ttu-id="b9861-140">Layout beta quando o item tem 350 pixels ou mais de espaço horizontal, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9861-140">Beta layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagrama que mostra um exemplo de layout beta.](images/content-view/layout3.png)

-   <span data-ttu-id="b9861-142">A ilustração a seguir mostra o layout beta quando o item tem 350 pixels ou mais de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-142">The following illustration shows the beta layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Captura de tela que mostra um exemplo de layout beta para email.](images/content-view/betaviewmore.png)

-   <span data-ttu-id="b9861-144">A ilustração a seguir mostra o layout beta quando o item tem menos de 350 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-144">The following illustration shows the Beta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagrama que mostra um exemplo de layout beta com menos de 350 pixels de espaço horizontal.](images/content-view/layout4.png)

-   <span data-ttu-id="b9861-146">A ilustração a seguir mostra o layout beta quando o item tem menos de 350 pixels de espaço horizontal:</span><span class="sxs-lookup"><span data-stu-id="b9861-146">The following illustration shows the beta layout when the item has less than 350 pixels of horizontal space:</span></span>

    ![exemplo de layout beta](images/content-view/betaviewless.png)

<span data-ttu-id="b9861-148">**Layout gama**</span><span class="sxs-lookup"><span data-stu-id="b9861-148">**Gamma Layout**</span></span>

<span data-ttu-id="b9861-149">O padrão de layout gama é semelhante ao alfa, mas usa um layout de duas linhas em vez de quatro.</span><span class="sxs-lookup"><span data-stu-id="b9861-149">The Gamma layout pattern is similar to Alpha but uses a two-line layout instead of four.</span></span> <span data-ttu-id="b9861-150">Esse layout é ideal para cenários nos quais você deseja ver um trecho de código, mas deseja ajustar mais itens na tela ou para tipos de arquivo que exigem menos espaço para mostrar as informações mais críticas.</span><span class="sxs-lookup"><span data-stu-id="b9861-150">This layout is ideal for scenarios in which you want to see a snippet but want to fit more items on the screen, or for file types that require less space to show the most critical information.</span></span> <span data-ttu-id="b9861-151">O layout gama tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="b9861-151">The Gamma layout has the following specifications:</span></span>

-   <span data-ttu-id="b9861-152">Linhas: 2</span><span class="sxs-lookup"><span data-stu-id="b9861-152">Rows: 2</span></span>
-   <span data-ttu-id="b9861-153">Propriedades: 4</span><span class="sxs-lookup"><span data-stu-id="b9861-153">Properties: 4</span></span>
-   <span data-ttu-id="b9861-154">A ilustração a seguir mostra o layout gama quando o item tem 350 pixels ou mais de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-154">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagrama que mostra um exemplo de layout de gama.](images/content-view/layout5.png)

-   <span data-ttu-id="b9861-156">A ilustração a seguir mostra o layout gama quando o item tem 350 pixels ou mais de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-156">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Captura de tela que mostra um exemplo de layout de gama para um item de lista de verificação.](images/content-view/gammaviewmore.png)

-   <span data-ttu-id="b9861-158">A ilustração a seguir mostra o layout gama quando o item tem menos de 350 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-158">The following illustration shows the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagrama que mostra um exemplo de layout gama com menos de 350 pixels de espaço horizontal.](images/content-view/layout6.png)

-   <span data-ttu-id="b9861-160">Exemplo do layout gama quando o item tem menos de 350 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-160">Example of the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![exemplo de layout de gama](images/content-view/gammaviewless.png)

<span data-ttu-id="b9861-162">**Layout Delta**</span><span class="sxs-lookup"><span data-stu-id="b9861-162">**Delta Layout**</span></span>

<span data-ttu-id="b9861-163">O padrão de layout Delta é otimizado para exibir muitas propriedades mais curtas, como imagens e músicas.</span><span class="sxs-lookup"><span data-stu-id="b9861-163">The Delta layout pattern is optimized for displaying many shorter properties such as for music and pictures.</span></span> <span data-ttu-id="b9861-164">Ele tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="b9861-164">It has the following specifications:</span></span>

-   <span data-ttu-id="b9861-165">Linhas: 2</span><span class="sxs-lookup"><span data-stu-id="b9861-165">Rows: 2</span></span>
-   <span data-ttu-id="b9861-166">Propriedades: 6</span><span class="sxs-lookup"><span data-stu-id="b9861-166">Properties: 6</span></span>
-   <span data-ttu-id="b9861-167">Layout Delta quando o item tem 700 pixels ou mais de espaço horizontal, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9861-167">Delta layout when the item has 700 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagrama que mostra um exemplo de layout Delta.](images/content-view/layout7.png)

-   <span data-ttu-id="b9861-169">Exemplo do layout Delta quando o item tem 700 pixels ou mais de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-169">Example of the delta layout when the item has 700 pixels or more of horizontal space.</span></span>

    ![Captura de tela que mostra um exemplo de layout Delta para um arquivo de música.](images/content-view/deltalayoutmore.png)

-   <span data-ttu-id="b9861-171">Layout Delta quando o item tem entre 350 e 700 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-171">Delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Diagrama que mostra um exemplo de layout Delta que tem entre 350 e 700 pixels de espaço horizontal.](images/content-view/layout8.png)

-   <span data-ttu-id="b9861-173">Exemplo do layout Delta quando o item tem entre 350 e 700 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-173">Example of the delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![exemplo de layout de Delta](images/content-view/deltaviewbetween.png)

-   <span data-ttu-id="b9861-175">Layout Delta quando o item tem menos de 350 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-175">Delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![exemplo de layout](images/content-view/layout9.png)

-   <span data-ttu-id="b9861-177">Exemplo do layout Delta quando o item tem menos de 350 pixels de espaço horizontal.</span><span class="sxs-lookup"><span data-stu-id="b9861-177">Example of the delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Captura de tela que mostra um exemplo de layout Delta para um arquivo de música com menos de 350 pixels de espaço horizontal.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="b9861-179">Etapa 3: registrar Propriedades personalizadas e layout para o tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="b9861-179">Step 3: Registering Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="b9861-180">Depois de entender o modo de resultado da pesquisa, o modo de procura e os padrões de layout, você pode registrar uma lista de propriedades Personalizada para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b9861-180">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="b9861-181">**Para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo.**</span><span class="sxs-lookup"><span data-stu-id="b9861-181">**To register a custom property list and layout pattern for your file type.**</span></span>

1.  <span data-ttu-id="b9861-182">Escolha entre os quatro padrões de layout: alfa, beta, gama ou Delta.</span><span class="sxs-lookup"><span data-stu-id="b9861-182">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>
2.  <span data-ttu-id="b9861-183">Considere as seguintes regras de formatação, que se aplicam igualmente a todos os quatro padrões de layout:</span><span class="sxs-lookup"><span data-stu-id="b9861-183">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>
    -   <span data-ttu-id="b9861-184">A propriedade 1 é sempre exibida em um tamanho de fonte maior.</span><span class="sxs-lookup"><span data-stu-id="b9861-184">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="b9861-185">O tamanho de fonte grande geralmente usado para o nome do item, mas também pode ser usado para a propriedade de âncora ou outro item.</span><span class="sxs-lookup"><span data-stu-id="b9861-185">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
    -   <span data-ttu-id="b9861-186">A propriedade 4 destina-se a trechos nos padrões de layout alfa, beta e gama.</span><span class="sxs-lookup"><span data-stu-id="b9861-186">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="b9861-187">Essa propriedade é alocada mais espaço nesses padrões e é exibida em uma cor de fonte cinza, em oposição a preto, como as outras propriedades, para ajudá-lo a destacar.</span><span class="sxs-lookup"><span data-stu-id="b9861-187">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
    -   <span data-ttu-id="b9861-188">As medidas de pixel abaixo estão em pixels relativos e o tamanho inclui o ícone/miniatura à esquerda das propriedades e o espaço entre o ícone/miniatura e o retângulo de seleção.</span><span class="sxs-lookup"><span data-stu-id="b9861-188">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
    -   <span data-ttu-id="b9861-189">A maioria das propriedades tem um tamanho de exibição mínimo.</span><span class="sxs-lookup"><span data-stu-id="b9861-189">Most properties have a minimum display size.</span></span> <span data-ttu-id="b9861-190">Portanto, eles não serão exibidos se não houver espaço suficiente para eles em um tamanho de exibição específico.</span><span class="sxs-lookup"><span data-stu-id="b9861-190">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="b9861-191">O tamanho mínimo geralmente é de 100 pixels de largura.</span><span class="sxs-lookup"><span data-stu-id="b9861-191">The minimum size is usually 100 pixels wide.</span></span>
    -   <span data-ttu-id="b9861-192">Cada padrão de layout define o número de linhas e o número de propriedades em cada linha.</span><span class="sxs-lookup"><span data-stu-id="b9861-192">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>
3.  <span data-ttu-id="b9861-193">Decida quais propriedades você deseja exibir no layout e qual Propriedade deseja exibir em cada local.</span><span class="sxs-lookup"><span data-stu-id="b9861-193">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="b9861-194">Ao decidir qual propriedade será exibida em cada posição no layout, considere o comprimento típico da propriedade, sua importância para o usuário e se ela deve ser descartada quando o tamanho da janela for muito pequeno para conter todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="b9861-194">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>
4.  <span data-ttu-id="b9861-195">Registre um padrão de layout e uma lista de propriedades para o tipo de arquivo ou tipo de item adicionando as seguintes chaves na chave do registro ProgID para o tipo de arquivo ou item (neste exemplo, para o tipo de arquivo. xyz).</span><span class="sxs-lookup"><span data-stu-id="b9861-195">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  <span data-ttu-id="b9861-196">Observe as seguintes diretrizes de formatação para registrar Propriedades:</span><span class="sxs-lookup"><span data-stu-id="b9861-196">Observe the following formatting guidelines for registering properties:</span></span>

    -   <span data-ttu-id="b9861-197">Cada registro começa com `prop:`</span><span class="sxs-lookup"><span data-stu-id="b9861-197">Each registration starts with `prop:`</span></span>
    -   <span data-ttu-id="b9861-198">Cada propriedade requer o nome completo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="b9861-198">Each property requires the full property name.</span></span>
    -   <span data-ttu-id="b9861-199">As propriedades são separadas por um ponto-e-vírgula sem espaço.</span><span class="sxs-lookup"><span data-stu-id="b9861-199">Properties are separated by a semicolon with no space.</span></span>
    -   <span data-ttu-id="b9861-200">As propriedades são exibidas na ordem definida pelo padrão de layout selecionado.</span><span class="sxs-lookup"><span data-stu-id="b9861-200">Properties are displayed in the order defined by the selected layout pattern.</span></span>
    -   <span data-ttu-id="b9861-201">`~` indica que o rótulo da propriedade não deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b9861-201">`~` indicates that the property label should not be displayed.</span></span>
    -   <span data-ttu-id="b9861-202">`~System.LayoutPattern.PlaceHolder` deve ser usado se você quiser deixar em branco uma propriedade especificada no padrão de layout.</span><span class="sxs-lookup"><span data-stu-id="b9861-202">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

    <span data-ttu-id="b9861-203">A chave do registro de exemplo a seguir ilustra essas diretrizes de formatação.</span><span class="sxs-lookup"><span data-stu-id="b9861-203">The following sample registry key illustrates these formatting guidelines.</span></span>

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    <span data-ttu-id="b9861-204">Os valores possíveis para (ContentViewModeForBrowse) incluem o seguinte: prop: ~ System. ItemNameDisplay; System. Author; System. LayoutPattern. PlaceHolder; As palavras-chave System. System. DateModified; ~ System. Size</span><span class="sxs-lookup"><span data-stu-id="b9861-204">Possible values for (ContentViewModeForBrowse) include the following: prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified; ~System.Size</span></span>

## <a name="remarks"></a><span data-ttu-id="b9861-205">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9861-205">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9861-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9861-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9861-207">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="b9861-207">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="b9861-208">Nomes de tipos</span><span class="sxs-lookup"><span data-stu-id="b9861-208">Kind Names</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="b9861-209">System. PropList. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="b9861-209">System.PropList.ContentViewModeForBrowse</span></span>](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[<span data-ttu-id="b9861-210">System. PropList. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="b9861-210">System.PropList.ContentViewModeForSearch</span></span>](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
