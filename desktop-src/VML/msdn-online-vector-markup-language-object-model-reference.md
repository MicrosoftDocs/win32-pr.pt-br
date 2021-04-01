---
title: Referência de modelo de objeto VML
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008071"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="9d4b2-104">Referência de modelo de objeto VML</span><span class="sxs-lookup"><span data-stu-id="9d4b2-104">VML Object Model Reference</span></span>

<span data-ttu-id="9d4b2-105">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9d4b2-106">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9d4b2-107">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9d4b2-108">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9d4b2-109">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9d4b2-110">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9d4b2-111">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-111">In this topic:</span></span>

-   [<span data-ttu-id="9d4b2-112">Introdução</span><span class="sxs-lookup"><span data-stu-id="9d4b2-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="9d4b2-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-113">Example</span></span>](#example)
-   [<span data-ttu-id="9d4b2-114">Configurando a VML</span><span class="sxs-lookup"><span data-stu-id="9d4b2-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="9d4b2-115">Referência de OM de VML</span><span class="sxs-lookup"><span data-stu-id="9d4b2-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="9d4b2-116">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="9d4b2-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="9d4b2-117">Subelementos do elemento Shape</span><span class="sxs-lookup"><span data-stu-id="9d4b2-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="9d4b2-118">Elemento background</span><span class="sxs-lookup"><span data-stu-id="9d4b2-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="9d4b2-119">Elemento de extrusão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="9d4b2-120">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="9d4b2-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="9d4b2-121">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="9d4b2-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="9d4b2-122">Elemento ImageData</span><span class="sxs-lookup"><span data-stu-id="9d4b2-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="9d4b2-123">Elemento Path</span><span class="sxs-lookup"><span data-stu-id="9d4b2-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="9d4b2-124">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="9d4b2-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="9d4b2-125">Elemento skew</span><span class="sxs-lookup"><span data-stu-id="9d4b2-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="9d4b2-126">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="9d4b2-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="9d4b2-127">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="9d4b2-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="9d4b2-128">Tipos de dados usados no modelo de objeto VML</span><span class="sxs-lookup"><span data-stu-id="9d4b2-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="9d4b2-129">Introdução</span><span class="sxs-lookup"><span data-stu-id="9d4b2-129">Introduction</span></span>

<span data-ttu-id="9d4b2-130">[Linguagem VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) é uma linguagem baseada em texto que usa [XML](https://www.w3.org/TR/REC-xml.mdl) para estender o HTML com a finalidade de exibir informações gráficas vetoriais.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="9d4b2-131">O Modelo de Objeto do Documento do VML (DOM) define uma interface programática para a manipulação dos elementos do documento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="9d4b2-132">Isso permite que o usuário crie e modifique dinamicamente gráficos vetoriais por meio de uma interface neutra de plataforma e linguagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="9d4b2-133">O DOM do VML está em conformidade com a especificação de [modelo de objeto do documento](https://www.w3.org/TR/REC-DOM-Level-1/) .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="9d4b2-134">A VML usa o elemento [Shape](#shape-element) como o bloco de construção básico para imagens gráficas vetoriais.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="9d4b2-135">Depois que uma forma é criada, você pode modificar a forma por meio de atributos ou de subelementos anexados.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="9d4b2-136">Por exemplo, para alterar a cor de uma forma, atribua um valor de cor ao atributo **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="9d4b2-137">Vários dos atributos de uma forma também são [subelementos](/windows) e têm seus próprios atributos, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="9d4b2-138">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="9d4b2-139">Extrusão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="9d4b2-140">Preencher</span><span class="sxs-lookup"><span data-stu-id="9d4b2-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="9d4b2-141">Grupo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="9d4b2-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="9d4b2-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="9d4b2-143">Caminho</span><span class="sxs-lookup"><span data-stu-id="9d4b2-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="9d4b2-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="9d4b2-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="9d4b2-145">Inclinar</span><span class="sxs-lookup"><span data-stu-id="9d4b2-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="9d4b2-146">Pincel</span><span class="sxs-lookup"><span data-stu-id="9d4b2-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="9d4b2-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="9d4b2-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="9d4b2-148">O OM de VML usa vários [tipos de dados](/windows) para definir parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="9d4b2-149">Os tipos de texto prefixados com "VG" são enumerações e aqueles prefixados com "IVg" são objetos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="9d4b2-150">Clique aqui para obter uma lista.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-150">Click here for a list.</span></span> <span data-ttu-id="9d4b2-151">Os tipos de texto secundários são listados com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="9d4b2-152">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-152">Example</span></span>

<span data-ttu-id="9d4b2-153">O código VBScript a seguir mostra como criar uma forma simples:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-153">The following VBScript code shows how to create a simple shape:</span></span>


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



<span data-ttu-id="9d4b2-154">No exemplo acima, uma forma é criada usando o método Modelo de Objeto do Documento **CreateElement**.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="9d4b2-155">A forma é uma forma Rect predefinida de VML.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="9d4b2-156">Embora o objeto exista, ele não pode fazer parte do documento até que seja anexado ao documento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="9d4b2-157">Usando o método **AppendChild** , o Rect torna-se um filho de um elemento **div** chamado MyDiv.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="9d4b2-158">Alguns atributos de estilo mínimos (**posição**, **largura**, **altura**, **superior**, **esquerda**) são definidos para dar um tamanho específico à forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="9d4b2-159">Por fim, uma cor é atribuída com o atributo **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="9d4b2-160">Observe que qualquer linguagem de script ou qualquer linguagem que possa trabalhar com interfaces Modelo de Objeto do Documento pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="9d4b2-161">Configurando a VML</span><span class="sxs-lookup"><span data-stu-id="9d4b2-161">Setting up VML</span></span>

<span data-ttu-id="9d4b2-162">Uma implementação de VML é por meio do Microsoft Internet Explorer 5,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="9d4b2-163">Para configurar o objeto de renderização corretamente em uma página da Web, as seguintes adições devem ser feitas:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="9d4b2-164">O esquema deve ser configurado na inicial</span><span class="sxs-lookup"><span data-stu-id="9d4b2-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="9d4b2-165">Marque da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="9d4b2-166">O comportamento de renderização deve fazer parte do estilo do documento:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="9d4b2-167">Veja a seguir um exemplo de página da Web HTML configurada corretamente para VML mostrando a criação dinâmica de uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



<span data-ttu-id="9d4b2-168">Observe que, em versões beta, uma marca de objeto ActiveX e um estilo de comportamento diferente eram necessários.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="9d4b2-169">Referência de OM de VML</span><span class="sxs-lookup"><span data-stu-id="9d4b2-169">VML OM Reference</span></span>

<span data-ttu-id="9d4b2-170">Essa referência define o elemento [Shape](#shape-element) , os [subelementos](/windows)e os [tipos de dados](/windows) que são usados pelo modelo de objeto de VML.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="9d4b2-171">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="9d4b2-171">Shape element</span></span>

<span data-ttu-id="9d4b2-172">As formas são os blocos de construção de imagens gráficas definidas por linguagem VML (VML).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="9d4b2-173">A forma é o elemento de nível superior e vários subelementos ajudam a definir a natureza de cada forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="9d4b2-174">A VML fornece formas predefinidas:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="9d4b2-175">**Atributos de forma**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="9d4b2-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-176">**Arc**</span></span>
-   <span data-ttu-id="9d4b2-177">**Curva**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-177">**Curve**</span></span>
-   <span data-ttu-id="9d4b2-178">**Linha**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-178">**Line**</span></span>
-   <span data-ttu-id="9d4b2-179">**Múltipla**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-179">**PolyLine**</span></span>
-   <span data-ttu-id="9d4b2-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-180">**Rect**</span></span>
-   <span data-ttu-id="9d4b2-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-181">**RoundRect**</span></span>



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-182">Ajuste</span><span class="sxs-lookup"><span data-stu-id="9d4b2-182">Adj</span></span>          | <span data-ttu-id="9d4b2-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="9d4b2-184">Uma lista delimitada por vírgulas de números que são os parâmetros para as fórmulas de guia que definem o caminho da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-184">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="9d4b2-185">Os valores podem ser omitidos para permitir o uso de padrões.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-185">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="9d4b2-186">Pode haver até 8 valores de ajuste.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-186">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="9d4b2-187">Alt</span><span class="sxs-lookup"><span data-stu-id="9d4b2-187">Alt</span></span>          | <span data-ttu-id="9d4b2-188">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-188">String.</span></span> <span data-ttu-id="9d4b2-189">Texto alternativo associado à forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-189">Alternative text associated with shape.</span></span> <span data-ttu-id="9d4b2-190">Usado para navegação não gráfica.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-190">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d4b2-191">Botão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-191">Button</span></span>       | <span data-ttu-id="9d4b2-192">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-192">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-193">Exibe o comportamento do botão ao clicar.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-193">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d4b2-194">BWMode</span><span class="sxs-lookup"><span data-stu-id="9d4b2-194">BWMode</span></span>       | <span data-ttu-id="9d4b2-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d4b2-196">Determina como a forma será renderizada no modo de exibição preto-e-branco em aplicativos ou quando impressa em impressoras pretas e brancas.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-196">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="9d4b2-197">Os valores incluem: **cor**, **automático**, **escala de cinza**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **preto**, **branco**, não **desenhado**.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-197">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9d4b2-198">Padrão: **automático**.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-198">Default: **Auto**.</span></span> |
| <span data-ttu-id="9d4b2-199">BWNormal</span><span class="sxs-lookup"><span data-stu-id="9d4b2-199">BWNormal</span></span>     | <span data-ttu-id="9d4b2-200">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-200">VgBlackWhiteMode.</span></span> <span data-ttu-id="9d4b2-201">Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em preto e branco normal.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-201">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="9d4b2-202">Os valores incluem: **cor**, **automático**, **escala de cinza**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **preto**, **branco**, não **desenhado**.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-202">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9d4b2-203">Padrão: **automático**.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-203">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="9d4b2-204">BWPure</span><span class="sxs-lookup"><span data-stu-id="9d4b2-204">BWPure</span></span>       | <span data-ttu-id="9d4b2-205">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-205">VgBlackWhiteMode.</span></span> <span data-ttu-id="9d4b2-206">Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em B/W puro.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-206">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="9d4b2-207">Os valores incluem: **cor**, **automático**, **escala de cinza**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **preto**, **branco**, não **desenhado**.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-207">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9d4b2-208">Padrão: **automático**.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-208">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="9d4b2-209">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="9d4b2-209">ChildShapes</span></span>  | <span data-ttu-id="9d4b2-210">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-210">IVgGroupShapes.</span></span> <span data-ttu-id="9d4b2-211">Uma coleção de outras formas neste grupo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-211">A collection of other shapes in this group.</span></span> <span data-ttu-id="9d4b2-212">Esta coleção dá suporte aos métodos de comprimento e item padrão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-212">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d4b2-213">Chromakey</span><span class="sxs-lookup"><span data-stu-id="9d4b2-213">Chromakey</span></span>    | <span data-ttu-id="9d4b2-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d4b2-215">Um valor de cor que será transparente e mostrará qualquer coisa por trás da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-215">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9d4b2-216">Control1</span><span class="sxs-lookup"><span data-stu-id="9d4b2-216">Control1</span></span>     | <span data-ttu-id="9d4b2-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-218">Ponto de controle para curva.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-218">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d4b2-219">Control2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-219">Control2</span></span>     | <span data-ttu-id="9d4b2-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-221">Ponto de controle para curva.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-221">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d4b2-222">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="9d4b2-222">CoordOrigin</span></span>  | <span data-ttu-id="9d4b2-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) As coordenadas no canto superior esquerdo do retângulo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="9d4b2-224">Intervalo de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-224">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9d4b2-225">CoordSize</span><span class="sxs-lookup"><span data-stu-id="9d4b2-225">CoordSize</span></span>    | <span data-ttu-id="9d4b2-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-227">A largura e a altura do espaço de coordenadas dentro do retângulo de referência dessa forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-227">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="9d4b2-228">Se não for especificado, será o mesmo que a largura e a altura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-228">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="9d4b2-229">Intervalo de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-229">Range from 0 to infinity.</span></span> <span data-ttu-id="9d4b2-230">Padrão: "1000, 1000".</span><span class="sxs-lookup"><span data-stu-id="9d4b2-230">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="9d4b2-231">Ângulo de fim</span><span class="sxs-lookup"><span data-stu-id="9d4b2-231">EndAngle</span></span>     | <span data-ttu-id="9d4b2-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9d4b2-233">Ângulo de extremidade da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-233">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9d4b2-234">Extrusão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-234">Extrusion</span></span>    | <span data-ttu-id="9d4b2-235">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-235">IVgExtrusion.</span></span> <span data-ttu-id="9d4b2-236">Especifica o valor do objeto de extrusão para esta forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-236">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="9d4b2-237">Consulte o elemento de [extrusão](msdn-online-vml-extrusion-element.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-237">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9d4b2-238">Preencher</span><span class="sxs-lookup"><span data-stu-id="9d4b2-238">Fill</span></span>         | <span data-ttu-id="9d4b2-239">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-239">VgFillFormat.</span></span> <span data-ttu-id="9d4b2-240">Especifica o valor de preenchimento para esta forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-240">Specifies the fill value for this shape.</span></span> <span data-ttu-id="9d4b2-241">Consulte o elemento [Fill](msdn-online-vml-fill-element.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-241">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="9d4b2-242">EstiloDePreenchimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-242">FillColor</span></span>    | <span data-ttu-id="9d4b2-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d4b2-244">A cor primária do pincel a ser usada para preencher o caminho desta forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-244">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d4b2-245">Preencher</span><span class="sxs-lookup"><span data-stu-id="9d4b2-245">Filled</span></span>       | <span data-ttu-id="9d4b2-246">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-246">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-247">Se for true, o caminho que define a forma será preenchido.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-247">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="9d4b2-248">Por padrão, ele será preenchido usando uma cor sólida, a menos que haja um subelemento Fill que especifique propriedades de preenchimento mais complexas.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-248">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="9d4b2-249">Se for false, o preenchimento será transparente.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-249">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="9d4b2-250">Inverter</span><span class="sxs-lookup"><span data-stu-id="9d4b2-250">Flip</span></span>         | <span data-ttu-id="9d4b2-251">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-251">VgFlipOrientation.</span></span> <span data-ttu-id="9d4b2-252">Os valores são: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="9d4b2-252">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9d4b2-253">ForceDash</span><span class="sxs-lookup"><span data-stu-id="9d4b2-253">ForceDash</span></span>    | <span data-ttu-id="9d4b2-254">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-254">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-255">Indica que um contorno tracejado deve ser renderizado quando não há nenhuma linha e nenhum preenchimento para uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-255">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="9d4b2-256">Esse comportamento é geralmente útil para tornar as formas invisíveis visíveis na edição de aplicativos para que possam ser selecionadas e operadas, como em um mapa de imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-256">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="9d4b2-257">Fórmulas</span><span class="sxs-lookup"><span data-stu-id="9d4b2-257">Formulas</span></span>     | <span data-ttu-id="9d4b2-258">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-258">IVgFormulas.</span></span> <span data-ttu-id="9d4b2-259">Uma matriz de fórmulas que define uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-259">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9d4b2-260">De</span><span class="sxs-lookup"><span data-stu-id="9d4b2-260">From</span></span>         | <span data-ttu-id="9d4b2-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-262">Ponto de partida da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-262">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9d4b2-263">HRef</span><span class="sxs-lookup"><span data-stu-id="9d4b2-263">HRef</span></span>         | <span data-ttu-id="9d4b2-264">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-264">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-265">A URL para saltar se essa forma for clicada.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-265">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d4b2-266">ImageData</span><span class="sxs-lookup"><span data-stu-id="9d4b2-266">ImageData</span></span>    | <span data-ttu-id="9d4b2-267">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-267">IVgImageData.</span></span> <span data-ttu-id="9d4b2-268">Informações da imagem se a forma for uma imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-268">Image information if the shape is a picture.</span></span> <span data-ttu-id="9d4b2-269">Consulte o elemento ImageData para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-269">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d4b2-270">OnEd</span><span class="sxs-lookup"><span data-stu-id="9d4b2-270">OnEd</span></span>         | <span data-ttu-id="9d4b2-271">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-271">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-272">Oculta todos os identificadores, exceto a parte superior esquerda e inferior direita, como nos identificadores de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-272">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="9d4b2-273">Opacidade</span><span class="sxs-lookup"><span data-stu-id="9d4b2-273">Opacity</span></span>      | <span data-ttu-id="9d4b2-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d4b2-275">A opacidade de toda a forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-275">The opacity of the entire shape.</span></span> <span data-ttu-id="9d4b2-276">Um número entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-276">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d4b2-277">Caminho</span><span class="sxs-lookup"><span data-stu-id="9d4b2-277">Path</span></span>         | <span data-ttu-id="9d4b2-278">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-278">IVgPath.</span></span> <span data-ttu-id="9d4b2-279">Uma cadeia de caracteres que contém os comandos que definem o caminho.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-279">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d4b2-280">Pontos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-280">Points</span></span>       | <span data-ttu-id="9d4b2-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="9d4b2-282">Uma coleção de pontos que define uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-282">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9d4b2-283">Imprimir</span><span class="sxs-lookup"><span data-stu-id="9d4b2-283">Print</span></span>        | <span data-ttu-id="9d4b2-284">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-284">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-285">Se for true, essa forma deve ser impressa.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-285">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d4b2-286">Rotação</span><span class="sxs-lookup"><span data-stu-id="9d4b2-286">Rotation</span></span>     | <span data-ttu-id="9d4b2-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9d4b2-288">Define a rotação da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-288">Sets rotation of shape.</span></span> <span data-ttu-id="9d4b2-289">O valor é propagado para o estilo de forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-289">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d4b2-290">Escala</span><span class="sxs-lookup"><span data-stu-id="9d4b2-290">Scale</span></span>        | <span data-ttu-id="9d4b2-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-292">Escala de forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-292">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d4b2-293">Shadow</span><span class="sxs-lookup"><span data-stu-id="9d4b2-293">Shadow</span></span>       | <span data-ttu-id="9d4b2-294">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-294">IVgShadow.</span></span> <span data-ttu-id="9d4b2-295">Especifica a sombra desta forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-295">Specifies the shadow for this shape.</span></span> <span data-ttu-id="9d4b2-296">Consulte o elemento [Shadow](msdn-online-vml-shadow-element.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-296">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d4b2-297">Spt</span><span class="sxs-lookup"><span data-stu-id="9d4b2-297">Spt</span></span>          | <span data-ttu-id="9d4b2-298">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-298">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d4b2-299">StartAngle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-299">StartAngle</span></span>   | <span data-ttu-id="9d4b2-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9d4b2-301">Ângulo inicial da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-301">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d4b2-302">Traço</span><span class="sxs-lookup"><span data-stu-id="9d4b2-302">Stroke</span></span>       | <span data-ttu-id="9d4b2-303">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-303">VgStrokeFormat.</span></span> <span data-ttu-id="9d4b2-304">Consulte elemento de traço para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-304">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d4b2-305">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-305">StrokeColor</span></span>  | <span data-ttu-id="9d4b2-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d4b2-307">A cor primária do pincel a ser usada para traçar o caminho desta forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-307">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="9d4b2-308">Traçados</span><span class="sxs-lookup"><span data-stu-id="9d4b2-308">Stroked</span></span>      | <span data-ttu-id="9d4b2-309">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-309">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-310">Se for true, o caminho que define a forma será traçado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-310">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d4b2-311">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="9d4b2-311">StrokeWeight</span></span> | <span data-ttu-id="9d4b2-312">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-312">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="9d4b2-313">A largura do pincel a ser usada para traçar o caminho.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-313">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="9d4b2-314">Intervalos entre 0 e 1584.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-314">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d4b2-315">TextPath</span><span class="sxs-lookup"><span data-stu-id="9d4b2-315">TextPath</span></span>     | <span data-ttu-id="9d4b2-316">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-316">IVgTextPath.</span></span> <span data-ttu-id="9d4b2-317">Especifica o objeto TextPath da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-317">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="9d4b2-318">Consulte o elemento [TextPath](msdn-online-vml-textpath-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-318">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d4b2-319">Para</span><span class="sxs-lookup"><span data-stu-id="9d4b2-319">To</span></span>           | <span data-ttu-id="9d4b2-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-321">Ponto de extremidade da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-321">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d4b2-322">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-322">Type</span></span>         | <span data-ttu-id="9d4b2-323">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-323">String.</span></span> <span data-ttu-id="9d4b2-324">Tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-324">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="9d4b2-325">Subelementos do elemento Shape</span><span class="sxs-lookup"><span data-stu-id="9d4b2-325">Subelements of the Shape Element</span></span>

<span data-ttu-id="9d4b2-326">Os subelementos a seguir fazem parte do modelo de objeto VML.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-326">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="9d4b2-327">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-327">Background</span></span>](#background-element)
-   [<span data-ttu-id="9d4b2-328">Extrusão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-328">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="9d4b2-329">Preencher</span><span class="sxs-lookup"><span data-stu-id="9d4b2-329">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="9d4b2-330">Grupo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-330">Group</span></span>](#group-element)
-   [<span data-ttu-id="9d4b2-331">Imagedata</span><span class="sxs-lookup"><span data-stu-id="9d4b2-331">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="9d4b2-332">Caminho</span><span class="sxs-lookup"><span data-stu-id="9d4b2-332">Path</span></span>](#path-element)
-   [<span data-ttu-id="9d4b2-333">Shadow</span><span class="sxs-lookup"><span data-stu-id="9d4b2-333">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="9d4b2-334">Inclinar</span><span class="sxs-lookup"><span data-stu-id="9d4b2-334">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="9d4b2-335">Pincel</span><span class="sxs-lookup"><span data-stu-id="9d4b2-335">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="9d4b2-336">TextPath</span><span class="sxs-lookup"><span data-stu-id="9d4b2-336">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="9d4b2-337">Elemento background</span><span class="sxs-lookup"><span data-stu-id="9d4b2-337">Background element</span></span>

<span data-ttu-id="9d4b2-338">Descreve o preenchimento do plano de fundo de uma página usando preenchimentos de VML.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-338">Describes the fill of the background of a page using VML fills.</span></span>

<span data-ttu-id="9d4b2-339">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-339">**Attributes**</span></span>



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-340">BWMode</span><span class="sxs-lookup"><span data-stu-id="9d4b2-340">BWMode</span></span>    | <span data-ttu-id="9d4b2-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d4b2-342">Determina como a forma será renderizada no modo de exibição preto e branco em aplicativos ou quando impressa.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-342">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="9d4b2-343">BWNormal</span><span class="sxs-lookup"><span data-stu-id="9d4b2-343">BWNormal</span></span>  | <span data-ttu-id="9d4b2-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d4b2-345">Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em preto e branco normal.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-345">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="9d4b2-346">BWPure</span><span class="sxs-lookup"><span data-stu-id="9d4b2-346">BWPure</span></span>    | <span data-ttu-id="9d4b2-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d4b2-348">Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em preto e branco puro.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-348">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="9d4b2-349">Preencher</span><span class="sxs-lookup"><span data-stu-id="9d4b2-349">Fill</span></span>      | <span data-ttu-id="9d4b2-350">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-350">VgFillFormat.</span></span> <span data-ttu-id="9d4b2-351">Especifica o preenchimento desta forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-351">Specifies the fill for this shape.</span></span> <span data-ttu-id="9d4b2-352">Confira elemento [Fill](msdn-online-vml-fill-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-352">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="9d4b2-353">EstiloDePreenchimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-353">FillColor</span></span> | <span data-ttu-id="9d4b2-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d4b2-355">A cor primária do pincel a ser usada para preencher o caminho desta forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-355">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="9d4b2-356">Duplicata do valor de cor no elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-356">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="9d4b2-357">O padrão é branco.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-357">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="9d4b2-358">Elemento de extrusão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-358">Extrusion element</span></span>

<span data-ttu-id="9d4b2-359">Descreve uma extrusão 3D da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-359">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="9d4b2-360">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-360">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-361">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="9d4b2-361">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="9d4b2-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-363">Se for true, o centro de rotação do grupo de objetos 3D (na verdade, há apenas um objeto no grupo) será determinado automaticamente para ser o centro do grupo; caso contrário, ele é determinado pelos parâmetros RotationCenter, que são uma fração da forma com 0, 0, sendo o centro.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-363">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-364">Profundidade de fundo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-364">BackDepth</span></span></td>
<td><span data-ttu-id="9d4b2-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="9d4b2-366">Quantidade de extrusão regressiva.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-366">Amount of backward extrusion.</span></span> <span data-ttu-id="9d4b2-367">Varia de 0 a 32767.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-367">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-368">Brightness</span><span class="sxs-lookup"><span data-stu-id="9d4b2-368">Brightness</span></span></td>
<td><span data-ttu-id="9d4b2-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d4b2-370">Brilho geral da cena.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-370">Overall brightness of the scene.</span></span> <span data-ttu-id="9d4b2-371">O padrão é &quot; 20.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-371">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-372">Cor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-372">Color</span></span></td>
<td><span data-ttu-id="9d4b2-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d4b2-374">A cor da extrusão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-374">The color of the extrusion.</span></span> <span data-ttu-id="9d4b2-375">Usado somente se ColorMode for personalizado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-375">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="9d4b2-376">Caso contrário, o define automaticamente a cor do efeito de extrusão como o mesmo que FillColor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-376">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-377">ColorMode</span><span class="sxs-lookup"><span data-stu-id="9d4b2-377">ColorMode</span></span></td>
<td><span data-ttu-id="9d4b2-378">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-378">Vg3DColorMode.</span></span> <span data-ttu-id="9d4b2-379">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-379">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-380">Auto (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-380">Auto (default)</span></span></li>
<li><span data-ttu-id="9d4b2-381">Personalizado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-381">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-382">Difusão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-382">Diffusity</span></span></td>
<td><span data-ttu-id="9d4b2-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d4b2-384">A taxa de incidente para a luz refletida difusamente.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-384">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="9d4b2-385">Valores menores que 1,0 são normais, mas valores maiores que um podem gerar efeitos interessantes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-385">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-386">Edge</span><span class="sxs-lookup"><span data-stu-id="9d4b2-386">Edge</span></span></td>
<td><span data-ttu-id="9d4b2-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9d4b2-388">Define o tamanho de uma borda chanfrada arredondada simulada.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-388">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="9d4b2-389">Varia de 0 a 32767 em ponto flutuante pts.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-389">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="9d4b2-390">O padrão é &quot; 1pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-390">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-391">Faceta</span><span class="sxs-lookup"><span data-stu-id="9d4b2-391">Facet</span></span></td>
<td><span data-ttu-id="9d4b2-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d4b2-393">Define a faceta da cena.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-393">Sets the facet of the scene.</span></span> <span data-ttu-id="9d4b2-394">O padrão é &quot; 30.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-394">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-395">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="9d4b2-395">ForeDepth</span></span></td>
<td><span data-ttu-id="9d4b2-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9d4b2-397">Quantidade de extrusão posterior.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-397">Amount of forward extrusion.</span></span> <span data-ttu-id="9d4b2-398">Varia de 0 a 32767.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-398">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-399">LightFace</span><span class="sxs-lookup"><span data-stu-id="9d4b2-399">LightFace</span></span></td>
<td><span data-ttu-id="9d4b2-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-401">Determimes se a face frontal do objeto responderá às alterações na iluminação 3D, por exemplo, quando um objeto for girado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-401">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-402">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="9d4b2-402">LightHarsh</span></span></td>
<td><span data-ttu-id="9d4b2-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-404">Iluminação de inverso para a fonte de luz primária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-404">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="9d4b2-405">O padrão é Falso.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-405">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-406">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-406">LightHarsh2</span></span></td>
<td><span data-ttu-id="9d4b2-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-408">Iluminação de durabilidade para a fonte de luz secundária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-408">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="9d4b2-409">O padrão é Falso.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-409">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-410">LightLevel</span><span class="sxs-lookup"><span data-stu-id="9d4b2-410">LightLevel</span></span></td>
<td><span data-ttu-id="9d4b2-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="9d4b2-412">Intensidade da fonte de luz primária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-412">Intensity of the primary light source.</span></span> <span data-ttu-id="9d4b2-413">O padrão é &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-413">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-414">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-414">LightLevel2</span></span></td>
<td><span data-ttu-id="9d4b2-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="9d4b2-416">Intensidade da fonte de luz secundária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-416">Intensity of the secondary light source.</span></span> <span data-ttu-id="9d4b2-417">O padrão é &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-417">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-418">LightPosition</span><span class="sxs-lookup"><span data-stu-id="9d4b2-418">LightPosition</span></span></td>
<td><span data-ttu-id="9d4b2-419">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-419">Vector3D.</span></span> <span data-ttu-id="9d4b2-420">Posição da fonte de luz primária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-420">Position of the primary light source.</span></span> <span data-ttu-id="9d4b2-421">O padrão é &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-421">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-422">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-422">LightPosition2</span></span></td>
<td><span data-ttu-id="9d4b2-423">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-423">Vector3D.</span></span> <span data-ttu-id="9d4b2-424">Posição da fonte de luz secundária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-424">Position of the secondary light source.</span></span> <span data-ttu-id="9d4b2-425">O padrão é &quot; -50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-425">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-426">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="9d4b2-426">LockRotationCenter</span></span></td>
<td><span data-ttu-id="9d4b2-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-428">&quot;Lockrotationcenter &quot; significa que a rotação do grupo é definida para ser por ângulo de rotação [1] graus sobre o eixo y na página seguido por ângulo de rotação [0] graus sobre o eixo x.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-428">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="9d4b2-429">Quando LockRotationCenter é false, a rotação é definida de acordo com os graus de ângulo de orientação sobre o vetor definido por orientação.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-429">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="9d4b2-430">Portanto, por exemplo, lockrotationcenter = false orientationangle = 45 Orientation = (0, 1, 0) é equivalente a lockrotationcenter = true RotationAngle = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-430">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-431">Metal</span><span class="sxs-lookup"><span data-stu-id="9d4b2-431">Metal</span></span></td>
<td><span data-ttu-id="9d4b2-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-433">Faz com que a luz refletida de forma especulada seja a cor do material em vez da cor da fonte de luz, tornando o objeto aparentemente mais metálico.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-433">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-434">Ativado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-434">On</span></span></td>
<td><span data-ttu-id="9d4b2-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-436">Ativa e desativa a exibição do efeito de extrusão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-436">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-437">Orientation</span><span class="sxs-lookup"><span data-stu-id="9d4b2-437">Orientation</span></span></td>
<td><span data-ttu-id="9d4b2-438">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-438">Vector3D.</span></span> <span data-ttu-id="9d4b2-439">Orientação da câmera.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-439">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-440">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-440">OrientationAngle</span></span></td>
<td><span data-ttu-id="9d4b2-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9d4b2-442">Ângulo entre a orientação da câmera e o plano XY.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-442">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-443">Aérea</span><span class="sxs-lookup"><span data-stu-id="9d4b2-443">Plane</span></span></td>
<td><span data-ttu-id="9d4b2-444">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-444">Vg3DExtrudePlane.</span></span> <span data-ttu-id="9d4b2-445">Permite a extrusão dos planos ortogonal ao plano de tela.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-445">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="9d4b2-446">Requer que ForeDepth e a profundidade de fundo sejam especificadas em unidades de desenho em vez de emus.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-446">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="9d4b2-447">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-447">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-448">XY</span><span class="sxs-lookup"><span data-stu-id="9d4b2-448">XY</span></span></li>
<li><span data-ttu-id="9d4b2-449">ZX</span><span class="sxs-lookup"><span data-stu-id="9d4b2-449">ZX</span></span></li>
<li><span data-ttu-id="9d4b2-450">YZ</span><span class="sxs-lookup"><span data-stu-id="9d4b2-450">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-451">Renderizar</span><span class="sxs-lookup"><span data-stu-id="9d4b2-451">Render</span></span></td>
<td><span data-ttu-id="9d4b2-452">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-452">Vg3DRenderMode.</span></span> <span data-ttu-id="9d4b2-453">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-453">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-454">Solid (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-454">Solid (default)</span></span></li>
<li><span data-ttu-id="9d4b2-455">WireFrame</span><span class="sxs-lookup"><span data-stu-id="9d4b2-455">WireFrame</span></span></li>
<li><span data-ttu-id="9d4b2-456">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="9d4b2-456">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-457">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-457">RotationAngle</span></span></td>
<td><span data-ttu-id="9d4b2-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-459">AngleX, incline ou AngleZ é controlado pelo atributo ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-459">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-460">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="9d4b2-460">RotationCenter</span></span></td>
<td><span data-ttu-id="9d4b2-461">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-461">Vector3D.</span></span> <span data-ttu-id="9d4b2-462">Centro de rotação.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-462">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-463">Luminosidade</span><span class="sxs-lookup"><span data-stu-id="9d4b2-463">Shininess</span></span></td>
<td><span data-ttu-id="9d4b2-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d4b2-465">Determina o quão concentrado ou distribuído a reflexão especular é.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-465">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="9d4b2-466">Um valor alto seria de 8 a 10 e aproximaria um espelho, e um valor baixo seria de 2 a 3 e seria um roupas sequined aproximado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-466">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="9d4b2-467">São recomendados valores de 3 a 7.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-467">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="9d4b2-468">Valores altos refletirão as fontes de luz do Pinpoint.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-468">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-469">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="9d4b2-469">SkewAmt</span></span></td>
<td><span data-ttu-id="9d4b2-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="9d4b2-471">Se Type for Parallel, o atributo determinará a quantidade de distorção.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-471">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="9d4b2-472">Varia de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-472">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-473">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-473">SkewAngle</span></span></td>
<td><span data-ttu-id="9d4b2-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9d4b2-475">Se Type for Parallel, o atributo determinará o grau de distorção.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-475">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="9d4b2-476">O padrão é &quot; -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-476">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-477">Refletir</span><span class="sxs-lookup"><span data-stu-id="9d4b2-477">Specularity</span></span></td>
<td><span data-ttu-id="9d4b2-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d4b2-479">A taxa de incidentes para a luz refletida especulada.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-479">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="9d4b2-480">Valores menores que 1,0 são normais, mas valores maiores que um podem gerar efeitos interessantes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-480">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-481">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-481">Type</span></span></td>
<td><span data-ttu-id="9d4b2-482">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-482">VgExtrusionType.</span></span> <span data-ttu-id="9d4b2-483">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-483">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-484">Paralelo (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-484">Parallel (default)</span></span></li>
<li><span data-ttu-id="9d4b2-485">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="9d4b2-485">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-486">Ponto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-486">Viewpoint</span></span></td>
<td><span data-ttu-id="9d4b2-487">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-487">Vector3D.</span></span> <span data-ttu-id="9d4b2-488">O ponto em que a cena está sendo visualizada.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-488">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-489">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="9d4b2-489">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="9d4b2-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-491">Pode ter valores de 0,5 a 0,5 para posicionar a origem do ponto de vista dentro da caixa delimitadora de forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-491">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="9d4b2-492">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="9d4b2-492">Fill element</span></span>

<span data-ttu-id="9d4b2-493">Descreve como um caminho deve ser preenchido para preenchimentos mais complexos do que uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-493">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="9d4b2-494">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-494">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-495">AlignShape</span><span class="sxs-lookup"><span data-stu-id="9d4b2-495">AlignShape</span></span></td>
<td><span data-ttu-id="9d4b2-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-497">Alinhe a imagem com a forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-497">Align the image with the shape.</span></span> <span data-ttu-id="9d4b2-498">Se for false, alinhar a imagem com a janela.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-498">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-499">Ângulo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-499">Angle</span></span></td>
<td><span data-ttu-id="9d4b2-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9d4b2-501">O ângulo ao longo do qual o gradiente vai.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-501">The angle along which the gradient goes.</span></span> <span data-ttu-id="9d4b2-502">0 graus é ao longo do eixo horizontal da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-502">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-503">Aspecto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-503">Aspect</span></span></td>
<td><span data-ttu-id="9d4b2-504"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-504"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="9d4b2-505">O atributo ImageSize será ajustado para preservar o aspecto da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-505">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="9d4b2-506">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-506">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-507">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-507">Value</span></span></th>
<th><span data-ttu-id="9d4b2-508">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-508">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-509">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9d4b2-509">Ignore</span></span></td>
<td><span data-ttu-id="9d4b2-510">Ignorar problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-510">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-511">Mínimo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-511">AtLeast</span></span></td>
<td><span data-ttu-id="9d4b2-512">A imagem é pelo menos tão grande quanto o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-512">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-513">AtMost</span><span class="sxs-lookup"><span data-stu-id="9d4b2-513">AtMost</span></span></td>
<td><span data-ttu-id="9d4b2-514">A imagem não é maior que o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-514">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-515">Cor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-515">Color</span></span></td>
<td><span data-ttu-id="9d4b2-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> A cor de preenchimento principal.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="9d4b2-517">Mesmo que o atributo FillColor na forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-517">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-518">Color2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-518">Color2</span></span></td>
<td><span data-ttu-id="9d4b2-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d4b2-520">A cor secundária de um preenchimento quando o tipo de imagem é padrão ou um preenchimento gradiente.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-520">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-521">Cores</span><span class="sxs-lookup"><span data-stu-id="9d4b2-521">Colors</span></span></td>
<td><span data-ttu-id="9d4b2-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="9d4b2-523">Cores intermediárias no gradiente e suas posições relativas ao longo do gradiente, por exemplo, &quot; 30% vermelho, 70% azul, 90% verde &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-523">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="9d4b2-524">A cor primária (atributo de cor em forma) é 0% e a cor secundária (atributo Color2) é de 100%.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-524">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-525">Foco</span><span class="sxs-lookup"><span data-stu-id="9d4b2-525">Focus</span></span></td>
<td><span data-ttu-id="9d4b2-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="9d4b2-527">Ponto focal para preenchimento de gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-527">Focal point for linear gradient fill.</span></span> <span data-ttu-id="9d4b2-528">Os valores vão de-100 a + 100.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-528">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-529">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="9d4b2-529">FocusPosition</span></span></td>
<td><span data-ttu-id="9d4b2-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-531">Posição do retângulo mais interno para gradientes radiais.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-531">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="9d4b2-532">O vetor é uma fração (0,0-1,0) da largura e da altura da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-532">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-533">FocusSize</span><span class="sxs-lookup"><span data-stu-id="9d4b2-533">FocusSize</span></span></td>
<td><span data-ttu-id="9d4b2-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Tamanho do retângulo mais interno para gradientes radiais.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="9d4b2-535">O vetor é uma fração (0,0 a 1,0) da largura e da altura da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-535">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-536">Método</span><span class="sxs-lookup"><span data-stu-id="9d4b2-536">Method</span></span></td>
<td><span data-ttu-id="9d4b2-537">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-537">VgSigmaType.</span></span> <span data-ttu-id="9d4b2-538">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-538">Values include:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-539">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9d4b2-539">None</span></span></li>
<li><span data-ttu-id="9d4b2-540">Linear</span><span class="sxs-lookup"><span data-stu-id="9d4b2-540">Linear</span></span></li>
<li><span data-ttu-id="9d4b2-541">Sigma</span><span class="sxs-lookup"><span data-stu-id="9d4b2-541">Sigma</span></span></li>
<li><span data-ttu-id="9d4b2-542">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9d4b2-542">Any</span></span></li>
</ul>
<p><span data-ttu-id="9d4b2-543">O padrão é Sigma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-543">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-544">Ativado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-544">On</span></span></td>
<td><span data-ttu-id="9d4b2-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-546">Ativa a exibição de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-546">Turns fill display on.</span></span> <span data-ttu-id="9d4b2-547">O mesmo que o atributo Fill na forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-547">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-548">Opacidade</span><span class="sxs-lookup"><span data-stu-id="9d4b2-548">Opacity</span></span></td>
<td><span data-ttu-id="9d4b2-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d4b2-550">Opacidade do preenchimento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-550">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-551">Opacity2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-551">Opacity2</span></span></td>
<td><span data-ttu-id="9d4b2-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d4b2-553">A opacidade secundária para gradientes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-553">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-554">Origem</span><span class="sxs-lookup"><span data-stu-id="9d4b2-554">Origin</span></span></td>
<td><span data-ttu-id="9d4b2-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-556">Ponto relativo ao canto superior esquerdo da imagem que é tratada como a origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-556">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="9d4b2-557">O padrão é o centro da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-557">Default is the center of the image.</span></span> <span data-ttu-id="9d4b2-558">O vetor é uma fração (de 0,0 a 1,0) da largura e da altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-558">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-559">Posição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-559">Position</span></span></td>
<td><span data-ttu-id="9d4b2-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-561">Ponto no retângulo de referência da forma para posicionar a origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-561">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="9d4b2-562">O padrão é o centro do retângulo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-562">Default is the center of the container rectangle.</span></span> <span data-ttu-id="9d4b2-563">O vetor é uma fração (0,0-1,0) da largura e da altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-563">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-564">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9d4b2-564">Size</span></span></td>
<td><span data-ttu-id="9d4b2-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-566">O tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-566">The size of the image.</span></span> <span data-ttu-id="9d4b2-567">O padrão é o tamanho do pixel da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-567">Default is pixel size of the image.</span></span> <span data-ttu-id="9d4b2-568">Pode ser especificado em coordenadas absolutas ou em porcentagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-568">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-569">Src</span><span class="sxs-lookup"><span data-stu-id="9d4b2-569">Src</span></span></td>
<td><span data-ttu-id="9d4b2-570"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-570"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d4b2-571">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-571">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9d4b2-572">Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-572">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-573">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-573">Type</span></span></td>
<td><span data-ttu-id="9d4b2-574">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-574">VgFillType.</span></span> <span data-ttu-id="9d4b2-575">Pode ser um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-575">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-576">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-576">Background</span></span></li>
<li><span data-ttu-id="9d4b2-577">Quadro</span><span class="sxs-lookup"><span data-stu-id="9d4b2-577">Frame</span></span></li>
<li><span data-ttu-id="9d4b2-578">Gradient</span><span class="sxs-lookup"><span data-stu-id="9d4b2-578">Gradient</span></span></li>
<li><span data-ttu-id="9d4b2-579">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="9d4b2-579">GradientCenter</span></span></li>
<li><span data-ttu-id="9d4b2-580">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="9d4b2-580">GradientRadial</span></span></li>
<li><span data-ttu-id="9d4b2-581">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-581">GradientTitle</span></span></li>
<li><span data-ttu-id="9d4b2-582">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="9d4b2-582">GradientUnscaled</span></span></li>
<li><span data-ttu-id="9d4b2-583">Padrão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-583">Pattern</span></span></li>
<li><span data-ttu-id="9d4b2-584">Sólido</span><span class="sxs-lookup"><span data-stu-id="9d4b2-584">Solid</span></span></li>
<li><span data-ttu-id="9d4b2-585">Tile</span><span class="sxs-lookup"><span data-stu-id="9d4b2-585">Tile</span></span></li>
</ul>
<span data-ttu-id="9d4b2-586">O bloco, o padrão e o quadro exigem que os atributos da imagem sejam fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-586">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="9d4b2-587">Gradiente e GradientRadial exigem que os atributos de gradiente sejam fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-587">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="9d4b2-588">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="9d4b2-588">Group element</span></span>

<span data-ttu-id="9d4b2-589">Um grupo é uma coleção de formas individuais que podem ser posicionadas e transformadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-589">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-590">Item</span><span class="sxs-lookup"><span data-stu-id="9d4b2-590">Item</span></span>   | <span data-ttu-id="9d4b2-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-592">Item especificado na matriz de formas.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-592">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="9d4b2-593">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-593">Length</span></span> | <span data-ttu-id="9d4b2-594">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-594">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-595">Número de formas neste grupo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-595">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="9d4b2-596">Elemento ImageData</span><span class="sxs-lookup"><span data-stu-id="9d4b2-596">Imagedata element</span></span>

<span data-ttu-id="9d4b2-597">Descreve uma imagem a ser renderizada na parte superior de uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-597">Describes a picture to be rendered on top of a shape.</span></span>



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-598">Binível</span><span class="sxs-lookup"><span data-stu-id="9d4b2-598">BiLevel</span></span>     | <span data-ttu-id="9d4b2-599">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-599">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-600">Exibir imagem em apenas duas cores (geralmente preto e branco).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-600">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="9d4b2-601">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="9d4b2-601">BlackLevel</span></span>  | <span data-ttu-id="9d4b2-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d4b2-603">Permite ajuste para definir o nível de forma que os pretos apareçam como verdadeiros pretos e todas as outras cores fiquem visíveis como sombras acima do preto.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-603">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="9d4b2-604">Chromakey</span><span class="sxs-lookup"><span data-stu-id="9d4b2-604">Chromakey</span></span>   | <span data-ttu-id="9d4b2-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d4b2-606">Cor transparente da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-606">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9d4b2-607">CropBottom</span><span class="sxs-lookup"><span data-stu-id="9d4b2-607">CropBottom</span></span>  | <span data-ttu-id="9d4b2-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-609">Cortar distância da parte inferior da imagem expressa como uma porcentagem do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-609">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="9d4b2-610">CropLeft</span><span class="sxs-lookup"><span data-stu-id="9d4b2-610">CropLeft</span></span>    | <span data-ttu-id="9d4b2-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-612">Corte de distância da borda esquerda da imagem expressa como uma fração do tamanho da imagem (de 0,0 a 1,0).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-612">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="9d4b2-613">No entanto, o "corte de saída" tem suporte e, portanto, os valores inferiores a 0 e maiores que 1 têm suporte; por exemplo,-5, 20 descortaremos os limites 25X o tamanho da imagem com 4/5 em um lado da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-613">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="9d4b2-614">CropRight</span><span class="sxs-lookup"><span data-stu-id="9d4b2-614">CropRight</span></span>   | <span data-ttu-id="9d4b2-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-616">Cortar distância da direita da imagem expressa como uma porcentagem do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-616">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="9d4b2-617">CropTop</span><span class="sxs-lookup"><span data-stu-id="9d4b2-617">CropTop</span></span>     | <span data-ttu-id="9d4b2-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-619">Cortar distância da parte superior da imagem expressa como uma porcentagem do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-619">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="9d4b2-620">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-620">EmbossColor</span></span> | <span data-ttu-id="9d4b2-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d4b2-622">Isso é definido como uma porcentagem da cor da sombra para criar um efeito de imagem em alto-relevo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-622">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d4b2-623">Conheça</span><span class="sxs-lookup"><span data-stu-id="9d4b2-623">Gain</span></span>        | <span data-ttu-id="9d4b2-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-625">Ajusta a intensidade de todas as cores.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-625">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="9d4b2-626">Basicamente define como o branco brilhante será.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-626">Essentially sets how bright white will be.</span></span> <span data-ttu-id="9d4b2-627">Varia de 0 a 32767.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-627">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="9d4b2-628">Gama</span><span class="sxs-lookup"><span data-stu-id="9d4b2-628">Gamma</span></span>       | <span data-ttu-id="9d4b2-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d4b2-630">Correção gama.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-630">Gamma correction.</span></span> <span data-ttu-id="9d4b2-631">Aumentá-lo dá mais contraste a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-631">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d4b2-632">GrayScale</span><span class="sxs-lookup"><span data-stu-id="9d4b2-632">GrayScale</span></span>   | <span data-ttu-id="9d4b2-633">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-633">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-634">Exibir imagem em cores de escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-634">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d4b2-635">Src</span><span class="sxs-lookup"><span data-stu-id="9d4b2-635">Src</span></span>         | <span data-ttu-id="9d4b2-636">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-636">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-637">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-637">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9d4b2-638">Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-638">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="9d4b2-639">Elemento Path</span><span class="sxs-lookup"><span data-stu-id="9d4b2-639">Path element</span></span>

<span data-ttu-id="9d4b2-640">Define o caminho que compõe a forma, usando uma cadeia de caracteres que contém um conjunto avançado de comandos de "movimento de caneta".</span><span class="sxs-lookup"><span data-stu-id="9d4b2-640">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-641">Limo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-641">Limo</span></span></td>
<td><span data-ttu-id="9d4b2-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="9d4b2-643">Define o ponto em que a forma é alongada; por exemplo, para uma forma Giraffe, o ponto de limo estaria no pescoço, portanto, quando a forma for redimensionada, o pescoço será alongado e o restante da forma manterá suas dimensões.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-643">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-644">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="9d4b2-644">TextBoxRect</span></span></td>
<td><span data-ttu-id="9d4b2-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="9d4b2-646">Matriz que contém os retângulos que definem onde o texto deve ir.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-646">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-647">V</span><span class="sxs-lookup"><span data-stu-id="9d4b2-647">V</span></span></td>
<td><span data-ttu-id="9d4b2-648"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-648"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d4b2-649">Faz a correspondência do atributo v na marca de caminho.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-649">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="9d4b2-650">Observe que o caminho pode corresponder ao atributo ou elemento de caminho.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-650">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-651">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-651">Value</span></span></td>
<td><span data-ttu-id="9d4b2-652"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-652"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d4b2-653">Uma representação de texto dos comandos que definem o caminho.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-653">A text representation of the commands that define the path.</span></span> <span data-ttu-id="9d4b2-654">Os valores de coordenadas X ou y podem ser uma referência a uma fórmula no formulário em &quot; @# &quot; que # é o número ordinal da fórmula, por exemplo, &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-654">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="9d4b2-655">Essa cadeia de caracteres de atributo é composta por um conjunto avançado de comandos, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-655">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-656">Comando</span><span class="sxs-lookup"><span data-stu-id="9d4b2-656">Command</span></span></th>
<th><span data-ttu-id="9d4b2-657">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-657">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-658">AE (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-658">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="9d4b2-659"><strong>Centro</strong>(x, y) <strong>tamanho</strong>(w, h) <strong>início-ângulo</strong>, <strong>ângulo de extremidade</strong></span><span class="sxs-lookup"><span data-stu-id="9d4b2-659"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="9d4b2-660">Desenhe um segmento de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-660">Draw a segment of an ellipse.</span></span> <span data-ttu-id="9d4b2-661">Uma linha reta é desenhada a partir do ponto atual até o ponto inicial do segmento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-661">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-662">Al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-662">al (angleelipse)</span></span></td>
<td><span data-ttu-id="9d4b2-663">O mesmo que a AE, exceto que há um m implícito para o ponto inicial do segmento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-663">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-664">ar (arco)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-664">ar (arc)</span></span></td>
<td><span data-ttu-id="9d4b2-665">O mesmo que em.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-665">Same as at.</span></span> <span data-ttu-id="9d4b2-666">No entanto, um novo subcaminho é iniciado por um m implícito até o ponto inicial do arco.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-666">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-667">at (ArcTo)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-667">at (arcto)</span></span></td>
<td><span data-ttu-id="9d4b2-668"><strong>esquerda</strong>, <strong>superior</strong>, <strong>direita</strong>, <strong>inferior</strong>, <strong>início</strong>(x, y) <strong>fim</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-668"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d4b2-669">Os quatro primeiros valores definem a caixa delimitadora de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-669">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="9d4b2-670">Os últimos quatro definem dois vetores radiais.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-670">The last four define two radial vectors.</span></span> <span data-ttu-id="9d4b2-671">Um segmento da elipse é desenhado que começa no ângulo definido pelo vetor RADIUS inicial e termina no ângulo definido pelo vetor de término.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-671">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="9d4b2-672">Uma linha reta é desenhada a partir do ponto atual até o início do arco. O arco é sempre desenhado em uma direção no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-672">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-673">c (curvato)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-673">c (curveto)</span></span></td>
<td><span data-ttu-id="9d4b2-674"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>para</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-674"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d4b2-675">Desenhe uma curva de Bézier cúbica do ponto atual até a coordenada fornecida pelos dois parâmetros finais, os pontos de controle fornecidos pelos quatro primeiros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-675">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="9d4b2-676">O ponto atual torna-se o ponto de extremidade do Bezier.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-676">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-677">e (final)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-677">e (end)</span></span></td>
<td><span data-ttu-id="9d4b2-678">Finalizar o conjunto atual de subcaminhos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-678">End the current set of subpaths.</span></span> <span data-ttu-id="9d4b2-679">Um determinado conjunto de subcaminhos (como delimitados por fim) é preenchido usando eofill.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-679">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="9d4b2-680">Os conjuntos subsequentes de subcaminhos são preenchidos de forma independente e sobrepostas em itens existentes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-680">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-681">l (LineTo)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-681">l (lineto)</span></span></td>
<td><span data-ttu-id="9d4b2-682">x, y</span><span class="sxs-lookup"><span data-stu-id="9d4b2-682">x,y</span></span><br/> <span data-ttu-id="9d4b2-683">Desenha uma linha do ponto atual para a coordenada x, y, que se torna o novo ponto atual.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-683">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="9d4b2-684">Pares de coordenadas adicionais podem ser especificados para formar uma polilinha, por exemplo, &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-684">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-685">m (MoveTo)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-685">m (moveto)</span></span></td>
<td><span data-ttu-id="9d4b2-686">x, y</span><span class="sxs-lookup"><span data-stu-id="9d4b2-686">x,y</span></span><br/> <span data-ttu-id="9d4b2-687">Inicie um novo subcaminho na coordenada x, y.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-687">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-688">NF (Nofill)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-688">nf (nofill)</span></span></td>
<td><span data-ttu-id="9d4b2-689">O conjunto de subcaminhos atual (delimitado por fim) não será preenchido.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-689">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-690">NS (nostroke)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-690">ns (nostroke)</span></span></td>
<td><span data-ttu-id="9d4b2-691">O conjunto de subcaminhos atual (delimitado por fim) não será traçado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-691">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-692">QB (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-692">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="9d4b2-693">(<strong>ControlPoint</strong>(x, y)) \*,<strong>fim</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-693">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d4b2-694">Define uma ou mais curvas de Bézier quadráticas por meio de pontos de controle e um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-694">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="9d4b2-695">Pontos intermediários (em curva) são obtidos pela interpolação entre pontos de controle sucessivos semelhantes a fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-695">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="9d4b2-696">O subcaminho não precisa ser um início; nesse caso, o subcaminho é fechado e o último ponto define o ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-696">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-697">qx (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-697">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="9d4b2-698"><strong>fim</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-698"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d4b2-699">Uma elipse de trimestre é desenhada do ponto atual para o ponto de extremidade fornecido.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-699">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="9d4b2-700">Inicialmente, o segmento elíptico é tangential a uma linha paralela ao eixo x; ou seja, o segmento começa horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-700">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-701">qy (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-701">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="9d4b2-702"><strong>fim</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-702"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d4b2-703">O mesmo que QX, exceto que o segmento elíptico é inicialmente tangential para uma linha paralela ao eixo y; ou seja, o segmento começa verticalmente.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-703">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-704">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-704">r (rlineto)</span></span></td>
<td><span data-ttu-id="9d4b2-705">x, y</span><span class="sxs-lookup"><span data-stu-id="9d4b2-705">x,y</span></span> <br/> <span data-ttu-id="9d4b2-706">Desenhe uma linha do ponto atual para a coordenada relativa (cpx + x, CPY + y).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-706">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="9d4b2-707">Se pares de coordenadas adicionais forem fornecidos, cada novo ponto será calculado em relação ao último.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-707">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-708">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-708">t (rmoveto)</span></span></td>
<td><span data-ttu-id="9d4b2-709">x, y</span><span class="sxs-lookup"><span data-stu-id="9d4b2-709">x,y</span></span><br/> <span data-ttu-id="9d4b2-710">Inicie um novo subcaminho nas coordenadas relativas (cpx + x, CPY + y) em que cpx, CPY é a posição atual.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-710">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-711">v (curvato)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-711">v (curveto)</span></span></td>
<td><span data-ttu-id="9d4b2-712"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>para</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-712"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="9d4b2-713">Curva de Bézier cúbica usando as coordenadas fornecidas em relação ao ponto atual.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-713">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="9d4b2-714">Todos os pontos são computados em relação ao mesmo ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-714">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-715">WA (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-715">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="9d4b2-716">O mesmo que em, mas o arco é desenhado em uma direção horária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-716">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-717">WR (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-717">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="9d4b2-718">O mesmo que ar, mas é desenhado em direção horária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-718">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-719">x (fechar)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-719">x (close)</span></span></td>
<td><span data-ttu-id="9d4b2-720">Feche o subcaminho atual, desenhando uma linha reta do ponto atual para o ponto de mover original.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-720">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="9d4b2-721">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="9d4b2-721">Shadow element</span></span>

<span data-ttu-id="9d4b2-722">Descreve um efeito de sombra em uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-722">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-723">Cor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-723">Color</span></span></td>
<td><span data-ttu-id="9d4b2-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d4b2-725">Cor da sombra primária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-725">Color of the primary shadow.</span></span> <span data-ttu-id="9d4b2-726">O padrão é RGB (128128128)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-726">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-727">Color2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-727">Color2</span></span></td>
<td><span data-ttu-id="9d4b2-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d4b2-729">Cor da segunda sombra ou realce em uma sombra em relevo ou em baixo-relevo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-729">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="9d4b2-730">O padrão é RGB (203203203).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-730">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-731">Matriz</span><span class="sxs-lookup"><span data-stu-id="9d4b2-731">Matrix</span></span></td>
<td><span data-ttu-id="9d4b2-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="9d4b2-733">Uma matriz de transformação de perspectiva no formato, &quot; Sxx, SXY, syx, syy, px, py &quot; [s = Scale, p = Perspective].</span><span class="sxs-lookup"><span data-stu-id="9d4b2-733">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="9d4b2-734">Os s itens especificam como a sombra deve ser dimensionada em relação à forma, e os itens p especificam como a sombra deve ser distorcida em relação à forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-734">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="9d4b2-735">Por exemplo, a matriz a seguir redimensiona a forma por um fator de 2 e a inclina por um fator de 4 em todas as direções:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-735">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="9d4b2-736">&quot;2, 2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-736">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="9d4b2-737">Essa matriz só será usada se o tipo da sombra for definido como perspectiva.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-737">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-738">Obscurecida</span><span class="sxs-lookup"><span data-stu-id="9d4b2-738">Obscured</span></span></td>
<td><span data-ttu-id="9d4b2-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-740">A sombra pode ser vista por meio de se não houver preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-740">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="9d4b2-741">O padrão é Falso.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-741">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-742">Deslocamento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-742">Offset</span></span></td>
<td><span data-ttu-id="9d4b2-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="9d4b2-744">Valor do deslocamento x, y do local da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-744">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="9d4b2-745">O padrão é &quot; 2PT, 2PT &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-745">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-746">Offset2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-746">Offset2</span></span></td>
<td><span data-ttu-id="9d4b2-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-748">Valor do deslocamento x, y segundo do local da forma? s.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-748">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="9d4b2-749">Os valores são uma medida absoluta ou um valor fracionário de Shape (-0,5 a + 0,5).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-749">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-750">Ativado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-750">On</span></span></td>
<td><span data-ttu-id="9d4b2-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-752">Ativa e desativa a exibição da sombra.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-752">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-753">Opacidade</span><span class="sxs-lookup"><span data-stu-id="9d4b2-753">Opacity</span></span></td>
<td><span data-ttu-id="9d4b2-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d4b2-755">Opacidade do efeito de sombra.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-755">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-756">Origem</span><span class="sxs-lookup"><span data-stu-id="9d4b2-756">Origin</span></span></td>
<td><span data-ttu-id="9d4b2-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Um par de valores fracionários de forma de-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-758">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-758">Type</span></span></td>
<td><span data-ttu-id="9d4b2-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="9d4b2-760">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-760">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-761">Único (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-761">Single (default)</span></span></li>
<li><span data-ttu-id="9d4b2-762">Double</span><span class="sxs-lookup"><span data-stu-id="9d4b2-762">Double</span></span></li>
<li><span data-ttu-id="9d4b2-763">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="9d4b2-763">Perspective</span></span></li>
<li><span data-ttu-id="9d4b2-764">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="9d4b2-764">ShapeRelative</span></span></li>
<li><span data-ttu-id="9d4b2-765">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="9d4b2-765">DrawingRelative</span></span></li>
<li><span data-ttu-id="9d4b2-766">Emboss</span><span class="sxs-lookup"><span data-stu-id="9d4b2-766">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="9d4b2-767">Elemento skew</span><span class="sxs-lookup"><span data-stu-id="9d4b2-767">Skew element</span></span>

<span data-ttu-id="9d4b2-768">Descreve um efeito de inclinação de perspectiva em uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-768">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="9d4b2-769">A distorção é aplicada aos dados gráficos vetoriais, não aos dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-769">The skew is applied to vector graphic data, not image data.</span></span>



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-770">Matriz</span><span class="sxs-lookup"><span data-stu-id="9d4b2-770">Matrix</span></span> | <span data-ttu-id="9d4b2-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-772">Uma matriz de transformação de perspectiva no formato "Sxx, SXY, syx, syy, px, py" \[ s = Scale, p = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-772">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="9d4b2-773">Se o deslocamento estiver em unidades absolutas, então px, py estão nas unidades da UME ^-1; caso contrário, eles são uma fração inversa do tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-773">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="9d4b2-774">Deslocamento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-774">Offset</span></span> | <span data-ttu-id="9d4b2-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-776">Valor do deslocamento x, y do local da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-776">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="9d4b2-777">O padrão é "2PT, 2PT".</span><span class="sxs-lookup"><span data-stu-id="9d4b2-777">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="9d4b2-778">Ativado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-778">On</span></span>     | <span data-ttu-id="9d4b2-779">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-779">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-780">Ativa ou desativa a exibição da distorção.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-780">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="9d4b2-781">Origem</span><span class="sxs-lookup"><span data-stu-id="9d4b2-781">Origin</span></span> | <span data-ttu-id="9d4b2-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-783">Um par de valores fracionários de forma de-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-783">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="9d4b2-784">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="9d4b2-784">Stroke element</span></span>

<span data-ttu-id="9d4b2-785">Descreve como desenhar o caminho se algo além de uma linha sólida com uma cor sólida for desejada.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-785">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-786">Cor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-786">Color</span></span></td>
<td><span data-ttu-id="9d4b2-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-788">A cor da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-788">The color of the line.</span></span> <span data-ttu-id="9d4b2-789">O mesmo que o atributo StrokeColor na forma, mas o substitui.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-789">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-790">Color2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-790">Color2</span></span></td>
<td><span data-ttu-id="9d4b2-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d4b2-792">Cor secundária.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-792">Secondary color.</span></span> <span data-ttu-id="9d4b2-793">Usado quando FillType é padrão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-793">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-794">DashStyle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-794">DashStyle</span></span></td>
<td><span data-ttu-id="9d4b2-795"><strong>VgLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-795"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="9d4b2-796">Formato de estilo de tracejado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-796">Dash style format.</span></span> <span data-ttu-id="9d4b2-797">Pode ser um valor específico ou uma sequência de números com um padrão de Dash definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-797">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="9d4b2-798">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-798">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-799">Solid (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-799">Solid (default)</span></span></li>
<li><span data-ttu-id="9d4b2-800">ShortDash</span><span class="sxs-lookup"><span data-stu-id="9d4b2-800">ShortDash</span></span></li>
<li><span data-ttu-id="9d4b2-801">ShortDot</span><span class="sxs-lookup"><span data-stu-id="9d4b2-801">ShortDot</span></span></li>
<li><span data-ttu-id="9d4b2-802">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="9d4b2-802">ShortDashDot</span></span></li>
<li><span data-ttu-id="9d4b2-803">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="9d4b2-803">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="9d4b2-804">Ponto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-804">Dot</span></span></li>
<li><span data-ttu-id="9d4b2-805">Traço</span><span class="sxs-lookup"><span data-stu-id="9d4b2-805">Dash</span></span></li>
<li><span data-ttu-id="9d4b2-806">DashDot</span><span class="sxs-lookup"><span data-stu-id="9d4b2-806">DashDot</span></span></li>
<li><span data-ttu-id="9d4b2-807">LongDash</span><span class="sxs-lookup"><span data-stu-id="9d4b2-807">LongDash</span></span></li>
<li><span data-ttu-id="9d4b2-808">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="9d4b2-808">LongDashDot</span></span></li>
<li><span data-ttu-id="9d4b2-809">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="9d4b2-809">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-810">Seta de fim</span><span class="sxs-lookup"><span data-stu-id="9d4b2-810">EndArrow</span></span></td>
<td><span data-ttu-id="9d4b2-811"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-811"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="9d4b2-812">Ponta de seta para o final da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-812">Arrowhead for the end of the line.</span></span> <span data-ttu-id="9d4b2-813">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-813">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-814">Nenhum (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-814">None (default)</span></span></li>
<li><span data-ttu-id="9d4b2-815">Bloquear</span><span class="sxs-lookup"><span data-stu-id="9d4b2-815">Block</span></span></li>
<li><span data-ttu-id="9d4b2-816">Clássico</span><span class="sxs-lookup"><span data-stu-id="9d4b2-816">Classic</span></span></li>
<li><span data-ttu-id="9d4b2-817">Diamond</span><span class="sxs-lookup"><span data-stu-id="9d4b2-817">Diamond</span></span></li>
<li><span data-ttu-id="9d4b2-818">Oval</span><span class="sxs-lookup"><span data-stu-id="9d4b2-818">Oval</span></span></li>
<li><span data-ttu-id="9d4b2-819">Aberto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-819">Open</span></span></li>
<li><span data-ttu-id="9d4b2-820">Divisa</span><span class="sxs-lookup"><span data-stu-id="9d4b2-820">Chevron</span></span></li>
<li><span data-ttu-id="9d4b2-821">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="9d4b2-821">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-822">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="9d4b2-822">EndArrowLength</span></span></td>
<td><span data-ttu-id="9d4b2-823"><strong>VgArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-823"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="9d4b2-824">Comprimento da ponta de seta para o fim da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-824">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="9d4b2-825">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-825">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-826">Short</span><span class="sxs-lookup"><span data-stu-id="9d4b2-826">Short</span></span></li>
<li><span data-ttu-id="9d4b2-827">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-827">Medium (default)</span></span></li>
<li><span data-ttu-id="9d4b2-828">long</span><span class="sxs-lookup"><span data-stu-id="9d4b2-828">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-829">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="9d4b2-829">EndArrowWidth</span></span></td>
<td><span data-ttu-id="9d4b2-830"><strong>VgArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-830"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="9d4b2-831">Largura da ponta de seta para o fim da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-831">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="9d4b2-832">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-832">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-833">Encontrar</span><span class="sxs-lookup"><span data-stu-id="9d4b2-833">Narrow</span></span></li>
<li><span data-ttu-id="9d4b2-834">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-834">Medium (default)</span></span></li>
<li><span data-ttu-id="9d4b2-835">Ampla</span><span class="sxs-lookup"><span data-stu-id="9d4b2-835">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-836">EndCap</span><span class="sxs-lookup"><span data-stu-id="9d4b2-836">EndCap</span></span></td>
<td><span data-ttu-id="9d4b2-837"><strong>VgLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-837"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="9d4b2-838">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-838">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-839">Plano</span><span class="sxs-lookup"><span data-stu-id="9d4b2-839">Flat</span></span></li>
<li><span data-ttu-id="9d4b2-840">Square</span><span class="sxs-lookup"><span data-stu-id="9d4b2-840">Square</span></span></li>
<li><span data-ttu-id="9d4b2-841">Round</span><span class="sxs-lookup"><span data-stu-id="9d4b2-841">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-842">FillType</span><span class="sxs-lookup"><span data-stu-id="9d4b2-842">FillType</span></span></td>
<td><span data-ttu-id="9d4b2-843"><strong>VgLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-843"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="9d4b2-844">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-844">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-845">Solid (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-845">Solid (default)</span></span></li>
<li><span data-ttu-id="9d4b2-846">Tile</span><span class="sxs-lookup"><span data-stu-id="9d4b2-846">Tile</span></span></li>
<li><span data-ttu-id="9d4b2-847">Padrão</span><span class="sxs-lookup"><span data-stu-id="9d4b2-847">Pattern</span></span></li>
<li><span data-ttu-id="9d4b2-848">Quadro</span><span class="sxs-lookup"><span data-stu-id="9d4b2-848">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-849">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="9d4b2-849">ImageAlignShape</span></span></td>
<td><span data-ttu-id="9d4b2-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-851">Alinhe a imagem com a forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-851">Align the image with the shape.</span></span> <span data-ttu-id="9d4b2-852">Se for false, alinhar a imagem com a janela.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-852">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-853">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="9d4b2-853">ImageAspect</span></span></td>
<td><span data-ttu-id="9d4b2-854"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-854"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="9d4b2-855">O atributo ImageSize será ajustado para preservar o aspecto da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-855">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="9d4b2-856">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-856">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-857">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-857">Value</span></span></th>
<th><span data-ttu-id="9d4b2-858">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-858">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-859">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9d4b2-859">Ignore</span></span></td>
<td><span data-ttu-id="9d4b2-860">Ignorar problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-860">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-861">Mínimo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-861">AtLeast</span></span></td>
<td><span data-ttu-id="9d4b2-862">A imagem é pelo menos tão grande quanto o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-862">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-863">AtMost</span><span class="sxs-lookup"><span data-stu-id="9d4b2-863">AtMost</span></span></td>
<td><span data-ttu-id="9d4b2-864">A imagem não é maior que o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-864">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-865">ImageSize</span><span class="sxs-lookup"><span data-stu-id="9d4b2-865">ImageSize</span></span></td>
<td><span data-ttu-id="9d4b2-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d4b2-867">Tamanho da imagem com a qual formar o pincel.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-867">Size of the image to form the brush with.</span></span> <span data-ttu-id="9d4b2-868">O padrão é o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-868">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-869">Joinstyle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-869">JoinStyle</span></span></td>
<td><span data-ttu-id="9d4b2-870"><strong>VgLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-870"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="9d4b2-871">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-871">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-872">Round (junção arredondada)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-872">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="9d4b2-873">Bisel (junta chanfrada)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-873">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="9d4b2-874">Mitre (junta de Mitre)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-874">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-875">Estilo de Linha</span><span class="sxs-lookup"><span data-stu-id="9d4b2-875">LineStyle</span></span></td>
<td><span data-ttu-id="9d4b2-876"><strong>VgLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-876"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="9d4b2-877">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-877">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-878">Único</span><span class="sxs-lookup"><span data-stu-id="9d4b2-878">Single</span></span></li>
<li><span data-ttu-id="9d4b2-879">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-879">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="9d4b2-880">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-880">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="9d4b2-881">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-881">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="9d4b2-882">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-882">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-883">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="9d4b2-883">MiterLimit</span></span></td>
<td><span data-ttu-id="9d4b2-884"><a href="msdn-online-vml-vglength.md">Comprimento</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-884"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="9d4b2-885">A distância máxima entre o ponto interno e o ponto externo de uma junção.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-885">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="9d4b2-886">Esse número é um múltiplo da espessura da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-886">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="9d4b2-887">Varia de 0 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-887">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-888">Ativado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-888">On</span></span></td>
<td><span data-ttu-id="9d4b2-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d4b2-890">Ativa e desativa a exibição da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-890">Turns the display of the line on and off.</span></span> <span data-ttu-id="9d4b2-891">O mesmo que o atributo Stroke na forma, mas o substitui.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-891">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-892">Opacidade</span><span class="sxs-lookup"><span data-stu-id="9d4b2-892">Opacity</span></span></td>
<td><span data-ttu-id="9d4b2-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d4b2-894">Opacidade do traço.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-894">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-895">Src</span><span class="sxs-lookup"><span data-stu-id="9d4b2-895">Src</span></span></td>
<td><span data-ttu-id="9d4b2-896">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-896">String.</span></span> <span data-ttu-id="9d4b2-897">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-897">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9d4b2-898">Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-898">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-899">StartArrow</span><span class="sxs-lookup"><span data-stu-id="9d4b2-899">StartArrow</span></span></td>
<td><span data-ttu-id="9d4b2-900"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-900"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="9d4b2-901">Ponta de seta para o início da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-901">Arrowhead for the start of the line.</span></span> <span data-ttu-id="9d4b2-902">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-902">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-903">Nenhum (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-903">None (default)</span></span></li>
<li><span data-ttu-id="9d4b2-904">Bloquear</span><span class="sxs-lookup"><span data-stu-id="9d4b2-904">Block</span></span></li>
<li><span data-ttu-id="9d4b2-905">Clássico</span><span class="sxs-lookup"><span data-stu-id="9d4b2-905">Classic</span></span></li>
<li><span data-ttu-id="9d4b2-906">Diamond</span><span class="sxs-lookup"><span data-stu-id="9d4b2-906">Diamond</span></span></li>
<li><span data-ttu-id="9d4b2-907">Oval</span><span class="sxs-lookup"><span data-stu-id="9d4b2-907">Oval</span></span></li>
<li><span data-ttu-id="9d4b2-908">Aberto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-908">Open</span></span></li>
<li><span data-ttu-id="9d4b2-909">Divisa</span><span class="sxs-lookup"><span data-stu-id="9d4b2-909">Chevron</span></span></li>
<li><span data-ttu-id="9d4b2-910">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="9d4b2-910">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-911">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="9d4b2-911">StartArrowLength</span></span></td>
<td><span data-ttu-id="9d4b2-912">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-912">VgArrowHeadLength.</span></span> <span data-ttu-id="9d4b2-913">Comprimento da ponta de seta para o início da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-913">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="9d4b2-914">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-914">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-915">Short</span><span class="sxs-lookup"><span data-stu-id="9d4b2-915">Short</span></span></li>
<li><span data-ttu-id="9d4b2-916">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-916">Medium (default)</span></span></li>
<li><span data-ttu-id="9d4b2-917">long</span><span class="sxs-lookup"><span data-stu-id="9d4b2-917">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-918">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="9d4b2-918">StartArrowWidth</span></span></td>
<td><span data-ttu-id="9d4b2-919">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-919">VgArrowheadWidth.</span></span> <span data-ttu-id="9d4b2-920">Largura da ponta de seta para o início da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-920">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="9d4b2-921">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-921">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-922">Estreito médio (padrão) largo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-922">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-923">Peso</span><span class="sxs-lookup"><span data-stu-id="9d4b2-923">Weight</span></span></td>
<td><span data-ttu-id="9d4b2-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9d4b2-925">Largura da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-925">Width of line.</span></span> <span data-ttu-id="9d4b2-926">Varia de 0 a 1584.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-926">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="9d4b2-927">O atributo DashStyle permite que o usuário especifique um padrão de traço definido por personalizado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-927">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="9d4b2-928">Isso é feito usando uma série de números.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-928">This is done using a series of numbers.</span></span> <span data-ttu-id="9d4b2-929">Os estilos de traço são definidos em termos do comprimento do traço (a parte desenhada do traço) e o comprimento do espaço entre os traços.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-929">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="9d4b2-930">Os comprimentos são relativos à largura da linha; um comprimento de &quot; 1 &quot; é igual à largura da linha.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-930">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="9d4b2-931">O estilo EndCap é aplicado a cada traço; os estilos de seta não são.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-931">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="9d4b2-932">A cadeia de caracteres define primeiro o comprimento do traço em seguida, o comprimento do espaço.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-932">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="9d4b2-933">Isso pode ser repetido para formar estilos de traço complexos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-933">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="9d4b2-934">A cadeia de caracteres sempre deve conter um par de números; Se ele contiver um número ímpar de números, o último pode ser desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-934">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="9d4b2-935">A tabela a seguir lista alguns valores típicos e uma descrição do efeito pretendido.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-935">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="9d4b2-936">&quot;0 &quot; implica um ponto que deve ser consta simétrico (com Endcaps arredondado deve ser um círculo).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-936">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="9d4b2-937">Se a linha EndCap for simples, um visualizador deverá escolher um sistema operacional interno onde for possível (ou seja, algo que seja rápido de desenhar).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-937">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="9d4b2-938">O exemplo a seguir mostra alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-938">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-939">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-939">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="9d4b2-940">traços curtos (cada traço e o espaço entre é duas vezes a largura da linha)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-940">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-941">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-941">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="9d4b2-942">ponto (cada traço é a largura da linha enquanto cada espaço é duas vezes a largura da linha)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-942">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-943">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-943">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="9d4b2-944">Dash (cada traço é quatro vezes a largura da linha enquanto cada espaço é duas vezes a largura da linha)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-944">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-945">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-945">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="9d4b2-946">tracejado longo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-946">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-947">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-947">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9d4b2-948">traço ponto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-948">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-949">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-949">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9d4b2-950">ponto de tracejado longo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-950">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-951">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d4b2-951">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9d4b2-952">ponto ponto traço longo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-952">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="9d4b2-953">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="9d4b2-953">TextPath element</span></span>

<span data-ttu-id="9d4b2-954">Descreve um caminho de vetor baseado nos dados de texto, na fonte e nos estilos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-954">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="9d4b2-955">O caminho de texto é distorcido para estar em conformidade com um elemento **path** , se fornecido.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-955">The text path is warped to conform to a **Path** element if supplied.</span></span>



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-956">FitPath</span><span class="sxs-lookup"><span data-stu-id="9d4b2-956">FitPath</span></span>  | <span data-ttu-id="9d4b2-957">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-957">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-958">Dimensiona o texto para preencher o caminho em que ele se encontra.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-958">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="9d4b2-959">FitShape</span><span class="sxs-lookup"><span data-stu-id="9d4b2-959">FitShape</span></span> | <span data-ttu-id="9d4b2-960">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-960">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-961">Alonga o caminho do texto para as bordas da caixa de forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-961">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="9d4b2-962">Ativado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-962">On</span></span>       | <span data-ttu-id="9d4b2-963">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-963">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-964">Determina se os caminhos de caracteres são exibidos ou não.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-964">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="9d4b2-965">String</span><span class="sxs-lookup"><span data-stu-id="9d4b2-965">String</span></span>   | <span data-ttu-id="9d4b2-966">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-966">String.</span></span> <span data-ttu-id="9d4b2-967">O texto a ser renderizado como um caminho de texto.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-967">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="9d4b2-968">Trim</span><span class="sxs-lookup"><span data-stu-id="9d4b2-968">Trim</span></span>     | <span data-ttu-id="9d4b2-969">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-969">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-970">Remove qualquer espaço adicional reservado para ascendentes e descendentes, se não for usado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-970">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="9d4b2-971">XScale</span><span class="sxs-lookup"><span data-stu-id="9d4b2-971">XScale</span></span>   | <span data-ttu-id="9d4b2-972">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-972">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-973">Use a medida x reta em vez de medir ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-973">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="9d4b2-974">Tipos de dados usados no modelo de objeto VML</span><span class="sxs-lookup"><span data-stu-id="9d4b2-974">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="9d4b2-975">Os tipos de dados a seguir são usados pelo modelo de objeto VML.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-975">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="9d4b2-976">Double</span><span class="sxs-lookup"><span data-stu-id="9d4b2-976">Double</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-977">Fixo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-977">Fixed</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-978">Inteiro</span><span class="sxs-lookup"><span data-stu-id="9d4b2-978">Integer</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-979">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="9d4b2-979">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-980">IVgColor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-980">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-981">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="9d4b2-981">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-982">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-982">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-983">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="9d4b2-983">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-984">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="9d4b2-984">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-985">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="9d4b2-985">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-986">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="9d4b2-986">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-987">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="9d4b2-987">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-988">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="9d4b2-988">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-989">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="9d4b2-989">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-990">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="9d4b2-990">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-991">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="9d4b2-991">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-992">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-992">Length</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-993">Medida</span><span class="sxs-lookup"><span data-stu-id="9d4b2-993">Measure</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-994">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="9d4b2-994">String</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-995">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="9d4b2-995">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-996">VgFraction</span><span class="sxs-lookup"><span data-stu-id="9d4b2-996">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="9d4b2-997">VgTriState</span><span class="sxs-lookup"><span data-stu-id="9d4b2-997">VgTriState</span></span>](/windows)

<span data-ttu-id="9d4b2-998">**Tipo de dados Double**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-998">**Double data type**</span></span>

<span data-ttu-id="9d4b2-999">Um inteiro de precisão dupla com intervalo de-infinito para infinito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-999">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="9d4b2-1000">**Tipo de dados fixo**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1000">**Fixed data type**</span></span>

<span data-ttu-id="9d4b2-1001">Número de ponto flutuante com intervalo de-32766,0 a 32766,0.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1001">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="9d4b2-1002">**Tipo de dados Integer**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1002">**Integer data type**</span></span>

<span data-ttu-id="9d4b2-1003">Um número inteiro com um intervalo de-infinito para infinito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1003">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="9d4b2-1004">**Tipo de dados IVgAdjustments**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1004">**IVgAdjustments data type**</span></span>

<span data-ttu-id="9d4b2-1005">Coleção de ajustes em uma forma que pode ser usada para alterar as dimensões de uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1005">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="9d4b2-1006">Os ajustes podem ser usados como espaços reservados temporários ou por qualquer motivo que você usaria variáveis.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1006">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="9d4b2-1007">Há apenas oito ajustes na coleção.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1007">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="9d4b2-1008">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1008">Attributes</span></span> | <span data-ttu-id="9d4b2-1009">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1009">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1010">Exists</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1010">Exists</span></span>     | <span data-ttu-id="9d4b2-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d4b2-1012">Determina se existe um ajuste especificado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1012">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="9d4b2-1013">Observe que um índice deve ser usado; ou seja, Exists (item) deve ser usado para recuperar a existência de um item.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1013">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9d4b2-1014">Item</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1014">Item</span></span>       | <span data-ttu-id="9d4b2-1015">[Longo](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1015">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1016">Matriz de ajustes indexados de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1016">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="9d4b2-1017">Observe que os ajustes podem ser do SPARC especificado; ou seja, os valores intermediários da matriz nem sempre podem ser preenchidos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1017">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="9d4b2-1018">Por exemplo, item 1, 3 e 5 podem ter valores para um comprimento de 3, com item (0), Item (2) e item (4) especificado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1018">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="9d4b2-1019">Para ver se existe um item, use o atributo Exists.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1019">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="9d4b2-1020">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1020">Length</span></span>     | <span data-ttu-id="9d4b2-1021">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1021">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1022">Número de ajustes.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1022">Number of adjustments.</span></span> <span data-ttu-id="9d4b2-1023">Não pode ser maior que 8.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1023">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9d4b2-1024">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1024">Value</span></span>      | <span data-ttu-id="9d4b2-1025">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1025">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1026">Representação de texto de valores numéricos, com vírgulas entre cada número.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1026">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="9d4b2-1027">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1027">**IVgColor**</span></span>

<span data-ttu-id="9d4b2-1028">Especifica uma cor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1028">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-1029">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1029">Attributes</span></span></th>
<th><span data-ttu-id="9d4b2-1030">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1030">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1031">RGB</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1031">RGB</span></span></td>
<td><span data-ttu-id="9d4b2-1032"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1032"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="9d4b2-1033">Valor RGB (Long) da cor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1033">RGB value (Long) of the color.</span></span> <span data-ttu-id="9d4b2-1034">Somente válido se o tipo for RGB.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1034">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1035">R</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1035">R</span></span></td>
<td><span data-ttu-id="9d4b2-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9d4b2-1037">Componente vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1037">Red component of the color.</span></span> <span data-ttu-id="9d4b2-1038">Pode variar entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1038">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1039">G</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1039">G</span></span></td>
<td><span data-ttu-id="9d4b2-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9d4b2-1041">Componente verde da cor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1041">Green component of the color.</span></span> <span data-ttu-id="9d4b2-1042">Pode variar entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1042">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1043">B</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1043">B</span></span></td>
<td><span data-ttu-id="9d4b2-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9d4b2-1045">Componente azul da cor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1045">Blue component of the color.</span></span> <span data-ttu-id="9d4b2-1046">Pode variar entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1046">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1047">String</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1047">String</span></span></td>
<td><span data-ttu-id="9d4b2-1048"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1048"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d4b2-1049">Representação de texto da cor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1049">Text representation of the color.</span></span> <span data-ttu-id="9d4b2-1050">Há suporte para os seguintes tipos de cor nomeados:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1050">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-1051">Preto (#000000)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1051">Black (#000000)</span></span></li>
<li><span data-ttu-id="9d4b2-1052">Prata (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1052">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="9d4b2-1053">Cinza (#808080)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1053">Gray (#808080)</span></span></li>
<li><span data-ttu-id="9d4b2-1054">Branco (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1054">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="9d4b2-1055">Bordô (#800000)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1055">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="9d4b2-1056">Vermelho (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1056">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="9d4b2-1057">Roxo (#800080)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1057">Purple (#800080)</span></span></li>
<li><span data-ttu-id="9d4b2-1058">Fuchsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1058">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="9d4b2-1059">Verde (#008000)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1059">Green (#008000)</span></span></li>
<li><span data-ttu-id="9d4b2-1060">Verde-limão (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1060">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="9d4b2-1061">Verde-oliva (#808000)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1061">Olive (#808000)</span></span></li>
<li><span data-ttu-id="9d4b2-1062">Amarelo (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1062">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="9d4b2-1063">Azul (#000080)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1063">Navy (#000080)</span></span></li>
<li><span data-ttu-id="9d4b2-1064">Azul (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1064">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="9d4b2-1065">Azul-petróleo (#008080)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1065">Teal (#008080)</span></span></li>
<li><span data-ttu-id="9d4b2-1066">Azul-piscina (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1066">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1067">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1067">Type</span></span></td>
<td><span data-ttu-id="9d4b2-1068"><strong>VgColorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1068"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="9d4b2-1069">Tipo de cor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1069">Type of color.</span></span> <span data-ttu-id="9d4b2-1070">Um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1070">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-1071">Mixed</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1071">Mixed</span></span></li>
<li><span data-ttu-id="9d4b2-1072">nomeado</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1072">Named</span></span></li>
<li><span data-ttu-id="9d4b2-1073">RGB</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1073">RGB</span></span></li>
<li><span data-ttu-id="9d4b2-1074">Esquema</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1074">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d4b2-1075">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1075">**IVgEquation**</span></span>

<span data-ttu-id="9d4b2-1076">Equações usadas para fórmulas.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1076">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1077">Operação</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1077">Operation</span></span></td>
<td><span data-ttu-id="9d4b2-1078"><strong>VgEquationOperationType</strong> Nome da operação a ser executada nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1078"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="9d4b2-1079">As seguintes operações podem ser usadas em uma equação:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1079">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-1080">Operação</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1080">Operation</span></span></th>
<th><span data-ttu-id="9d4b2-1081">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1081">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1082">Abs</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1082">Abs</span></span></td>
<td><span data-ttu-id="9d4b2-1083">Valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1083">Absolute value.</span></span> <br/> <span data-ttu-id="9d4b2-1084"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1084"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1085">Atan2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1085">Atan2</span></span></td>
<td><span data-ttu-id="9d4b2-1086">Aritmética polar--resulta em unidades FD (graus multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1086">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="9d4b2-1087"><strong>ATAN2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1087"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1088">Cos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1088">Cos</span></span></td>
<td><span data-ttu-id="9d4b2-1089">Cosseno, argumento em unidades FD (graus multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1089">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="9d4b2-1090">v \* <strong>cos</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1090">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1091">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1091">Cosatan2</span></span></td>
<td><span data-ttu-id="9d4b2-1092">Preserva a precisão total no cálculo intermediário.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1092">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="9d4b2-1093">v \* <strong>cos (ATAN2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="9d4b2-1093">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1094">Ellipse</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1094">Ellipse</span></span></td>
<td><span data-ttu-id="9d4b2-1095">Ellipse</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1095">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1096">If</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1096">If</span></span></td>
<td><span data-ttu-id="9d4b2-1097">Se o teste de condição.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1097">If Condition test.</span></span> <span data-ttu-id="9d4b2-1098">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="9d4b2-1098">v > 0 <strong>?</strong></span></span> <span data-ttu-id="9d4b2-1099">P1: P2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1099">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1100">Máx</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1100">Max</span></span></td>
<td><span data-ttu-id="9d4b2-1101">O maior de dois valores.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1101">The greater of two values.</span></span> <br/> <span data-ttu-id="9d4b2-1102"><strong>Max</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1102"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1103">Mid</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1103">Mid</span></span></td>
<td><span data-ttu-id="9d4b2-1104">Média (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1104">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1105">Min</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1105">Min</span></span></td>
<td><span data-ttu-id="9d4b2-1106">O menor de dois valores.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1106">The lesser of two values.</span></span> <span data-ttu-id="9d4b2-1107"><strong>mín</strong>. (v, P1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1107"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1108">Mod</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1108">Mod</span></span></td>
<td><span data-ttu-id="9d4b2-1109">Módulo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1109">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1110">Produto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1110">Product</span></span></td>
<td><span data-ttu-id="9d4b2-1111">Usado para multiplicação e divisão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1111">Used for multiplication and division.</span></span> <span data-ttu-id="9d4b2-1112">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1112">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1113">Sin</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1113">Sin</span></span></td>
<td><span data-ttu-id="9d4b2-1114">Seno, argumento em unidades FD (graus multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1114">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="9d4b2-1115">v \* <strong>sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1115">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1116">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1116">Sinatan2</span></span></td>
<td><span data-ttu-id="9d4b2-1117">Preserva a precisão total no cálculo intermediário.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1117">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="9d4b2-1118">v \* <strong>sin</strong>(<strong>ATAN2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1119">Sqrt</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1119">Sqrt</span></span></td>
<td><span data-ttu-id="9d4b2-1120">O resultado é positivo e arredonda para baixo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1120">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="9d4b2-1121"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1121"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1122">Somar</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1122">Sum</span></span></td>
<td><span data-ttu-id="9d4b2-1123">Usado para adição e subtração.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1123">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="9d4b2-1124">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1124">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1125">Sumangle</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1125">Sumangle</span></span></td>
<td><span data-ttu-id="9d4b2-1126">Ângulo existente (dimensionado por 65536), onde P1 e P2 estão em graus.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1126">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="9d4b2-1127">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1127">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1128">Tan</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1128">Tan</span></span></td>
<td><span data-ttu-id="9d4b2-1129">Tangente, o argumento está em unidades FD (graus multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1129">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="9d4b2-1130">v \* tan (P1)</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1130">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1131">Val</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1131">Val</span></span></td>
<td><span data-ttu-id="9d4b2-1132">Define um valor de guia de algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1132">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1133">Param1</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1133">Param1</span></span></td>
<td><span data-ttu-id="9d4b2-1134"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1134"><strong>Integer</strong>.</span></span> <span data-ttu-id="9d4b2-1135">O primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1135">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1136">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1136">Paramtype1</span></span></td>
<td><span data-ttu-id="9d4b2-1137"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1137"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="9d4b2-1138">O tipo do primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1138">The type of the first parameter.</span></span> <span data-ttu-id="9d4b2-1139">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1139">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-1140">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1140">Type</span></span></th>
<th><span data-ttu-id="9d4b2-1141">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1142">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1142">Value</span></span></td>
<td><span data-ttu-id="9d4b2-1143">O parâmetro é um valor simples.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1143">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1144">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1144">AdjustmentReference</span></span></td>
<td><span data-ttu-id="9d4b2-1145">O parâmetro é uma referência a um ajuste.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1145">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="9d4b2-1146">Por exemplo, se o primeiro parâmetro for 1, o valor do primeiro ajuste será usado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1146">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1147">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1147">FormulaReference</span></span></td>
<td><span data-ttu-id="9d4b2-1148">O parâmetro é o resultado de uma referência ao resultado de uma fórmula anterior.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1148">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="9d4b2-1149">Por exemplo, se o primeiro parâmetro for 2, o resultado da fórmula 2 será usado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1149">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1150">Param2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1150">Param2</span></span></td>
<td><span data-ttu-id="9d4b2-1151"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1151"><strong>Integer</strong>.</span></span> <span data-ttu-id="9d4b2-1152">O segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1152">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1153">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1153">Paramtype2</span></span></td>
<td><span data-ttu-id="9d4b2-1154"><strong>VgFormulaParamType</strong> O tipo de parâmetro 2.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1154"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1155">Val</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1155">Val</span></span></td>
<td><span data-ttu-id="9d4b2-1156"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1156"><strong>Integer</strong>.</span></span> <span data-ttu-id="9d4b2-1157">O resultado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1157">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1158">Valtype2</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1158">Valtype2</span></span></td>
<td><span data-ttu-id="9d4b2-1159"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1159"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="9d4b2-1160">O tipo do resultado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1160">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d4b2-1161">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1161">**IVgFixedRectangle**</span></span>

<span data-ttu-id="9d4b2-1162">Especifica um retângulo fixo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1162">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="9d4b2-1163">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1163">Attributes</span></span> | <span data-ttu-id="9d4b2-1164">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1164">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1165">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1165">Value</span></span>      | <span data-ttu-id="9d4b2-1166">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1166">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1167">Valor de texto que especifica o caminho.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1167">Text value specifying the path.</span></span>         |
| <span data-ttu-id="9d4b2-1168">Esquerda</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1168">Left</span></span>       | <span data-ttu-id="9d4b2-1169">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1169">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1170">Coordenada da extrema esquerda do retângulo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1170">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="9d4b2-1171">Parte superior</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1171">Top</span></span>        | <span data-ttu-id="9d4b2-1172">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1172">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1173">Coordenada superior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1173">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="9d4b2-1174">Direita</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1174">Right</span></span>      | <span data-ttu-id="9d4b2-1175">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1175">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1176">Coordenada da extrema direita do retângulo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1176">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="9d4b2-1177">Inferior</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1177">Bottom</span></span>     | <span data-ttu-id="9d4b2-1178">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1178">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1179">Coordenada inferior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1179">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="9d4b2-1180">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1180">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="9d4b2-1181">Matriz de retângulos fixos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1181">Array of fixed rectangles.</span></span>



| <span data-ttu-id="9d4b2-1182">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1182">Attributes</span></span> | <span data-ttu-id="9d4b2-1183">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1183">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1184">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1184">Value</span></span>      | <span data-ttu-id="9d4b2-1185">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1185">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1186">Representação de texto da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1186">Text representation of array.</span></span>                           |
| <span data-ttu-id="9d4b2-1187">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1187">Length</span></span>     | <span data-ttu-id="9d4b2-1188">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1188">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1189">Número de retângulos nesta matriz.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1189">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="9d4b2-1190">Item</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1190">Item</span></span>       | <span data-ttu-id="9d4b2-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1192">O objeto Rectangle no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1192">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="9d4b2-1193">Tipo de dados **IVgFormula**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1193">**IVgFormula** data type</span></span>

<span data-ttu-id="9d4b2-1194">Definições para fórmulas que podem variar o caminho de uma forma ou ser usadas para outras finalidades de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1194">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="9d4b2-1195">As fórmulas podem se basear no atributo **adj** de uma forma, que pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1195">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="9d4b2-1196">As fórmulas também podem fazer referência a outras fórmulas.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1196">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="9d4b2-1197">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1197">Attributes</span></span> | <span data-ttu-id="9d4b2-1198">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1199">Eqn</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1199">Eqn</span></span>        | <span data-ttu-id="9d4b2-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1201">Cada fórmula define um único valor como o resultado da avaliação da expressão.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1201">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="9d4b2-1202">A expressão é definida por esse atributo e tem a forma geral de uma operação seguida por até três argumentos, que podem ser valores de ajuste (por exemplo, \# 2), os resultados de fórmulas anteriores (por exemplo, @2 ), números fixos ou valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1202">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="9d4b2-1203">**Tipo de dados IVgFormulas**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1203">**IVgFormulas data type**</span></span>

<span data-ttu-id="9d4b2-1204">Uma coleção de objetos de fórmula.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1204">A collection of formula objects.</span></span>



| <span data-ttu-id="9d4b2-1205">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1205">Attributes</span></span> | <span data-ttu-id="9d4b2-1206">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1206">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1207">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1207">Length</span></span>     | <span data-ttu-id="9d4b2-1208">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1208">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1209">Número de objetos de fórmula na coleção.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1209">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="9d4b2-1210">Item</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1210">Item</span></span>       | <span data-ttu-id="9d4b2-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1212">Uma fórmula específica.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1212">A specific formula.</span></span> <span data-ttu-id="9d4b2-1213">Observe que a matriz de fórmulas pode ser herdada do tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1213">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="9d4b2-1214">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1214">**IVgGradientColorArray**</span></span>

<span data-ttu-id="9d4b2-1215">Uma matriz de cores que define um gradiente (intervalo combinado de cores).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1215">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="9d4b2-1216">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1216">Attributes</span></span> | <span data-ttu-id="9d4b2-1217">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1217">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1218">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1218">Value</span></span>      | <span data-ttu-id="9d4b2-1219">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1219">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1220">Especifica a matriz de cores; por exemplo, "vermelho. 2; verde. 4; Black. 7 "</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1220">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="9d4b2-1221">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1221">Length</span></span>     | <span data-ttu-id="9d4b2-1222">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1222">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1223">Número de cores na matriz.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1223">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="9d4b2-1224">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1224">Methods</span></span>     | <span data-ttu-id="9d4b2-1225">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1225">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1226">Addcolor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1226">AddColor</span></span>    | <span data-ttu-id="9d4b2-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d4b2-1228">Adiciona uma nova cor no ponto de extremidade especificado por fração.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1228">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="9d4b2-1229">A nova cor é branca por padrão e é o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1229">The new color is white by default and is the return value.</span></span> <span data-ttu-id="9d4b2-1230">A cor pode ser alterada por referência.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1230">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="9d4b2-1231">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1231">RemoveColor</span></span> | <span data-ttu-id="9d4b2-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d4b2-1233">Remove uma cor no ponto de extremidade especificado por fração.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1233">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="9d4b2-1234">Observação: se 0,0 ou 1,0 não existir, ele será implícito e a cor branca será usada nesse ponto.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1234">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="9d4b2-1235">**Tipo de dados IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1235">**IVgPoints datatype**</span></span>

<span data-ttu-id="9d4b2-1236">Matriz de pontos que define uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1236">Array of points that define a shape.</span></span>



| <span data-ttu-id="9d4b2-1237">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1237">Attributes</span></span> | <span data-ttu-id="9d4b2-1238">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1238">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4b2-1239">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1239">Value</span></span>      | <span data-ttu-id="9d4b2-1240">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1240">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1241">Representação de texto da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1241">Text representation of array.</span></span>           |
| <span data-ttu-id="9d4b2-1242">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1242">Length</span></span>     | <span data-ttu-id="9d4b2-1243">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1243">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d4b2-1244">Número de pontos nesta matriz.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1244">Number of points in this array.</span></span>        |
| <span data-ttu-id="9d4b2-1245">Item</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1245">Item</span></span>       | <span data-ttu-id="9d4b2-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d4b2-1247">O ponto no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1247">The point at the specified index.</span></span> |



 

<span data-ttu-id="9d4b2-1248">**Tipo de dados IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1248">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="9d4b2-1249">Uma matriz usada para inclinar formas, uma matriz de transformação de perspectiva no formato "*Sxx, SXY, syx, syy, px, py* " \[ *s* = Scale, *p* = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1249">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="9d4b2-1250">Se o deslocamento estiver em unidades absolutas, *px, py* estão nas unidades da UME ^-1; caso contrário, eles são uma fração inversa do tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1250">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="9d4b2-1251">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1251">Attributes</span></span>   | <span data-ttu-id="9d4b2-1252">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1252">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="9d4b2-1253">XtoX</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1253">XtoX</span></span>         | <span data-ttu-id="9d4b2-1254">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1254">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d4b2-1255">YtoX</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1255">YtoX</span></span>         | <span data-ttu-id="9d4b2-1256">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1256">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d4b2-1257">XtoY</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1257">XtoY</span></span>         | <span data-ttu-id="9d4b2-1258">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1258">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d4b2-1259">YtoY</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1259">YtoY</span></span>         | <span data-ttu-id="9d4b2-1260">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1260">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d4b2-1261">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1261">PerspectiveX</span></span> | <span data-ttu-id="9d4b2-1262">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1262">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d4b2-1263">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1263">PerspectiveY</span></span> | <span data-ttu-id="9d4b2-1264">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1264">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="9d4b2-1265">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1265">**IVgSkewOffset**</span></span>

<span data-ttu-id="9d4b2-1266">Especifica o deslocamento da distorção.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1266">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-1267">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1267">Attributes</span></span></th>
<th><span data-ttu-id="9d4b2-1268">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1269">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1269">Value</span></span></td>
<td><span data-ttu-id="9d4b2-1270"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1270"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d4b2-1271">Representação de texto do deslocamento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1271">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1272">X</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1272">X</span></span></td>
<td><span data-ttu-id="9d4b2-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d4b2-1274">Componente X.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1274">X component.</span></span> <span data-ttu-id="9d4b2-1275">Porcentagem ou medida.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1275">Percentage or measure.</span></span> <span data-ttu-id="9d4b2-1276">Se não houver unidades, o tipo ShapeRelative será implícito; caso contrário, o tipo absoluto será implícito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1276">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1277">S</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1277">Y</span></span></td>
<td><span data-ttu-id="9d4b2-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d4b2-1279">Componente Y.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1279">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1280">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1280">Type</span></span></td>
<td><span data-ttu-id="9d4b2-1281"><strong>VgSkewTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1281"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="9d4b2-1282">Especifica o tipo de transformação.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1282">Specifies the type of transformation.</span></span> <span data-ttu-id="9d4b2-1283">Os valores válidos são pontos inteiros que variam entre-infinito e infinito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1283">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-1284">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1284">Type</span></span></th>
<th><span data-ttu-id="9d4b2-1285">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1286">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1286">ShapeRelative</span></span></td>
<td><span data-ttu-id="9d4b2-1287">Os valores do deslocamento são porcentagens (proporção) do tamanho da forma original; por exemplo, um valor de 0,5 significa um deslocamento metade do tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1287">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1288">Absoluto</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1288">Absolute</span></span></td>
<td><span data-ttu-id="9d4b2-1289">Os valores são unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1289">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d4b2-1290">**Tipo de dados IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1290">**IVgVector2D data type**</span></span>

<span data-ttu-id="9d4b2-1291">Especifica um vetor bidimensional que consiste em dois números **duplos** .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1291">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d4b2-1292">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1292">Attributes</span></span></th>
<th><span data-ttu-id="9d4b2-1293">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1293">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1294">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1294">Value</span></span></td>
<td><span data-ttu-id="9d4b2-1295"><strong>Cadeia de caracteres</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1295"><strong>String</strong>.</span></span> <span data-ttu-id="9d4b2-1296">Representação de texto de ambos os números de vetor separados por um espaço.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1296">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1297">X</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1297">X</span></span></td>
<td><span data-ttu-id="9d4b2-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d4b2-1299">Componente X deste vetor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1299">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1300">S</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1300">Y</span></span></td>
<td><span data-ttu-id="9d4b2-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d4b2-1302">Componente Y deste vetor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1302">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1303">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1303">Type</span></span></td>
<td><span data-ttu-id="9d4b2-1304"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1304"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="9d4b2-1305">Unidades esperadas para este vetor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1305">Expected units for this vector.</span></span> <span data-ttu-id="9d4b2-1306">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1306">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-1307">Medida</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1307">Measure</span></span></li>
<li><span data-ttu-id="9d4b2-1308">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1308">Length</span></span></li>
<li><span data-ttu-id="9d4b2-1309">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1309">AngleInDegrees</span></span></li>
<li><span data-ttu-id="9d4b2-1310">Fraction</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1310">Fraction</span></span></li>
<li><span data-ttu-id="9d4b2-1311">Número inteiro de porcentagem de números</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1311">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d4b2-1312">**Tipo de dados IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1312">**IVgVector3D data type**</span></span>

<span data-ttu-id="9d4b2-1313">Especifica um vetor tridimensional que consiste em três números **duplos** .</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1313">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1314">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1314">Value</span></span></td>
<td><span data-ttu-id="9d4b2-1315"><strong>Cadeia de caracteres</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1315"><strong>String</strong>.</span></span> <span data-ttu-id="9d4b2-1316">Representação de texto de três números de vetor separados por um espaço.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1316">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1317">X</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1317">X</span></span></td>
<td><span data-ttu-id="9d4b2-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d4b2-1319">Componente X deste vetor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1319">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1320">S</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1320">Y</span></span></td>
<td><span data-ttu-id="9d4b2-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d4b2-1322">Componente Y deste vetor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1322">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d4b2-1323">Z</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1323">Z</span></span></td>
<td><span data-ttu-id="9d4b2-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d4b2-1325">Componente Z deste vetor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1325">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d4b2-1326">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1326">Type</span></span></td>
<td><span data-ttu-id="9d4b2-1327"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1327"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="9d4b2-1328">Unidades esperadas para este vetor.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1328">Expected units for this vector.</span></span> <span data-ttu-id="9d4b2-1329">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1329">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d4b2-1330">Medida</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1330">Measure</span></span></li>
<li><span data-ttu-id="9d4b2-1331">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1331">Length</span></span></li>
<li><span data-ttu-id="9d4b2-1332">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1332">AngleInDegrees</span></span></li>
<li><span data-ttu-id="9d4b2-1333">Fraction</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1333">Fraction</span></span></li>
<li><span data-ttu-id="9d4b2-1334">Número</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1334">Number</span></span></li>
<li><span data-ttu-id="9d4b2-1335">Percentual</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1335">Percentage</span></span></li>
<li><span data-ttu-id="9d4b2-1336">Integer</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1336">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d4b2-1337">**Tipo de dados length**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1337">**Length data type**</span></span>

<span data-ttu-id="9d4b2-1338">Um número de ponto flutuante com um intervalo de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1338">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="9d4b2-1339">**Tipo de dados Measure**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1339">**Measure data type**</span></span>

<span data-ttu-id="9d4b2-1340">Um número de ponto flutuante de-infinito para infinito.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1340">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="9d4b2-1341">**Tipo de dados String**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1341">**String data type**</span></span>

<span data-ttu-id="9d4b2-1342">Dados de caractere de qualquer comprimento.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1342">Character data of any length.</span></span>

<span data-ttu-id="9d4b2-1343">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1343">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="9d4b2-1344">Modo de renderização para preto e branco.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1344">Rendering mode for black and white.</span></span> <span data-ttu-id="9d4b2-1345">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1345">Possible values are:</span></span>

-   <span data-ttu-id="9d4b2-1346">**Cor**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1346">**Color**</span></span>
-   <span data-ttu-id="9d4b2-1347">**Automático**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1347">**Auto**</span></span>
-   <span data-ttu-id="9d4b2-1348">**Escala**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1348">**GrayScale**</span></span>
-   <span data-ttu-id="9d4b2-1349">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1349">**LightGrayScale**</span></span>
-   <span data-ttu-id="9d4b2-1350">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1350">**InverseGray**</span></span>
-   <span data-ttu-id="9d4b2-1351">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1351">**GrayOutline**</span></span>
-   <span data-ttu-id="9d4b2-1352">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1352">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="9d4b2-1353">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1353">**HighContrast**</span></span>
-   <span data-ttu-id="9d4b2-1354">**Preto**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1354">**Black**</span></span>
-   <span data-ttu-id="9d4b2-1355">**Branca**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1355">**White**</span></span>
-   <span data-ttu-id="9d4b2-1356">**Não desenhado**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1356">**Undrawn**</span></span>

<span data-ttu-id="9d4b2-1357">**Tipo de dados VgFraction**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1357">**VgFraction data type**</span></span>

<span data-ttu-id="9d4b2-1358">Número de ponto flutuante com intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1358">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="9d4b2-1359">As frações também podem ser especificadas como uma porcentagem; por exemplo, "50%".</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1359">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="9d4b2-1360">**Tipo de dados VgTriState**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1360">**VgTriState datatype**</span></span>

<span data-ttu-id="9d4b2-1361">Enumeração usada para valores que podem ser um dos três Estados:</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1361">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="9d4b2-1362">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1362">**TRUE**</span></span>
-   <span data-ttu-id="9d4b2-1363">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1363">**FALSE**</span></span>
-   <span data-ttu-id="9d4b2-1364">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="9d4b2-1364">**MIXED**</span></span>