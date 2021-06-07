---
title: Referência do modelo de objeto VML
description: Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c387935119babc73442e9b8f307672925bdf71d3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444817"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="70912-104">Referência do modelo de objeto VML</span><span class="sxs-lookup"><span data-stu-id="70912-104">VML Object Model Reference</span></span>

<span data-ttu-id="70912-105">Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="70912-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="70912-106">As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="70912-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="70912-107">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="70912-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="70912-108">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="70912-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="70912-109">Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="70912-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="70912-110">Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="70912-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="70912-111">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="70912-111">In this topic:</span></span>

-   [<span data-ttu-id="70912-112">Introdução</span><span class="sxs-lookup"><span data-stu-id="70912-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="70912-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="70912-113">Example</span></span>](#example)
-   [<span data-ttu-id="70912-114">Configurando o VML</span><span class="sxs-lookup"><span data-stu-id="70912-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="70912-115">Referência de OM do VML</span><span class="sxs-lookup"><span data-stu-id="70912-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="70912-116">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="70912-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="70912-117">Subelementos do elemento Shape</span><span class="sxs-lookup"><span data-stu-id="70912-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="70912-118">Elemento Background</span><span class="sxs-lookup"><span data-stu-id="70912-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="70912-119">Elemento Deiaion</span><span class="sxs-lookup"><span data-stu-id="70912-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="70912-120">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="70912-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="70912-121">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="70912-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="70912-122">Elemento Imagedata</span><span class="sxs-lookup"><span data-stu-id="70912-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="70912-123">Elemento Path</span><span class="sxs-lookup"><span data-stu-id="70912-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="70912-124">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="70912-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="70912-125">Elemento Skew</span><span class="sxs-lookup"><span data-stu-id="70912-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="70912-126">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="70912-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="70912-127">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="70912-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="70912-128">Tipos de dados usados no modelo de objeto VML</span><span class="sxs-lookup"><span data-stu-id="70912-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="70912-129">Introdução</span><span class="sxs-lookup"><span data-stu-id="70912-129">Introduction</span></span>

<span data-ttu-id="70912-130">[linguagem VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) é uma linguagem baseada em texto que usa [XML](https://www.w3.org/TR/REC-xml.mdl) para estender HTML com a finalidade de exibir informações gráficas vetoriais.</span><span class="sxs-lookup"><span data-stu-id="70912-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="70912-131">O DOM (Modelo de Objeto do Documento VML) define uma interface programática para a manipulação dos elementos do documento.</span><span class="sxs-lookup"><span data-stu-id="70912-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="70912-132">Isso permite que o usuário crie e modifique dinamicamente elementos gráficos vetoriais por meio de uma interface de plataforma e neutralidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="70912-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="70912-133">O DOM do VML está em conformidade com a [Modelo de Objeto do Documento](https://www.w3.org/TR/REC-DOM-Level-1/) especificação.</span><span class="sxs-lookup"><span data-stu-id="70912-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="70912-134">O VML usa o [elemento Shape](#shape-element) como o bloco de construção básico para imagens gráficas vetoriais.</span><span class="sxs-lookup"><span data-stu-id="70912-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="70912-135">Depois que uma forma é criada, você pode modificar a forma por meio de atributos ou subelementos anexados.</span><span class="sxs-lookup"><span data-stu-id="70912-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="70912-136">Por exemplo, para alterar a cor de uma forma, atribua um valor de cor ao **atributo FillColor.**</span><span class="sxs-lookup"><span data-stu-id="70912-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="70912-137">Vários dos atributos de uma forma também são [subelementos](/windows) e têm seus próprios atributos, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="70912-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="70912-138">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="70912-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="70912-139">Extrusão</span><span class="sxs-lookup"><span data-stu-id="70912-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="70912-140">Preencher</span><span class="sxs-lookup"><span data-stu-id="70912-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="70912-141">Grupo</span><span class="sxs-lookup"><span data-stu-id="70912-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="70912-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="70912-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="70912-143">Caminho</span><span class="sxs-lookup"><span data-stu-id="70912-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="70912-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="70912-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="70912-145">Inclinar</span><span class="sxs-lookup"><span data-stu-id="70912-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="70912-146">Curso</span><span class="sxs-lookup"><span data-stu-id="70912-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="70912-147">Textpath</span><span class="sxs-lookup"><span data-stu-id="70912-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="70912-148">O VML OM usa vários [tipos de dados](/windows) para definir parâmetros.</span><span class="sxs-lookup"><span data-stu-id="70912-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="70912-149">Os tipos de dados prefixados com "Vg" são enumerações e aqueles prefixados com "IVg" são objetos.</span><span class="sxs-lookup"><span data-stu-id="70912-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="70912-150">Clique aqui para ver uma lista.</span><span class="sxs-lookup"><span data-stu-id="70912-150">Click here for a list.</span></span> <span data-ttu-id="70912-151">Tipos de dados secundários são listados com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="70912-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="70912-152">Exemplo</span><span class="sxs-lookup"><span data-stu-id="70912-152">Example</span></span>

<span data-ttu-id="70912-153">O código VBScript a seguir mostra como criar uma forma simples:</span><span class="sxs-lookup"><span data-stu-id="70912-153">The following VBScript code shows how to create a simple shape:</span></span>


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



<span data-ttu-id="70912-154">No exemplo acima, uma forma é criada usando o método Modelo de Objeto do Documento **CreateElement**.</span><span class="sxs-lookup"><span data-stu-id="70912-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="70912-155">A forma é uma forma de Rect predefinida de VML.</span><span class="sxs-lookup"><span data-stu-id="70912-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="70912-156">Embora o objeto exista, ele não pode fazer parte do documento até que seja anexado ao documento.</span><span class="sxs-lookup"><span data-stu-id="70912-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="70912-157">Usando o **método AppendChild,** o Rect se tornou um filho de um **elemento DIV** chamado MyDiv.</span><span class="sxs-lookup"><span data-stu-id="70912-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="70912-158">Alguns atributos de estilo mínimos (**Position**, **Width**, **Height**, **Top**, **Left**) são definidos para dar à forma um tamanho específico.</span><span class="sxs-lookup"><span data-stu-id="70912-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="70912-159">Por fim, uma cor é atribuída com o **atributo FillColor.**</span><span class="sxs-lookup"><span data-stu-id="70912-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="70912-160">Observe que qualquer linguagem de script ou qualquer linguagem que possa trabalhar com interfaces Modelo de Objeto do Documento pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="70912-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="70912-161">Configurando o VML</span><span class="sxs-lookup"><span data-stu-id="70912-161">Setting up VML</span></span>

<span data-ttu-id="70912-162">Uma implementação do VML é por meio do Microsoft Internet Explorer 5.0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="70912-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="70912-163">Para configurar o objeto de renderização corretamente em uma página da Web, as seguintes adições devem ser feitas:</span><span class="sxs-lookup"><span data-stu-id="70912-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="70912-164">O esquema deve ser definido na inicial</span><span class="sxs-lookup"><span data-stu-id="70912-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="70912-165">tag da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="70912-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="70912-166">O comportamento de renderização deve fazer parte do estilo do documento:</span><span class="sxs-lookup"><span data-stu-id="70912-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="70912-167">A seguir, é mostrado um exemplo de página da Web HTML configurada corretamente para o VML mostrando a criação dinâmica de uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


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



<span data-ttu-id="70912-168">Observe que, em versões beta, uma marca de objeto ActiveX e um estilo de comportamento diferente foram necessários.</span><span class="sxs-lookup"><span data-stu-id="70912-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="70912-169">Referência de OM do VML</span><span class="sxs-lookup"><span data-stu-id="70912-169">VML OM Reference</span></span>

<span data-ttu-id="70912-170">Essa referência define o elemento [Shape,](#shape-element) os [](/windows) [subelementos](/windows)e os tipos de dados usados pelo modelo de objeto do VML.</span><span class="sxs-lookup"><span data-stu-id="70912-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="70912-171">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="70912-171">Shape element</span></span>

<span data-ttu-id="70912-172">Formas são os blocos de construção de imagens gráficas definidos linguagem VML (VML).</span><span class="sxs-lookup"><span data-stu-id="70912-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="70912-173">A forma é o elemento de nível superior e vários subelementos ajudam a definir a natureza de cada forma.</span><span class="sxs-lookup"><span data-stu-id="70912-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="70912-174">O VML fornece formas predefinida:</span><span class="sxs-lookup"><span data-stu-id="70912-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="70912-175">**Atributos de forma**</span><span class="sxs-lookup"><span data-stu-id="70912-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="70912-176">**Arco**</span><span class="sxs-lookup"><span data-stu-id="70912-176">**Arc**</span></span>
-   <span data-ttu-id="70912-177">**Curva**</span><span class="sxs-lookup"><span data-stu-id="70912-177">**Curve**</span></span>
-   <span data-ttu-id="70912-178">**Linha**</span><span class="sxs-lookup"><span data-stu-id="70912-178">**Line**</span></span>
-   <span data-ttu-id="70912-179">**Polilinha**</span><span class="sxs-lookup"><span data-stu-id="70912-179">**PolyLine**</span></span>
-   <span data-ttu-id="70912-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="70912-180">**Rect**</span></span>
-   <span data-ttu-id="70912-181">**Roundrect**</span><span class="sxs-lookup"><span data-stu-id="70912-181">**RoundRect**</span></span>



|   <span data-ttu-id="70912-182">Subelemento</span><span class="sxs-lookup"><span data-stu-id="70912-182">Subelement</span></span>           |    <span data-ttu-id="70912-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-183">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-184">Adj</span><span class="sxs-lookup"><span data-stu-id="70912-184">Adj</span></span>          | <span data-ttu-id="70912-185">[IVgAdjustments.](msdn-online-vml-ivgadjustments-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="70912-186">Uma lista delimitada por vírgulas de números que são os parâmetros para as fórmulas de guia que definem o caminho da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-186">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="70912-187">Os valores podem ser omitidos para permitir o uso de padrões.</span><span class="sxs-lookup"><span data-stu-id="70912-187">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="70912-188">Pode haver até 8 valores de ajuste.</span><span class="sxs-lookup"><span data-stu-id="70912-188">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="70912-189">Alt</span><span class="sxs-lookup"><span data-stu-id="70912-189">Alt</span></span>          | <span data-ttu-id="70912-190">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70912-190">String.</span></span> <span data-ttu-id="70912-191">Texto alternativo associado à forma.</span><span class="sxs-lookup"><span data-stu-id="70912-191">Alternative text associated with shape.</span></span> <span data-ttu-id="70912-192">Usado para navegação não gráfica.</span><span class="sxs-lookup"><span data-stu-id="70912-192">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="70912-193">Botão</span><span class="sxs-lookup"><span data-stu-id="70912-193">Button</span></span>       | <span data-ttu-id="70912-194">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-194">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-195">Exibe o comportamento do botão ao clicar.</span><span class="sxs-lookup"><span data-stu-id="70912-195">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="70912-196">BWMode</span><span class="sxs-lookup"><span data-stu-id="70912-196">BWMode</span></span>       | <span data-ttu-id="70912-197">[VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md)</span><span class="sxs-lookup"><span data-stu-id="70912-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="70912-198">Determina como a forma será renderizar na exibição em preto e branco em aplicativos ou quando impressa em impressoras em preto e branco.</span><span class="sxs-lookup"><span data-stu-id="70912-198">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="70912-199">Os valores incluem: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="70912-199">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="70912-200">Padrão: **Automático.**</span><span class="sxs-lookup"><span data-stu-id="70912-200">Default: **Auto**.</span></span> |
| <span data-ttu-id="70912-201">BWNormal</span><span class="sxs-lookup"><span data-stu-id="70912-201">BWNormal</span></span>     | <span data-ttu-id="70912-202">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="70912-202">VgBlackWhiteMode.</span></span> <span data-ttu-id="70912-203">Quando BWMode é Auto, essa propriedade é consultada para saber como renderizar a forma em preto e branco normais.</span><span class="sxs-lookup"><span data-stu-id="70912-203">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="70912-204">Os valores incluem: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="70912-204">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="70912-205">Padrão: **Automático.**</span><span class="sxs-lookup"><span data-stu-id="70912-205">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="70912-206">BWPure</span><span class="sxs-lookup"><span data-stu-id="70912-206">BWPure</span></span>       | <span data-ttu-id="70912-207">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="70912-207">VgBlackWhiteMode.</span></span> <span data-ttu-id="70912-208">Quando BWMode é Auto, essa propriedade é consultada para saber como renderizar a forma em B/W puro.</span><span class="sxs-lookup"><span data-stu-id="70912-208">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="70912-209">Os valores incluem: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="70912-209">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="70912-210">Padrão: **Automático.**</span><span class="sxs-lookup"><span data-stu-id="70912-210">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="70912-211">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="70912-211">ChildShapes</span></span>  | <span data-ttu-id="70912-212">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="70912-212">IVgGroupShapes.</span></span> <span data-ttu-id="70912-213">Uma coleção de outras formas neste grupo.</span><span class="sxs-lookup"><span data-stu-id="70912-213">A collection of other shapes in this group.</span></span> <span data-ttu-id="70912-214">Essa coleção dá suporte aos métodos Length e Item padrão.</span><span class="sxs-lookup"><span data-stu-id="70912-214">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="70912-215">Chromakey</span><span class="sxs-lookup"><span data-stu-id="70912-215">Chromakey</span></span>    | <span data-ttu-id="70912-216">[IVgColor.](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70912-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="70912-217">Um valor de cor que será transparente e mostrará qualquer coisa por trás da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-217">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="70912-218">Control1</span><span class="sxs-lookup"><span data-stu-id="70912-218">Control1</span></span>     | <span data-ttu-id="70912-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="70912-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-220">Ponto de controle para curva.</span><span class="sxs-lookup"><span data-stu-id="70912-220">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="70912-221">Control2</span><span class="sxs-lookup"><span data-stu-id="70912-221">Control2</span></span>     | <span data-ttu-id="70912-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="70912-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-223">Ponto de controle para curva.</span><span class="sxs-lookup"><span data-stu-id="70912-223">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="70912-224">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="70912-224">CoordOrigin</span></span>  | <span data-ttu-id="70912-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) As coordenadas no canto superior esquerdo do retângulo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70912-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="70912-226">Intervalo de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="70912-226">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="70912-227">CoordSize</span><span class="sxs-lookup"><span data-stu-id="70912-227">CoordSize</span></span>    | <span data-ttu-id="70912-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="70912-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-229">A largura e a altura do espaço de coordenadas dentro do retângulo de referência dessa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-229">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="70912-230">Se não for especificado, será o mesmo que a largura e a altura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="70912-230">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="70912-231">Intervalo de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="70912-231">Range from 0 to infinity.</span></span> <span data-ttu-id="70912-232">Padrão: "1000,1000".</span><span class="sxs-lookup"><span data-stu-id="70912-232">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="70912-233">EndAngle</span><span class="sxs-lookup"><span data-stu-id="70912-233">EndAngle</span></span>     | <span data-ttu-id="70912-234">[VgAngleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="70912-235">Ângulo final da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-235">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="70912-236">Extrusão</span><span class="sxs-lookup"><span data-stu-id="70912-236">Extrusion</span></span>    | <span data-ttu-id="70912-237">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="70912-237">IVgExtrusion.</span></span> <span data-ttu-id="70912-238">Especifica o valor do objeto Deiaion para essa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-238">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="70912-239">Consulte o [elemento Deiaion](msdn-online-vml-extrusion-element.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="70912-239">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="70912-240">Preencher</span><span class="sxs-lookup"><span data-stu-id="70912-240">Fill</span></span>         | <span data-ttu-id="70912-241">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="70912-241">VgFillFormat.</span></span> <span data-ttu-id="70912-242">Especifica o valor de preenchimento para essa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-242">Specifies the fill value for this shape.</span></span> <span data-ttu-id="70912-243">Consulte o [elemento Fill](msdn-online-vml-fill-element.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="70912-243">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="70912-244">Fillcolor</span><span class="sxs-lookup"><span data-stu-id="70912-244">FillColor</span></span>    | <span data-ttu-id="70912-245">[IVgColor.](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70912-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="70912-246">A cor primária do pincel a ser usada para preencher o caminho dessa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-246">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="70912-247">Preenchido</span><span class="sxs-lookup"><span data-stu-id="70912-247">Filled</span></span>       | <span data-ttu-id="70912-248">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-248">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-249">Se True, o caminho que define a forma será preenchido.</span><span class="sxs-lookup"><span data-stu-id="70912-249">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="70912-250">Por padrão, ele será preenchido usando uma cor sólida, a menos que haja um subelemento Fill que especifique propriedades de preenchimento mais complexas.</span><span class="sxs-lookup"><span data-stu-id="70912-250">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="70912-251">Se False, o preenchimento será transparente.</span><span class="sxs-lookup"><span data-stu-id="70912-251">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="70912-252">Inverter</span><span class="sxs-lookup"><span data-stu-id="70912-252">Flip</span></span>         | <span data-ttu-id="70912-253">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="70912-253">VgFlipOrientation.</span></span> <span data-ttu-id="70912-254">Os valores são: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="70912-254">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="70912-255">ForceDash</span><span class="sxs-lookup"><span data-stu-id="70912-255">ForceDash</span></span>    | <span data-ttu-id="70912-256">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-256">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-257">Indicação de que um contorno tracejado deve ser renderizado quando não há nenhuma linha e nenhum preenchimento para uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-257">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="70912-258">Esse comportamento geralmente é útil para tornar as formas invisíveis visíveis na edição de aplicativos para que possam ser selecionadas e operadas, como em um mapa de imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-258">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="70912-259">Fórmulas</span><span class="sxs-lookup"><span data-stu-id="70912-259">Formulas</span></span>     | <span data-ttu-id="70912-260">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="70912-260">IVgFormulas.</span></span> <span data-ttu-id="70912-261">Uma matriz de fórmulas que define uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-261">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="70912-262">De</span><span class="sxs-lookup"><span data-stu-id="70912-262">From</span></span>         | <span data-ttu-id="70912-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="70912-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-264">Ponto de partida da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-264">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="70912-265">Href</span><span class="sxs-lookup"><span data-stu-id="70912-265">HRef</span></span>         | <span data-ttu-id="70912-266">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-266">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-267">A URL a ser clicada se essa forma for clicada.</span><span class="sxs-lookup"><span data-stu-id="70912-267">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="70912-268">ImageData</span><span class="sxs-lookup"><span data-stu-id="70912-268">ImageData</span></span>    | <span data-ttu-id="70912-269">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="70912-269">IVgImageData.</span></span> <span data-ttu-id="70912-270">Informações de imagem se a forma for uma imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-270">Image information if the shape is a picture.</span></span> <span data-ttu-id="70912-271">Consulte o elemento ImageData para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="70912-271">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="70912-272">OnEd</span><span class="sxs-lookup"><span data-stu-id="70912-272">OnEd</span></span>         | <span data-ttu-id="70912-273">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-273">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-274">Oculta todos os alças, exceto a parte superior esquerda e inferior direita, como nos alças de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="70912-274">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="70912-275">Opacidade</span><span class="sxs-lookup"><span data-stu-id="70912-275">Opacity</span></span>      | <span data-ttu-id="70912-276">[VgAção .](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="70912-277">A opacidade de toda a forma.</span><span class="sxs-lookup"><span data-stu-id="70912-277">The opacity of the entire shape.</span></span> <span data-ttu-id="70912-278">Um número entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="70912-278">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="70912-279">Caminho</span><span class="sxs-lookup"><span data-stu-id="70912-279">Path</span></span>         | <span data-ttu-id="70912-280">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="70912-280">IVgPath.</span></span> <span data-ttu-id="70912-281">Uma cadeia de caracteres que contém os comandos que definem o caminho.</span><span class="sxs-lookup"><span data-stu-id="70912-281">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="70912-282">Pontos</span><span class="sxs-lookup"><span data-stu-id="70912-282">Points</span></span>       | <span data-ttu-id="70912-283">[IVgPoints.](msdn-online-vml-ivgpoints-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="70912-284">Uma coleção de pontos que definem uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-284">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="70912-285">Impressão</span><span class="sxs-lookup"><span data-stu-id="70912-285">Print</span></span>        | <span data-ttu-id="70912-286">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-286">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-287">Se True, essa forma deve ser impressa.</span><span class="sxs-lookup"><span data-stu-id="70912-287">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="70912-288">Rotação</span><span class="sxs-lookup"><span data-stu-id="70912-288">Rotation</span></span>     | <span data-ttu-id="70912-289">[VgAngleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="70912-290">Define a rotação da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-290">Sets rotation of shape.</span></span> <span data-ttu-id="70912-291">O valor é propagado para o estilo de forma.</span><span class="sxs-lookup"><span data-stu-id="70912-291">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="70912-292">Escala</span><span class="sxs-lookup"><span data-stu-id="70912-292">Scale</span></span>        | <span data-ttu-id="70912-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="70912-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-294">Escala de forma.</span><span class="sxs-lookup"><span data-stu-id="70912-294">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="70912-295">Shadow</span><span class="sxs-lookup"><span data-stu-id="70912-295">Shadow</span></span>       | <span data-ttu-id="70912-296">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="70912-296">IVgShadow.</span></span> <span data-ttu-id="70912-297">Especifica a sombra dessa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-297">Specifies the shadow for this shape.</span></span> <span data-ttu-id="70912-298">Consulte o [elemento Shadow](msdn-online-vml-shadow-element.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="70912-298">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="70912-299">Spt</span><span class="sxs-lookup"><span data-stu-id="70912-299">Spt</span></span>          | <span data-ttu-id="70912-300">Reservado.</span><span class="sxs-lookup"><span data-stu-id="70912-300">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="70912-301">Startangle</span><span class="sxs-lookup"><span data-stu-id="70912-301">StartAngle</span></span>   | <span data-ttu-id="70912-302">[VgAngleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="70912-303">Ângulo inicial da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-303">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="70912-304">Traço</span><span class="sxs-lookup"><span data-stu-id="70912-304">Stroke</span></span>       | <span data-ttu-id="70912-305">VgRogkeFormat.</span><span class="sxs-lookup"><span data-stu-id="70912-305">VgStrokeFormat.</span></span> <span data-ttu-id="70912-306">Consulte Elemento Stroke para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="70912-306">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="70912-307">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="70912-307">StrokeColor</span></span>  | <span data-ttu-id="70912-308">[IVgColor.](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70912-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="70912-309">A cor primária do pincel a ser usada para traço do caminho dessa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-309">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="70912-310">Acariciou</span><span class="sxs-lookup"><span data-stu-id="70912-310">Stroked</span></span>      | <span data-ttu-id="70912-311">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-311">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-312">Se True, o caminho que define a forma será traço.</span><span class="sxs-lookup"><span data-stu-id="70912-312">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="70912-313">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="70912-313">StrokeWeight</span></span> | <span data-ttu-id="70912-314">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="70912-314">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="70912-315">A largura do pincel a ser usada para traço do caminho.</span><span class="sxs-lookup"><span data-stu-id="70912-315">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="70912-316">Varia entre 0 e 1584.</span><span class="sxs-lookup"><span data-stu-id="70912-316">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="70912-317">Textpath</span><span class="sxs-lookup"><span data-stu-id="70912-317">TextPath</span></span>     | <span data-ttu-id="70912-318">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="70912-318">IVgTextPath.</span></span> <span data-ttu-id="70912-319">Especifica o objeto TextPath da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-319">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="70912-320">Consulte o [elemento TextPath](msdn-online-vml-textpath-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="70912-320">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="70912-321">Para</span><span class="sxs-lookup"><span data-stu-id="70912-321">To</span></span>           | <span data-ttu-id="70912-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="70912-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-323">Ponto de extremidade da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-323">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="70912-324">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-324">Type</span></span>         | <span data-ttu-id="70912-325">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70912-325">String.</span></span> <span data-ttu-id="70912-326">Tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="70912-326">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="70912-327">Subelementos do elemento Shape</span><span class="sxs-lookup"><span data-stu-id="70912-327">Subelements of the Shape Element</span></span>

<span data-ttu-id="70912-328">Os subelementos a seguir fazem parte do modelo de objeto VML.</span><span class="sxs-lookup"><span data-stu-id="70912-328">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="70912-329">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="70912-329">Background</span></span>](#background-element)
-   [<span data-ttu-id="70912-330">Extrusão</span><span class="sxs-lookup"><span data-stu-id="70912-330">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="70912-331">Preencher</span><span class="sxs-lookup"><span data-stu-id="70912-331">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="70912-332">Grupo</span><span class="sxs-lookup"><span data-stu-id="70912-332">Group</span></span>](#group-element)
-   [<span data-ttu-id="70912-333">Imagedata</span><span class="sxs-lookup"><span data-stu-id="70912-333">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="70912-334">Caminho</span><span class="sxs-lookup"><span data-stu-id="70912-334">Path</span></span>](#path-element)
-   [<span data-ttu-id="70912-335">Shadow</span><span class="sxs-lookup"><span data-stu-id="70912-335">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="70912-336">Inclinar</span><span class="sxs-lookup"><span data-stu-id="70912-336">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="70912-337">Curso</span><span class="sxs-lookup"><span data-stu-id="70912-337">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="70912-338">Textpath</span><span class="sxs-lookup"><span data-stu-id="70912-338">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="70912-339">Elemento Background</span><span class="sxs-lookup"><span data-stu-id="70912-339">Background element</span></span>

<span data-ttu-id="70912-340">Descreve o preenchimento da parte de fundo de uma página usando preenchimentos de VML.</span><span class="sxs-lookup"><span data-stu-id="70912-340">Describes the fill of the background of a page using VML fills.</span></span>


|   <span data-ttu-id="70912-341">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-341">Attribute</span></span>        |   <span data-ttu-id="70912-342">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-342">Description</span></span>                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-343">BWMode</span><span class="sxs-lookup"><span data-stu-id="70912-343">BWMode</span></span>    | <span data-ttu-id="70912-344">[VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md)</span><span class="sxs-lookup"><span data-stu-id="70912-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="70912-345">Determina como a forma será renderizar na exibição em preto e branco em aplicativos ou quando impressa.</span><span class="sxs-lookup"><span data-stu-id="70912-345">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="70912-346">BWNormal</span><span class="sxs-lookup"><span data-stu-id="70912-346">BWNormal</span></span>  | <span data-ttu-id="70912-347">[VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md)</span><span class="sxs-lookup"><span data-stu-id="70912-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="70912-348">Quando BWMode é Auto, essa propriedade é consultada para saber como renderizar a forma em preto e branco normais.</span><span class="sxs-lookup"><span data-stu-id="70912-348">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="70912-349">BWPure</span><span class="sxs-lookup"><span data-stu-id="70912-349">BWPure</span></span>    | <span data-ttu-id="70912-350">[VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md)</span><span class="sxs-lookup"><span data-stu-id="70912-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="70912-351">Quando BWMode é Auto, essa propriedade é consultada para saber como renderizar a forma em preto e branco puros.</span><span class="sxs-lookup"><span data-stu-id="70912-351">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="70912-352">Preencher</span><span class="sxs-lookup"><span data-stu-id="70912-352">Fill</span></span>      | <span data-ttu-id="70912-353">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="70912-353">VgFillFormat.</span></span> <span data-ttu-id="70912-354">Especifica o preenchimento dessa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-354">Specifies the fill for this shape.</span></span> <span data-ttu-id="70912-355">Consulte [Elemento Fill](msdn-online-vml-fill-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="70912-355">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="70912-356">Fillcolor</span><span class="sxs-lookup"><span data-stu-id="70912-356">FillColor</span></span> | <span data-ttu-id="70912-357">[IVgColor.](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70912-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="70912-358">A cor primária do pincel a ser usada para preencher o caminho dessa forma.</span><span class="sxs-lookup"><span data-stu-id="70912-358">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="70912-359">Duplicar do valor Color no elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="70912-359">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="70912-360">O padrão é branco.</span><span class="sxs-lookup"><span data-stu-id="70912-360">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="70912-361">Elemento Deiaion</span><span class="sxs-lookup"><span data-stu-id="70912-361">Extrusion element</span></span>

<span data-ttu-id="70912-362">Descreve uma shape em 3D.</span><span class="sxs-lookup"><span data-stu-id="70912-362">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="70912-363">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="70912-363">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-364">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="70912-364">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="70912-365"><a href="msdn-online-vml-vgtristate.md">VgTriState.</a></span><span class="sxs-lookup"><span data-stu-id="70912-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-366">Se True, o centro de rotação do grupo de objetos 3D (na verdade, há apenas um objeto no grupo) será determinado automaticamente como o centro do grupo; caso contrário, será determinado pelos parâmetros RotationCenter, que são uma fração da forma com 0,0,0 sendo o centro.</span><span class="sxs-lookup"><span data-stu-id="70912-366">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-367">BackDepth</span><span class="sxs-lookup"><span data-stu-id="70912-367">BackDepth</span></span></td>
<td><span data-ttu-id="70912-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength.</strong></a></span><span class="sxs-lookup"><span data-stu-id="70912-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="70912-369">Quantidade deion para trás.</span><span class="sxs-lookup"><span data-stu-id="70912-369">Amount of backward extrusion.</span></span> <span data-ttu-id="70912-370">Varia de 0 a 32767.</span><span class="sxs-lookup"><span data-stu-id="70912-370">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-371">Brightness</span><span class="sxs-lookup"><span data-stu-id="70912-371">Brightness</span></span></td>
<td><span data-ttu-id="70912-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber.</a></span><span class="sxs-lookup"><span data-stu-id="70912-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="70912-373">Brilho geral da cena.</span><span class="sxs-lookup"><span data-stu-id="70912-373">Overall brightness of the scene.</span></span> <span data-ttu-id="70912-374">O padrão &quot; é 20.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-374">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-375">Color</span><span class="sxs-lookup"><span data-stu-id="70912-375">Color</span></span></td>
<td><span data-ttu-id="70912-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor.</a></span><span class="sxs-lookup"><span data-stu-id="70912-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="70912-377">A cor da paleta.</span><span class="sxs-lookup"><span data-stu-id="70912-377">The color of the extrusion.</span></span> <span data-ttu-id="70912-378">Usado somente se ColorMode for Personalizado.</span><span class="sxs-lookup"><span data-stu-id="70912-378">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="70912-379">Caso contrário, Automaticamente define a cor do efeito de paleta como a mesma que FillColor.</span><span class="sxs-lookup"><span data-stu-id="70912-379">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-380">Colormode</span><span class="sxs-lookup"><span data-stu-id="70912-380">ColorMode</span></span></td>
<td><span data-ttu-id="70912-381">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="70912-381">Vg3DColorMode.</span></span> <span data-ttu-id="70912-382">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-382">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-383">Auto (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-383">Auto (default)</span></span></li>
<li><span data-ttu-id="70912-384">Personalizado</span><span class="sxs-lookup"><span data-stu-id="70912-384">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-385">Difusidade</span><span class="sxs-lookup"><span data-stu-id="70912-385">Diffusity</span></span></td>
<td><span data-ttu-id="70912-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber.</a></span><span class="sxs-lookup"><span data-stu-id="70912-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="70912-387">A taxa de incidentes para luz refletida de forma difusa.</span><span class="sxs-lookup"><span data-stu-id="70912-387">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="70912-388">Valores menores que 1,0 são normais, mas valores maiores que um podem gerar efeitos interessantes.</span><span class="sxs-lookup"><span data-stu-id="70912-388">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-389">Edge</span><span class="sxs-lookup"><span data-stu-id="70912-389">Edge</span></span></td>
<td><span data-ttu-id="70912-390"><a href="msdn-online-vml-vglength.md">VgLength.</a></span><span class="sxs-lookup"><span data-stu-id="70912-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="70912-391">Define o tamanho de uma borda arredondada arredondada simulada.</span><span class="sxs-lookup"><span data-stu-id="70912-391">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="70912-392">Varia de 0 a 32767 em pontos flutuantes.</span><span class="sxs-lookup"><span data-stu-id="70912-392">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="70912-393">O padrão é &quot; &quot; 1pt.</span><span class="sxs-lookup"><span data-stu-id="70912-393">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-394">Faceta</span><span class="sxs-lookup"><span data-stu-id="70912-394">Facet</span></span></td>
<td><span data-ttu-id="70912-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber.</a></span><span class="sxs-lookup"><span data-stu-id="70912-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="70912-396">Define a faceta da cena.</span><span class="sxs-lookup"><span data-stu-id="70912-396">Sets the facet of the scene.</span></span> <span data-ttu-id="70912-397">O padrão &quot; é 30.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-397">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-398">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="70912-398">ForeDepth</span></span></td>
<td><span data-ttu-id="70912-399"><a href="msdn-online-vml-vglength.md">VgLength.</a></span><span class="sxs-lookup"><span data-stu-id="70912-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="70912-400">Quantidade deion de avanço.</span><span class="sxs-lookup"><span data-stu-id="70912-400">Amount of forward extrusion.</span></span> <span data-ttu-id="70912-401">Varia de 0 a 32767.</span><span class="sxs-lookup"><span data-stu-id="70912-401">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-402">LightFace</span><span class="sxs-lookup"><span data-stu-id="70912-402">LightFace</span></span></td>
<td><span data-ttu-id="70912-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-404">Determimes se a face frontal do objeto responderá às alterações na iluminação 3D, por exemplo, quando um objeto for girado.</span><span class="sxs-lookup"><span data-stu-id="70912-404">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-405">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="70912-405">LightHarsh</span></span></td>
<td><span data-ttu-id="70912-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-407">Iluminação de inverso para a fonte de luz primária.</span><span class="sxs-lookup"><span data-stu-id="70912-407">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="70912-408">O padrão é Falso.</span><span class="sxs-lookup"><span data-stu-id="70912-408">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-409">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="70912-409">LightHarsh2</span></span></td>
<td><span data-ttu-id="70912-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-411">Iluminação de durabilidade para a fonte de luz secundária.</span><span class="sxs-lookup"><span data-stu-id="70912-411">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="70912-412">O padrão é Falso.</span><span class="sxs-lookup"><span data-stu-id="70912-412">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-413">LightLevel</span><span class="sxs-lookup"><span data-stu-id="70912-413">LightLevel</span></span></td>
<td><span data-ttu-id="70912-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="70912-415">Intensidade da fonte de luz primária.</span><span class="sxs-lookup"><span data-stu-id="70912-415">Intensity of the primary light source.</span></span> <span data-ttu-id="70912-416">O padrão é &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-416">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-417">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="70912-417">LightLevel2</span></span></td>
<td><span data-ttu-id="70912-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="70912-419">Intensidade da fonte de luz secundária.</span><span class="sxs-lookup"><span data-stu-id="70912-419">Intensity of the secondary light source.</span></span> <span data-ttu-id="70912-420">O padrão é &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-420">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-421">LightPosition</span><span class="sxs-lookup"><span data-stu-id="70912-421">LightPosition</span></span></td>
<td><span data-ttu-id="70912-422">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="70912-422">Vector3D.</span></span> <span data-ttu-id="70912-423">Posição da fonte de luz primária.</span><span class="sxs-lookup"><span data-stu-id="70912-423">Position of the primary light source.</span></span> <span data-ttu-id="70912-424">O padrão é &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-424">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-425">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="70912-425">LightPosition2</span></span></td>
<td><span data-ttu-id="70912-426">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="70912-426">Vector3D.</span></span> <span data-ttu-id="70912-427">Posição da fonte de luz secundária.</span><span class="sxs-lookup"><span data-stu-id="70912-427">Position of the secondary light source.</span></span> <span data-ttu-id="70912-428">O padrão é &quot; -50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-428">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-429">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="70912-429">LockRotationCenter</span></span></td>
<td><span data-ttu-id="70912-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-431">&quot;Lockrotationcenter &quot; significa que a rotação do grupo é definida para ser por ângulo de rotação [1] graus sobre o eixo y na página seguido por ângulo de rotação [0] graus sobre o eixo x.</span><span class="sxs-lookup"><span data-stu-id="70912-431">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="70912-432">Quando LockRotationCenter é false, a rotação é definida de acordo com os graus de ângulo de orientação sobre o vetor definido por orientação.</span><span class="sxs-lookup"><span data-stu-id="70912-432">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="70912-433">Portanto, por exemplo, lockrotationcenter = false orientationangle = 45 Orientation = (0, 1, 0) é equivalente a lockrotationcenter = true RotationAngle = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="70912-433">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-434">Metal</span><span class="sxs-lookup"><span data-stu-id="70912-434">Metal</span></span></td>
<td><span data-ttu-id="70912-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-436">Faz com que a luz refletida de forma especulada seja a cor do material em vez da cor da fonte de luz, tornando o objeto aparentemente mais metálico.</span><span class="sxs-lookup"><span data-stu-id="70912-436">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-437">Ativado</span><span class="sxs-lookup"><span data-stu-id="70912-437">On</span></span></td>
<td><span data-ttu-id="70912-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-439">Ativa e desativa a exibição do efeito de extrusão.</span><span class="sxs-lookup"><span data-stu-id="70912-439">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-440">Orientation</span><span class="sxs-lookup"><span data-stu-id="70912-440">Orientation</span></span></td>
<td><span data-ttu-id="70912-441">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="70912-441">Vector3D.</span></span> <span data-ttu-id="70912-442">Orientação da câmera.</span><span class="sxs-lookup"><span data-stu-id="70912-442">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-443">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="70912-443">OrientationAngle</span></span></td>
<td><span data-ttu-id="70912-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="70912-445">Ângulo entre a orientação da câmera e o plano XY.</span><span class="sxs-lookup"><span data-stu-id="70912-445">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-446">Aérea</span><span class="sxs-lookup"><span data-stu-id="70912-446">Plane</span></span></td>
<td><span data-ttu-id="70912-447">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="70912-447">Vg3DExtrudePlane.</span></span> <span data-ttu-id="70912-448">Permite a extrusão dos planos ortogonal ao plano de tela.</span><span class="sxs-lookup"><span data-stu-id="70912-448">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="70912-449">Requer que ForeDepth e a profundidade de fundo sejam especificadas em unidades de desenho em vez de emus.</span><span class="sxs-lookup"><span data-stu-id="70912-449">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="70912-450">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-450">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-451">XY</span><span class="sxs-lookup"><span data-stu-id="70912-451">XY</span></span></li>
<li><span data-ttu-id="70912-452">ZX</span><span class="sxs-lookup"><span data-stu-id="70912-452">ZX</span></span></li>
<li><span data-ttu-id="70912-453">YZ</span><span class="sxs-lookup"><span data-stu-id="70912-453">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-454">Renderizar</span><span class="sxs-lookup"><span data-stu-id="70912-454">Render</span></span></td>
<td><span data-ttu-id="70912-455">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="70912-455">Vg3DRenderMode.</span></span> <span data-ttu-id="70912-456">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-456">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-457">Solid (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-457">Solid (default)</span></span></li>
<li><span data-ttu-id="70912-458">WireFrame</span><span class="sxs-lookup"><span data-stu-id="70912-458">WireFrame</span></span></li>
<li><span data-ttu-id="70912-459">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="70912-459">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-460">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="70912-460">RotationAngle</span></span></td>
<td><span data-ttu-id="70912-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-462">AngleX, incline ou AngleZ é controlado pelo atributo ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="70912-462">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-463">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="70912-463">RotationCenter</span></span></td>
<td><span data-ttu-id="70912-464">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="70912-464">Vector3D.</span></span> <span data-ttu-id="70912-465">Centro de rotação.</span><span class="sxs-lookup"><span data-stu-id="70912-465">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-466">Luminosidade</span><span class="sxs-lookup"><span data-stu-id="70912-466">Shininess</span></span></td>
<td><span data-ttu-id="70912-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="70912-468">Determina o quão concentrado ou distribuído a reflexão especular é.</span><span class="sxs-lookup"><span data-stu-id="70912-468">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="70912-469">Um valor alto seria de 8 a 10 e aproximaria um espelho, e um valor baixo seria de 2 a 3 e seria um roupas sequined aproximado.</span><span class="sxs-lookup"><span data-stu-id="70912-469">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="70912-470">São recomendados valores de 3 a 7.</span><span class="sxs-lookup"><span data-stu-id="70912-470">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="70912-471">Valores altos refletirão as fontes de luz do Pinpoint.</span><span class="sxs-lookup"><span data-stu-id="70912-471">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-472">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="70912-472">SkewAmt</span></span></td>
<td><span data-ttu-id="70912-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="70912-474">Se Type for Parallel, o atributo determinará a quantidade de distorção.</span><span class="sxs-lookup"><span data-stu-id="70912-474">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="70912-475">Varia de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="70912-475">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-476">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="70912-476">SkewAngle</span></span></td>
<td><span data-ttu-id="70912-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="70912-478">Se Type for Parallel, o atributo determinará o grau de distorção.</span><span class="sxs-lookup"><span data-stu-id="70912-478">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="70912-479">O padrão é &quot; -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-479">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-480">Refletir</span><span class="sxs-lookup"><span data-stu-id="70912-480">Specularity</span></span></td>
<td><span data-ttu-id="70912-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="70912-482">A taxa de incidentes para a luz refletida especulada.</span><span class="sxs-lookup"><span data-stu-id="70912-482">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="70912-483">Valores menores que 1,0 são normais, mas valores maiores que um podem gerar efeitos interessantes.</span><span class="sxs-lookup"><span data-stu-id="70912-483">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-484">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-484">Type</span></span></td>
<td><span data-ttu-id="70912-485">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="70912-485">VgExtrusionType.</span></span> <span data-ttu-id="70912-486">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-486">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-487">Paralelo (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-487">Parallel (default)</span></span></li>
<li><span data-ttu-id="70912-488">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="70912-488">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-489">Ponto</span><span class="sxs-lookup"><span data-stu-id="70912-489">Viewpoint</span></span></td>
<td><span data-ttu-id="70912-490">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="70912-490">Vector3D.</span></span> <span data-ttu-id="70912-491">O ponto em que a cena está sendo visualizada.</span><span class="sxs-lookup"><span data-stu-id="70912-491">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-492">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="70912-492">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="70912-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-494">Pode ter valores de 0,5 a 0,5 para posicionar a origem do ponto de vista dentro da caixa delimitadora de forma.</span><span class="sxs-lookup"><span data-stu-id="70912-494">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="70912-495">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="70912-495">Fill element</span></span>

<span data-ttu-id="70912-496">Descreve como um caminho deve ser preenchido para preenchimentos mais complexos do que uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="70912-496">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="70912-497">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="70912-497">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-498">AlignShape</span><span class="sxs-lookup"><span data-stu-id="70912-498">AlignShape</span></span></td>
<td><span data-ttu-id="70912-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-500">Alinhe a imagem com a forma.</span><span class="sxs-lookup"><span data-stu-id="70912-500">Align the image with the shape.</span></span> <span data-ttu-id="70912-501">Se for false, alinhar a imagem com a janela.</span><span class="sxs-lookup"><span data-stu-id="70912-501">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-502">Ângulo</span><span class="sxs-lookup"><span data-stu-id="70912-502">Angle</span></span></td>
<td><span data-ttu-id="70912-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="70912-504">O ângulo ao longo do qual o gradiente vai.</span><span class="sxs-lookup"><span data-stu-id="70912-504">The angle along which the gradient goes.</span></span> <span data-ttu-id="70912-505">0 graus é ao longo do eixo horizontal da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="70912-505">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-506">Aspecto</span><span class="sxs-lookup"><span data-stu-id="70912-506">Aspect</span></span></td>
<td><span data-ttu-id="70912-507"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="70912-507"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="70912-508">O atributo ImageSize será ajustado para preservar o aspecto da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-508">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="70912-509">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-509">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-510">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-510">Value</span></span></th>
<th><span data-ttu-id="70912-511">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-511">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-512">Ignorar</span><span class="sxs-lookup"><span data-stu-id="70912-512">Ignore</span></span></td>
<td><span data-ttu-id="70912-513">Ignorar problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="70912-513">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-514">Mínimo</span><span class="sxs-lookup"><span data-stu-id="70912-514">AtLeast</span></span></td>
<td><span data-ttu-id="70912-515">A imagem é pelo menos tão grande quanto o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-515">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-516">AtMost</span><span class="sxs-lookup"><span data-stu-id="70912-516">AtMost</span></span></td>
<td><span data-ttu-id="70912-517">A imagem não é maior que o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-517">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-518">Color</span><span class="sxs-lookup"><span data-stu-id="70912-518">Color</span></span></td>
<td><span data-ttu-id="70912-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> A cor de preenchimento principal.</span><span class="sxs-lookup"><span data-stu-id="70912-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="70912-520">Mesmo que o atributo FillColor na forma.</span><span class="sxs-lookup"><span data-stu-id="70912-520">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-521">Color2</span><span class="sxs-lookup"><span data-stu-id="70912-521">Color2</span></span></td>
<td><span data-ttu-id="70912-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="70912-523">A cor secundária de um preenchimento quando o tipo de imagem é padrão ou um preenchimento gradiente.</span><span class="sxs-lookup"><span data-stu-id="70912-523">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-524">Cores</span><span class="sxs-lookup"><span data-stu-id="70912-524">Colors</span></span></td>
<td><span data-ttu-id="70912-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="70912-526">Cores intermediárias no gradiente e suas posições relativas ao longo do gradiente, por exemplo, &quot; 30% vermelho, 70% azul, 90% verde &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-526">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="70912-527">A cor primária (atributo de cor em forma) é 0% e a cor secundária (atributo Color2) é de 100%.</span><span class="sxs-lookup"><span data-stu-id="70912-527">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-528">Foco</span><span class="sxs-lookup"><span data-stu-id="70912-528">Focus</span></span></td>
<td><span data-ttu-id="70912-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="70912-530">Ponto focal para preenchimento de gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="70912-530">Focal point for linear gradient fill.</span></span> <span data-ttu-id="70912-531">Os valores vão de-100 a + 100.</span><span class="sxs-lookup"><span data-stu-id="70912-531">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-532">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="70912-532">FocusPosition</span></span></td>
<td><span data-ttu-id="70912-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-534">Posição do retângulo mais interno para gradientes radiais.</span><span class="sxs-lookup"><span data-stu-id="70912-534">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="70912-535">O vetor é uma fração (0,0-1,0) da largura e da altura da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-535">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-536">FocusSize</span><span class="sxs-lookup"><span data-stu-id="70912-536">FocusSize</span></span></td>
<td><span data-ttu-id="70912-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Tamanho do retângulo mais interno para gradientes radiais.</span><span class="sxs-lookup"><span data-stu-id="70912-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="70912-538">O vetor é uma fração (0,0 a 1,0) da largura e da altura da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-538">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-539">Método</span><span class="sxs-lookup"><span data-stu-id="70912-539">Method</span></span></td>
<td><span data-ttu-id="70912-540">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="70912-540">VgSigmaType.</span></span> <span data-ttu-id="70912-541">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-541">Values include:</span></span>
<ul>
<li><span data-ttu-id="70912-542">Nenhum</span><span class="sxs-lookup"><span data-stu-id="70912-542">None</span></span></li>
<li><span data-ttu-id="70912-543">Linear</span><span class="sxs-lookup"><span data-stu-id="70912-543">Linear</span></span></li>
<li><span data-ttu-id="70912-544">Sigma</span><span class="sxs-lookup"><span data-stu-id="70912-544">Sigma</span></span></li>
<li><span data-ttu-id="70912-545">Qualquer</span><span class="sxs-lookup"><span data-stu-id="70912-545">Any</span></span></li>
</ul>
<p><span data-ttu-id="70912-546">O padrão é Sigma.</span><span class="sxs-lookup"><span data-stu-id="70912-546">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-547">Ativado</span><span class="sxs-lookup"><span data-stu-id="70912-547">On</span></span></td>
<td><span data-ttu-id="70912-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-549">Ativa a exibição de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="70912-549">Turns fill display on.</span></span> <span data-ttu-id="70912-550">O mesmo que o atributo Fill na forma.</span><span class="sxs-lookup"><span data-stu-id="70912-550">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-551">Opacidade</span><span class="sxs-lookup"><span data-stu-id="70912-551">Opacity</span></span></td>
<td><span data-ttu-id="70912-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="70912-553">Opacidade do preenchimento.</span><span class="sxs-lookup"><span data-stu-id="70912-553">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-554">Opacity2</span><span class="sxs-lookup"><span data-stu-id="70912-554">Opacity2</span></span></td>
<td><span data-ttu-id="70912-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="70912-556">A opacidade secundária para gradientes.</span><span class="sxs-lookup"><span data-stu-id="70912-556">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-557">Origem</span><span class="sxs-lookup"><span data-stu-id="70912-557">Origin</span></span></td>
<td><span data-ttu-id="70912-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-559">Ponto relativo ao canto superior esquerdo da imagem que é tratada como a origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-559">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="70912-560">O padrão é o centro da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-560">Default is the center of the image.</span></span> <span data-ttu-id="70912-561">O vetor é uma fração (de 0,0 a 1,0) da largura e da altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-561">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-562">Posição</span><span class="sxs-lookup"><span data-stu-id="70912-562">Position</span></span></td>
<td><span data-ttu-id="70912-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-564">Ponto no retângulo de referência da forma para posicionar a origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-564">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="70912-565">O padrão é o centro do retângulo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70912-565">Default is the center of the container rectangle.</span></span> <span data-ttu-id="70912-566">O vetor é uma fração (0,0-1,0) da largura e da altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-566">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-567">Tamanho</span><span class="sxs-lookup"><span data-stu-id="70912-567">Size</span></span></td>
<td><span data-ttu-id="70912-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-569">O tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-569">The size of the image.</span></span> <span data-ttu-id="70912-570">O padrão é o tamanho do pixel da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-570">Default is pixel size of the image.</span></span> <span data-ttu-id="70912-571">Pode ser especificado em coordenadas absolutas ou em porcentagem.</span><span class="sxs-lookup"><span data-stu-id="70912-571">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-572">Src</span><span class="sxs-lookup"><span data-stu-id="70912-572">Src</span></span></td>
<td><span data-ttu-id="70912-573"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-573"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="70912-574">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="70912-574">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="70912-575">Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="70912-575">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-576">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-576">Type</span></span></td>
<td><span data-ttu-id="70912-577">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="70912-577">VgFillType.</span></span> <span data-ttu-id="70912-578">Pode ser um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="70912-578">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="70912-579">Segundo plano</span><span class="sxs-lookup"><span data-stu-id="70912-579">Background</span></span></li>
<li><span data-ttu-id="70912-580">Quadro</span><span class="sxs-lookup"><span data-stu-id="70912-580">Frame</span></span></li>
<li><span data-ttu-id="70912-581">Gradient</span><span class="sxs-lookup"><span data-stu-id="70912-581">Gradient</span></span></li>
<li><span data-ttu-id="70912-582">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="70912-582">GradientCenter</span></span></li>
<li><span data-ttu-id="70912-583">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="70912-583">GradientRadial</span></span></li>
<li><span data-ttu-id="70912-584">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="70912-584">GradientTitle</span></span></li>
<li><span data-ttu-id="70912-585">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="70912-585">GradientUnscaled</span></span></li>
<li><span data-ttu-id="70912-586">Padrão</span><span class="sxs-lookup"><span data-stu-id="70912-586">Pattern</span></span></li>
<li><span data-ttu-id="70912-587">Sólido</span><span class="sxs-lookup"><span data-stu-id="70912-587">Solid</span></span></li>
<li><span data-ttu-id="70912-588">Tile</span><span class="sxs-lookup"><span data-stu-id="70912-588">Tile</span></span></li>
</ul>
<span data-ttu-id="70912-589">O bloco, o padrão e o quadro exigem que os atributos da imagem sejam fornecidos.</span><span class="sxs-lookup"><span data-stu-id="70912-589">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="70912-590">Gradiente e GradientRadial exigem que os atributos de gradiente sejam fornecidos.</span><span class="sxs-lookup"><span data-stu-id="70912-590">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="70912-591">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="70912-591">Group element</span></span>

<span data-ttu-id="70912-592">Um grupo é uma coleção de formas individuais que podem ser posicionadas e transformadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="70912-592">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|   <span data-ttu-id="70912-593">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-593">Attribute</span></span>        |   <span data-ttu-id="70912-594">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-594">Description</span></span>                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-595">Item</span><span class="sxs-lookup"><span data-stu-id="70912-595">Item</span></span>   | <span data-ttu-id="70912-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-597">Item especificado na matriz de formas.</span><span class="sxs-lookup"><span data-stu-id="70912-597">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="70912-598">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-598">Length</span></span> | <span data-ttu-id="70912-599">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-599">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-600">Número de formas neste grupo.</span><span class="sxs-lookup"><span data-stu-id="70912-600">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="70912-601">Elemento Imagedata</span><span class="sxs-lookup"><span data-stu-id="70912-601">Imagedata element</span></span>

<span data-ttu-id="70912-602">Descreve uma imagem a ser renderizada sobre uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-602">Describes a picture to be rendered on top of a shape.</span></span>



|   <span data-ttu-id="70912-603">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-603">Attribute</span></span>        |   <span data-ttu-id="70912-604">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-604">Description</span></span>                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-605">BiLevel</span><span class="sxs-lookup"><span data-stu-id="70912-605">BiLevel</span></span>     | <span data-ttu-id="70912-606">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-606">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-607">Exibir imagem em apenas duas cores (geralmente preto e branco).</span><span class="sxs-lookup"><span data-stu-id="70912-607">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="70912-608">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="70912-608">BlackLevel</span></span>  | <span data-ttu-id="70912-609">[VgAção .](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="70912-610">Permite o ajuste para definir o nível para que os pretos apareçam como pretos verdadeiros e todas as outras cores sejam visíveis como tons acima do preto.</span><span class="sxs-lookup"><span data-stu-id="70912-610">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="70912-611">Chromakey</span><span class="sxs-lookup"><span data-stu-id="70912-611">Chromakey</span></span>   | <span data-ttu-id="70912-612">[IVgColor.](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70912-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="70912-613">Cor transparente da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-613">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="70912-614">CropBottom</span><span class="sxs-lookup"><span data-stu-id="70912-614">CropBottom</span></span>  | <span data-ttu-id="70912-615">[VgNumber.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-616">Distância da recortar da parte inferior da imagem expressa como uma porcentagem do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-616">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="70912-617">CropLeft</span><span class="sxs-lookup"><span data-stu-id="70912-617">CropLeft</span></span>    | <span data-ttu-id="70912-618">[VgNumber.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-619">Distância de corte da borda esquerda da imagem expressa como uma fração do tamanho da imagem (de 0,0 a 1,0).</span><span class="sxs-lookup"><span data-stu-id="70912-619">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="70912-620">No entanto, há suporte para "corte de saída" e, portanto, há suporte para valores menores que 0 e maiores que 1; Por exemplo, -5, 20 cortaria os limites 25X do tamanho da imagem com 4/5 em um lado da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-620">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="70912-621">CropRight</span><span class="sxs-lookup"><span data-stu-id="70912-621">CropRight</span></span>   | <span data-ttu-id="70912-622">[VgNumber.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-623">Distância da recortar da direita da imagem expressa como uma porcentagem do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-623">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="70912-624">CropTop</span><span class="sxs-lookup"><span data-stu-id="70912-624">CropTop</span></span>     | <span data-ttu-id="70912-625">[VgNumber.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-626">Distância da recortar da parte superior da imagem expressa como uma porcentagem do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-626">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="70912-627">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="70912-627">EmbossColor</span></span> | <span data-ttu-id="70912-628">[IVgColor.](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70912-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="70912-629">Isso é definido como um percentual da cor da sombra para criar um efeito de imagem embossed.</span><span class="sxs-lookup"><span data-stu-id="70912-629">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="70912-630">Ganhar</span><span class="sxs-lookup"><span data-stu-id="70912-630">Gain</span></span>        | <span data-ttu-id="70912-631">[VgPositiveNumber.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-632">Ajusta a intensidade de todas as cores.</span><span class="sxs-lookup"><span data-stu-id="70912-632">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="70912-633">Essencialmente, define como o branco brilhante será.</span><span class="sxs-lookup"><span data-stu-id="70912-633">Essentially sets how bright white will be.</span></span> <span data-ttu-id="70912-634">Varia de 0 a 32767.</span><span class="sxs-lookup"><span data-stu-id="70912-634">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="70912-635">Gama</span><span class="sxs-lookup"><span data-stu-id="70912-635">Gamma</span></span>       | <span data-ttu-id="70912-636">[VgAção .](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="70912-637">Correção gama.</span><span class="sxs-lookup"><span data-stu-id="70912-637">Gamma correction.</span></span> <span data-ttu-id="70912-638">Aumentar isso dá mais contraste a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-638">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="70912-639">GrayScale</span><span class="sxs-lookup"><span data-stu-id="70912-639">GrayScale</span></span>   | <span data-ttu-id="70912-640">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-640">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-641">Exibir imagem em cores de escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="70912-641">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="70912-642">Src</span><span class="sxs-lookup"><span data-stu-id="70912-642">Src</span></span>         | <span data-ttu-id="70912-643">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-643">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-644">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="70912-644">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="70912-645">Esse atributo deve estar sempre presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="70912-645">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="70912-646">Elemento Path</span><span class="sxs-lookup"><span data-stu-id="70912-646">Path element</span></span>

<span data-ttu-id="70912-647">Define o caminho que com torna a forma, usando uma cadeia de caracteres que contém um conjunto rico de comandos de "movimentação de caneta".</span><span class="sxs-lookup"><span data-stu-id="70912-647">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-648">Limusine</span><span class="sxs-lookup"><span data-stu-id="70912-648">Limo</span></span></td>
<td><span data-ttu-id="70912-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D.</a></span><span class="sxs-lookup"><span data-stu-id="70912-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="70912-650">Define o ponto em que a forma é alongada; Por exemplo, para uma forma de mada, o ponto de shape deve estar no rosto, portanto, quando a forma for re dimensionada, o rosto se alongará e o restante da forma manterá suas dimensões.</span><span class="sxs-lookup"><span data-stu-id="70912-650">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-651">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="70912-651">TextBoxRect</span></span></td>
<td><span data-ttu-id="70912-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray.</a></span><span class="sxs-lookup"><span data-stu-id="70912-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="70912-653">Matriz que contém os retângulos que definem para onde o texto deve ir.</span><span class="sxs-lookup"><span data-stu-id="70912-653">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-654">V</span><span class="sxs-lookup"><span data-stu-id="70912-654">V</span></span></td>
<td><span data-ttu-id="70912-655"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-655"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="70912-656">Corresponde ao atributo v na marca Path.</span><span class="sxs-lookup"><span data-stu-id="70912-656">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="70912-657">Observe que o caminho pode corresponder ao atributo ou elemento Path.</span><span class="sxs-lookup"><span data-stu-id="70912-657">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-658">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-658">Value</span></span></td>
<td><span data-ttu-id="70912-659"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-659"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="70912-660">Uma representação de texto dos comandos que definem o caminho.</span><span class="sxs-lookup"><span data-stu-id="70912-660">A text representation of the commands that define the path.</span></span> <span data-ttu-id="70912-661">Valores de coordenada x ou y podem ser uma referência a uma fórmula no formato em que # é o número &quot; @# &quot; ordinal da fórmula, por exemplo, &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-661">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="70912-662">Essa cadeia de caracteres de atributo é feita de um conjunto rico de comandos, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="70912-662">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-663">Comando</span><span class="sxs-lookup"><span data-stu-id="70912-663">Command</span></span></th>
<th><span data-ttu-id="70912-664">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-664">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-665">ae (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="70912-665">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="70912-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span><span class="sxs-lookup"><span data-stu-id="70912-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="70912-667">Desenhar um segmento de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="70912-667">Draw a segment of an ellipse.</span></span> <span data-ttu-id="70912-668">Uma linha reta é desenhada do ponto atual para o ponto inicial do segmento.</span><span class="sxs-lookup"><span data-stu-id="70912-668">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-669">al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="70912-669">al (angleelipse)</span></span></td>
<td><span data-ttu-id="70912-670">O mesmo que ae, exceto que há um m implícito para o ponto de partida do segmento.</span><span class="sxs-lookup"><span data-stu-id="70912-670">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-671">ar (arc)</span><span class="sxs-lookup"><span data-stu-id="70912-671">ar (arc)</span></span></td>
<td><span data-ttu-id="70912-672">O mesmo que em.</span><span class="sxs-lookup"><span data-stu-id="70912-672">Same as at.</span></span> <span data-ttu-id="70912-673">No entanto, um novo subcaminho é iniciado por um m implícito para o ponto inicial do arco.</span><span class="sxs-lookup"><span data-stu-id="70912-673">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-674">at (arcto)</span><span class="sxs-lookup"><span data-stu-id="70912-674">at (arcto)</span></span></td>
<td><span data-ttu-id="70912-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="70912-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="70912-676">Os quatro primeiros valores definem a caixa delimitador de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="70912-676">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="70912-677">Os últimos quatro definem dois vetores radiais.</span><span class="sxs-lookup"><span data-stu-id="70912-677">The last four define two radial vectors.</span></span> <span data-ttu-id="70912-678">Um segmento da elipse é desenhado que começa no ângulo definido pelo vetor de raio inicial e termina no ângulo definido pelo vetor final.</span><span class="sxs-lookup"><span data-stu-id="70912-678">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="70912-679">Uma linha reta é desenhada do ponto atual para o início do arco. O arco sempre é desenhado em uma direção no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="70912-679">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-680">c (curveto)</span><span class="sxs-lookup"><span data-stu-id="70912-680">c (curveto)</span></span></td>
<td><span data-ttu-id="70912-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>para</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="70912-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="70912-682">Desenhe uma curva de bezier cúbica do ponto atual para a coordenada dada pelos dois parâmetros finais, os pontos de controle dados pelos quatro primeiros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="70912-682">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="70912-683">O ponto atual se torna o ponto de extremidade do bezier.</span><span class="sxs-lookup"><span data-stu-id="70912-683">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-684">e (fim)</span><span class="sxs-lookup"><span data-stu-id="70912-684">e (end)</span></span></td>
<td><span data-ttu-id="70912-685">Encerrar o conjunto atual de subcaminhos.</span><span class="sxs-lookup"><span data-stu-id="70912-685">End the current set of subpaths.</span></span> <span data-ttu-id="70912-686">Um determinado conjunto de subcamadas (conforme delimitado por fim) são preenchidos usando eofill.</span><span class="sxs-lookup"><span data-stu-id="70912-686">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="70912-687">Os conjuntos subsequentes de subcaminhos são preenchidos de forma independente e sobrepostos aos existentes.</span><span class="sxs-lookup"><span data-stu-id="70912-687">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-688">l (lineto)</span><span class="sxs-lookup"><span data-stu-id="70912-688">l (lineto)</span></span></td>
<td><span data-ttu-id="70912-689">x, y</span><span class="sxs-lookup"><span data-stu-id="70912-689">x,y</span></span><br/> <span data-ttu-id="70912-690">Desenhe uma linha do ponto atual para a coordenada x,y determinada, que se torna o novo ponto atual.</span><span class="sxs-lookup"><span data-stu-id="70912-690">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="70912-691">Pares de coordenadas adicionais podem ser especificados para formar uma polilinha, por exemplo, &quot; l 10,13,45,27,89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="70912-691">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-692">m (moveto)</span><span class="sxs-lookup"><span data-stu-id="70912-692">m (moveto)</span></span></td>
<td><span data-ttu-id="70912-693">x, y</span><span class="sxs-lookup"><span data-stu-id="70912-693">x,y</span></span><br/> <span data-ttu-id="70912-694">Inicie um novo subcaminho na coordenada x,y determinada.</span><span class="sxs-lookup"><span data-stu-id="70912-694">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-695">nf (nofill)</span><span class="sxs-lookup"><span data-stu-id="70912-695">nf (nofill)</span></span></td>
<td><span data-ttu-id="70912-696">O conjunto atual de subcaminhos (delimitado por fim) não será preenchido.</span><span class="sxs-lookup"><span data-stu-id="70912-696">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-697">ns (nostroke)</span><span class="sxs-lookup"><span data-stu-id="70912-697">ns (nostroke)</span></span></td>
<td><span data-ttu-id="70912-698">O conjunto atual de subcamadas (delimitados por fim) não será traço.</span><span class="sxs-lookup"><span data-stu-id="70912-698">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-699">qb (quadrático)</span><span class="sxs-lookup"><span data-stu-id="70912-699">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="70912-700">(<strong>ponto de</strong>controle (x, y))\*,<strong>final</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="70912-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="70912-701">Define uma ou mais curvas de bézier quadráticas por meio de pontos de controle e um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="70912-701">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="70912-702">Pontos intermediários (na curva) são obtidos pela interpolação entre pontos de controle sucessivos semelhantes às fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="70912-702">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="70912-703">O subcaminho não precisa ser um início, caso em que o subcaminho é fechado e o último ponto define o ponto inicial.</span><span class="sxs-lookup"><span data-stu-id="70912-703">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-704">qx (elipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="70912-704">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="70912-705"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="70912-705"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="70912-706">Uma elipse de trimestre é desenhada do ponto atual para o ponto de extremidade determinado.</span><span class="sxs-lookup"><span data-stu-id="70912-706">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="70912-707">O segmento elíptico é inicialmente tangente a uma linha paralela ao eixo x; Ou seja, o segmento começa horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="70912-707">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-708">qy (elipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="70912-708">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="70912-709"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="70912-709"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="70912-710">O mesmo que qx, exceto que o segmento elíptico é inicialmente tangente a uma linha paralela ao eixo y; Ou seja, o segmento começa verticalmente.</span><span class="sxs-lookup"><span data-stu-id="70912-710">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-711">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="70912-711">r (rlineto)</span></span></td>
<td><span data-ttu-id="70912-712">x, y</span><span class="sxs-lookup"><span data-stu-id="70912-712">x,y</span></span> <br/> <span data-ttu-id="70912-713">Desenhar uma linha do ponto atual para a coordenada relativa (cpx + x, cpy + y).</span><span class="sxs-lookup"><span data-stu-id="70912-713">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="70912-714">Se pares de coordenadas adicionais são dados, cada novo ponto é calculado em relação ao último.</span><span class="sxs-lookup"><span data-stu-id="70912-714">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-715">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="70912-715">t (rmoveto)</span></span></td>
<td><span data-ttu-id="70912-716">x, y</span><span class="sxs-lookup"><span data-stu-id="70912-716">x,y</span></span><br/> <span data-ttu-id="70912-717">Inicie um novo subcaminho nas coordenadas relativas ( cpx + x, cpy + y) em que cpx, cpy é a posição atual.</span><span class="sxs-lookup"><span data-stu-id="70912-717">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-718">v (curveto)</span><span class="sxs-lookup"><span data-stu-id="70912-718">v (curveto)</span></span></td>
<td><span data-ttu-id="70912-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>para</strong> (x,y)</span><span class="sxs-lookup"><span data-stu-id="70912-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="70912-720">Curva de bezier cúbica usando as coordenadas fornecidas em relação ao ponto atual.</span><span class="sxs-lookup"><span data-stu-id="70912-720">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="70912-721">Todos os pontos são computados em relação ao mesmo ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="70912-721">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-722">wa (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="70912-722">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="70912-723">O mesmo que em , mas o arco é desenhado em uma direção horário.</span><span class="sxs-lookup"><span data-stu-id="70912-723">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-724">wr (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="70912-724">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="70912-725">O mesmo que ar, mas é desenhado em uma direção horário.</span><span class="sxs-lookup"><span data-stu-id="70912-725">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-726">x (fechar)</span><span class="sxs-lookup"><span data-stu-id="70912-726">x (close)</span></span></td>
<td><span data-ttu-id="70912-727">Feche o subcaminho atual desenhando uma linha reta do ponto atual para o ponto de movimentação original.</span><span class="sxs-lookup"><span data-stu-id="70912-727">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="70912-728">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="70912-728">Shadow element</span></span>

<span data-ttu-id="70912-729">Descreve um efeito de sombra em uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-729">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-730">Color</span><span class="sxs-lookup"><span data-stu-id="70912-730">Color</span></span></td>
<td><span data-ttu-id="70912-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor.</a></span><span class="sxs-lookup"><span data-stu-id="70912-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="70912-732">Cor da sombra primária.</span><span class="sxs-lookup"><span data-stu-id="70912-732">Color of the primary shadow.</span></span> <span data-ttu-id="70912-733">O padrão é RGB(128.128.128)</span><span class="sxs-lookup"><span data-stu-id="70912-733">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-734">Color2</span><span class="sxs-lookup"><span data-stu-id="70912-734">Color2</span></span></td>
<td><span data-ttu-id="70912-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor.</a></span><span class="sxs-lookup"><span data-stu-id="70912-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="70912-736">Cor da segunda sombra ou realçada em uma sombra embossada ou gravada.</span><span class="sxs-lookup"><span data-stu-id="70912-736">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="70912-737">O padrão é RGB(203.203.203).</span><span class="sxs-lookup"><span data-stu-id="70912-737">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-738">Matriz</span><span class="sxs-lookup"><span data-stu-id="70912-738">Matrix</span></span></td>
<td><span data-ttu-id="70912-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix.</a></span><span class="sxs-lookup"><span data-stu-id="70912-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="70912-740">Uma matriz de transformação de perspectiva no formato, &quot; sxx, sxy, syx, syy, px,py &quot; [s=scale, p=perspective].</span><span class="sxs-lookup"><span data-stu-id="70912-740">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="70912-741">Os itens s especificam como a sombra deve ser dimensionada em relação à forma e os itens p especificam como a sombra deve se distorcer em relação à forma.</span><span class="sxs-lookup"><span data-stu-id="70912-741">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="70912-742">Por exemplo, a matriz a seguir ressaliza a forma por um fator de 2 e distorce-a por um fator de 4 em todas as direções:</span><span class="sxs-lookup"><span data-stu-id="70912-742">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="70912-743">&quot;2,2,2,2,4,4&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-743">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="70912-744">Essa matriz só será usada se o tipo da sombra estiver definido como perspectiva.</span><span class="sxs-lookup"><span data-stu-id="70912-744">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-745">Obscurecida</span><span class="sxs-lookup"><span data-stu-id="70912-745">Obscured</span></span></td>
<td><span data-ttu-id="70912-746"><a href="msdn-online-vml-vgtristate.md">VgTriState.</a></span><span class="sxs-lookup"><span data-stu-id="70912-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-747">A sombra poderá ser vista por meio de se não houver nenhum preenchimento na forma.</span><span class="sxs-lookup"><span data-stu-id="70912-747">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="70912-748">O padrão é Falso.</span><span class="sxs-lookup"><span data-stu-id="70912-748">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-749">Deslocamento</span><span class="sxs-lookup"><span data-stu-id="70912-749">Offset</span></span></td>
<td><span data-ttu-id="70912-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset.</a></span><span class="sxs-lookup"><span data-stu-id="70912-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="70912-751">Quantidade de deslocamento x,y do local da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-751">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="70912-752">O padrão &quot; é 2pt,2pt. &quot;</span><span class="sxs-lookup"><span data-stu-id="70912-752">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-753">Offset2</span><span class="sxs-lookup"><span data-stu-id="70912-753">Offset2</span></span></td>
<td><span data-ttu-id="70912-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-755">Quantidade de deslocamento x,y segundo da localização da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-755">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="70912-756">Os valores são uma medida absoluta ou um valor fracionado de forma (-0,5 a +0,5).</span><span class="sxs-lookup"><span data-stu-id="70912-756">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-757">Ativado</span><span class="sxs-lookup"><span data-stu-id="70912-757">On</span></span></td>
<td><span data-ttu-id="70912-758"><a href="msdn-online-vml-vgtristate.md">VgTriState.</a></span><span class="sxs-lookup"><span data-stu-id="70912-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-759">Liga e desliga a exibição da sombra.</span><span class="sxs-lookup"><span data-stu-id="70912-759">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-760">Opacidade</span><span class="sxs-lookup"><span data-stu-id="70912-760">Opacity</span></span></td>
<td><span data-ttu-id="70912-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgAção .</a></span><span class="sxs-lookup"><span data-stu-id="70912-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="70912-762">Opacidade do efeito de sombra.</span><span class="sxs-lookup"><span data-stu-id="70912-762">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-763">Origem</span><span class="sxs-lookup"><span data-stu-id="70912-763">Origin</span></span></td>
<td><span data-ttu-id="70912-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Um par de valores fracionados de forma de -0,5 a +0,5.</span><span class="sxs-lookup"><span data-stu-id="70912-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-765">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-765">Type</span></span></td>
<td><span data-ttu-id="70912-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="70912-767">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-767">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-768">Único (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-768">Single (default)</span></span></li>
<li><span data-ttu-id="70912-769">Double</span><span class="sxs-lookup"><span data-stu-id="70912-769">Double</span></span></li>
<li><span data-ttu-id="70912-770">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="70912-770">Perspective</span></span></li>
<li><span data-ttu-id="70912-771">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="70912-771">ShapeRelative</span></span></li>
<li><span data-ttu-id="70912-772">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="70912-772">DrawingRelative</span></span></li>
<li><span data-ttu-id="70912-773">Emboss</span><span class="sxs-lookup"><span data-stu-id="70912-773">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="70912-774">Elemento Skew</span><span class="sxs-lookup"><span data-stu-id="70912-774">Skew element</span></span>

<span data-ttu-id="70912-775">Descreve um efeito de distorção de perspectiva em uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-775">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="70912-776">A distorção é aplicada a dados gráficos vetoriais, não a dados de imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-776">The skew is applied to vector graphic data, not image data.</span></span>



|   <span data-ttu-id="70912-777">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-777">Attribute</span></span>        |   <span data-ttu-id="70912-778">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-778">Description</span></span>                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-779">Matriz</span><span class="sxs-lookup"><span data-stu-id="70912-779">Matrix</span></span> | <span data-ttu-id="70912-780">[IVgSkewMatrix.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-781">Uma matriz de transformação de perspectiva no formulário, "sxx, sxy, syx, syy,px,py" \[ s=scale, p=perspective \] .</span><span class="sxs-lookup"><span data-stu-id="70912-781">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="70912-782">Se offset estiver em unidades absolutas, px,py estão em emu ^ -1 unidades; caso contrário, eles serão uma fração inversa do tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-782">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="70912-783">Deslocamento</span><span class="sxs-lookup"><span data-stu-id="70912-783">Offset</span></span> | <span data-ttu-id="70912-784">[IvgSkewOffset.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-785">Quantidade de deslocamento x,y do local da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-785">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="70912-786">O padrão é "2pt,2pt".</span><span class="sxs-lookup"><span data-stu-id="70912-786">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="70912-787">Ativado</span><span class="sxs-lookup"><span data-stu-id="70912-787">On</span></span>     | <span data-ttu-id="70912-788">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-788">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-789">Liga ou desliga a exibição da distorção.</span><span class="sxs-lookup"><span data-stu-id="70912-789">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="70912-790">Origem</span><span class="sxs-lookup"><span data-stu-id="70912-790">Origin</span></span> | <span data-ttu-id="70912-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="70912-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-792">Um par de valores fracionados de forma de -0,5 a +0,5.</span><span class="sxs-lookup"><span data-stu-id="70912-792">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="70912-793">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="70912-793">Stroke element</span></span>

<span data-ttu-id="70912-794">Descreve como desenhar o caminho se algo além de uma linha sólida com uma cor sólida for desejado.</span><span class="sxs-lookup"><span data-stu-id="70912-794">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-795">Color</span><span class="sxs-lookup"><span data-stu-id="70912-795">Color</span></span></td>
<td><span data-ttu-id="70912-796"><a href="msdn-online-vml-vgtristate.md">VgTriState.</a></span><span class="sxs-lookup"><span data-stu-id="70912-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-797">A cor da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-797">The color of the line.</span></span> <span data-ttu-id="70912-798">O mesmo que o atributo StrokeColor em Forma, mas o substitui.</span><span class="sxs-lookup"><span data-stu-id="70912-798">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-799">Color2</span><span class="sxs-lookup"><span data-stu-id="70912-799">Color2</span></span></td>
<td><span data-ttu-id="70912-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor.</a></span><span class="sxs-lookup"><span data-stu-id="70912-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="70912-801">Cor secundária.</span><span class="sxs-lookup"><span data-stu-id="70912-801">Secondary color.</span></span> <span data-ttu-id="70912-802">Usado quando FillType é Pattern.</span><span class="sxs-lookup"><span data-stu-id="70912-802">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-803">Dashstyle</span><span class="sxs-lookup"><span data-stu-id="70912-803">DashStyle</span></span></td>
<td><span data-ttu-id="70912-804"><strong>VgLineDashStyle.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-804"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="70912-805">Formato de estilo traço.</span><span class="sxs-lookup"><span data-stu-id="70912-805">Dash style format.</span></span> <span data-ttu-id="70912-806">Pode ser um valor específico ou uma sequência de números com um padrão de traço definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="70912-806">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="70912-807">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-807">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-808">Solid (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-808">Solid (default)</span></span></li>
<li><span data-ttu-id="70912-809">ShortDash</span><span class="sxs-lookup"><span data-stu-id="70912-809">ShortDash</span></span></li>
<li><span data-ttu-id="70912-810">ShortDot</span><span class="sxs-lookup"><span data-stu-id="70912-810">ShortDot</span></span></li>
<li><span data-ttu-id="70912-811">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="70912-811">ShortDashDot</span></span></li>
<li><span data-ttu-id="70912-812">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="70912-812">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="70912-813">Ponto</span><span class="sxs-lookup"><span data-stu-id="70912-813">Dot</span></span></li>
<li><span data-ttu-id="70912-814">Traço</span><span class="sxs-lookup"><span data-stu-id="70912-814">Dash</span></span></li>
<li><span data-ttu-id="70912-815">DashDot</span><span class="sxs-lookup"><span data-stu-id="70912-815">DashDot</span></span></li>
<li><span data-ttu-id="70912-816">LongDash</span><span class="sxs-lookup"><span data-stu-id="70912-816">LongDash</span></span></li>
<li><span data-ttu-id="70912-817">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="70912-817">LongDashDot</span></span></li>
<li><span data-ttu-id="70912-818">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="70912-818">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-819">EndArrow</span><span class="sxs-lookup"><span data-stu-id="70912-819">EndArrow</span></span></td>
<td><span data-ttu-id="70912-820"><strong>VgArrowheadStyle.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-820"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="70912-821">Seta para o final da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-821">Arrowhead for the end of the line.</span></span> <span data-ttu-id="70912-822">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-822">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-823">Nenhum (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-823">None (default)</span></span></li>
<li><span data-ttu-id="70912-824">Bloquear</span><span class="sxs-lookup"><span data-stu-id="70912-824">Block</span></span></li>
<li><span data-ttu-id="70912-825">Clássico</span><span class="sxs-lookup"><span data-stu-id="70912-825">Classic</span></span></li>
<li><span data-ttu-id="70912-826">Diamond</span><span class="sxs-lookup"><span data-stu-id="70912-826">Diamond</span></span></li>
<li><span data-ttu-id="70912-827">Oval</span><span class="sxs-lookup"><span data-stu-id="70912-827">Oval</span></span></li>
<li><span data-ttu-id="70912-828">Aberto</span><span class="sxs-lookup"><span data-stu-id="70912-828">Open</span></span></li>
<li><span data-ttu-id="70912-829">Divisa</span><span class="sxs-lookup"><span data-stu-id="70912-829">Chevron</span></span></li>
<li><span data-ttu-id="70912-830">DoubleTronron</span><span class="sxs-lookup"><span data-stu-id="70912-830">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-831">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="70912-831">EndArrowLength</span></span></td>
<td><span data-ttu-id="70912-832"><strong>VgArrowHeadLength.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-832"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="70912-833">Comprimento da seta para o final da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-833">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="70912-834">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-834">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-835">Short</span><span class="sxs-lookup"><span data-stu-id="70912-835">Short</span></span></li>
<li><span data-ttu-id="70912-836">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-836">Medium (default)</span></span></li>
<li><span data-ttu-id="70912-837">long</span><span class="sxs-lookup"><span data-stu-id="70912-837">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-838">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="70912-838">EndArrowWidth</span></span></td>
<td><span data-ttu-id="70912-839"><strong>VgArrowheadWidth.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-839"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="70912-840">Largura da seta para o final da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-840">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="70912-841">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-841">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-842">Estreito</span><span class="sxs-lookup"><span data-stu-id="70912-842">Narrow</span></span></li>
<li><span data-ttu-id="70912-843">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-843">Medium (default)</span></span></li>
<li><span data-ttu-id="70912-844">Ampla</span><span class="sxs-lookup"><span data-stu-id="70912-844">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-845">Endcap</span><span class="sxs-lookup"><span data-stu-id="70912-845">EndCap</span></span></td>
<td><span data-ttu-id="70912-846"><strong>VgLineEndCapStyle.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-846"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="70912-847">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-847">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-848">Plano</span><span class="sxs-lookup"><span data-stu-id="70912-848">Flat</span></span></li>
<li><span data-ttu-id="70912-849">Square</span><span class="sxs-lookup"><span data-stu-id="70912-849">Square</span></span></li>
<li><span data-ttu-id="70912-850">Round</span><span class="sxs-lookup"><span data-stu-id="70912-850">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-851">Filltype</span><span class="sxs-lookup"><span data-stu-id="70912-851">FillType</span></span></td>
<td><span data-ttu-id="70912-852"><strong>VgLineFillType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-852"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="70912-853">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-853">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-854">Solid (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-854">Solid (default)</span></span></li>
<li><span data-ttu-id="70912-855">Tile</span><span class="sxs-lookup"><span data-stu-id="70912-855">Tile</span></span></li>
<li><span data-ttu-id="70912-856">Padrão</span><span class="sxs-lookup"><span data-stu-id="70912-856">Pattern</span></span></li>
<li><span data-ttu-id="70912-857">Quadro</span><span class="sxs-lookup"><span data-stu-id="70912-857">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-858">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="70912-858">ImageAlignShape</span></span></td>
<td><span data-ttu-id="70912-859"><a href="msdn-online-vml-vgtristate.md">VgTriState.</a></span><span class="sxs-lookup"><span data-stu-id="70912-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-860">Alinhe a imagem com a forma.</span><span class="sxs-lookup"><span data-stu-id="70912-860">Align the image with the shape.</span></span> <span data-ttu-id="70912-861">Se False, alinhe a imagem com a janela.</span><span class="sxs-lookup"><span data-stu-id="70912-861">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-862">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="70912-862">ImageAspect</span></span></td>
<td><span data-ttu-id="70912-863"><strong>VgAspectType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-863"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="70912-864">O atributo ImageSize será ajustado para preservar o aspecto da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-864">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="70912-865">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-865">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-866">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-866">Value</span></span></th>
<th><span data-ttu-id="70912-867">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-867">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-868">Ignorar</span><span class="sxs-lookup"><span data-stu-id="70912-868">Ignore</span></span></td>
<td><span data-ttu-id="70912-869">Ignorar problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="70912-869">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-870">Atleast</span><span class="sxs-lookup"><span data-stu-id="70912-870">AtLeast</span></span></td>
<td><span data-ttu-id="70912-871">A imagem é pelo menos tão grande quanto o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-871">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-872">No mais alto nível</span><span class="sxs-lookup"><span data-stu-id="70912-872">AtMost</span></span></td>
<td><span data-ttu-id="70912-873">A imagem não é maior que o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-873">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-874">Imagesize</span><span class="sxs-lookup"><span data-stu-id="70912-874">ImageSize</span></span></td>
<td><span data-ttu-id="70912-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="70912-876">Tamanho da imagem com a que formar o pincel.</span><span class="sxs-lookup"><span data-stu-id="70912-876">Size of the image to form the brush with.</span></span> <span data-ttu-id="70912-877">O padrão é o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="70912-877">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-878">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="70912-878">JoinStyle</span></span></td>
<td><span data-ttu-id="70912-879"><strong>VgLineJoinStyle.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-879"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="70912-880">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-880">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-881">Arredondado (junção arredondada)</span><span class="sxs-lookup"><span data-stu-id="70912-881">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="70912-882">Bevel (junção em bevel)</span><span class="sxs-lookup"><span data-stu-id="70912-882">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="70912-883">Miter (conjunto de miter)</span><span class="sxs-lookup"><span data-stu-id="70912-883">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-884">Estilo de Linha</span><span class="sxs-lookup"><span data-stu-id="70912-884">LineStyle</span></span></td>
<td><span data-ttu-id="70912-885"><strong>VgLineStyle.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-885"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="70912-886">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-886">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-887">Único</span><span class="sxs-lookup"><span data-stu-id="70912-887">Single</span></span></li>
<li><span data-ttu-id="70912-888">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="70912-888">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="70912-889">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="70912-889">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="70912-890">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="70912-890">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="70912-891">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="70912-891">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-892">Miterlimit</span><span class="sxs-lookup"><span data-stu-id="70912-892">MiterLimit</span></span></td>
<td><span data-ttu-id="70912-893"><a href="msdn-online-vml-vglength.md">Comprimento</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-893"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="70912-894">A distância máxima entre o ponto interno e o ponto externo de uma junção.</span><span class="sxs-lookup"><span data-stu-id="70912-894">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="70912-895">Esse número é um múltiplo da espessura da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-895">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="70912-896">Varia de 0 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="70912-896">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-897">Ativado</span><span class="sxs-lookup"><span data-stu-id="70912-897">On</span></span></td>
<td><span data-ttu-id="70912-898"><a href="msdn-online-vml-vgtristate.md">VgTriState.</a></span><span class="sxs-lookup"><span data-stu-id="70912-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="70912-899">Liga e desliga a exibição da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-899">Turns the display of the line on and off.</span></span> <span data-ttu-id="70912-900">O mesmo que o atributo Stroke em Forma, mas o substitui.</span><span class="sxs-lookup"><span data-stu-id="70912-900">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-901">Opacidade</span><span class="sxs-lookup"><span data-stu-id="70912-901">Opacity</span></span></td>
<td><span data-ttu-id="70912-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgAção .</a></span><span class="sxs-lookup"><span data-stu-id="70912-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="70912-903">Opacidade do traço.</span><span class="sxs-lookup"><span data-stu-id="70912-903">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-904">Src</span><span class="sxs-lookup"><span data-stu-id="70912-904">Src</span></span></td>
<td><span data-ttu-id="70912-905">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70912-905">String.</span></span> <span data-ttu-id="70912-906">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="70912-906">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="70912-907">Esse atributo deve estar sempre presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="70912-907">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-908">StartArrow</span><span class="sxs-lookup"><span data-stu-id="70912-908">StartArrow</span></span></td>
<td><span data-ttu-id="70912-909"><strong>VgArrowheadStyle.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-909"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="70912-910">Seta para o início da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-910">Arrowhead for the start of the line.</span></span> <span data-ttu-id="70912-911">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-911">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-912">Nenhum (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-912">None (default)</span></span></li>
<li><span data-ttu-id="70912-913">Bloquear</span><span class="sxs-lookup"><span data-stu-id="70912-913">Block</span></span></li>
<li><span data-ttu-id="70912-914">Clássico</span><span class="sxs-lookup"><span data-stu-id="70912-914">Classic</span></span></li>
<li><span data-ttu-id="70912-915">Diamond</span><span class="sxs-lookup"><span data-stu-id="70912-915">Diamond</span></span></li>
<li><span data-ttu-id="70912-916">Oval</span><span class="sxs-lookup"><span data-stu-id="70912-916">Oval</span></span></li>
<li><span data-ttu-id="70912-917">Aberto</span><span class="sxs-lookup"><span data-stu-id="70912-917">Open</span></span></li>
<li><span data-ttu-id="70912-918">Divisa</span><span class="sxs-lookup"><span data-stu-id="70912-918">Chevron</span></span></li>
<li><span data-ttu-id="70912-919">DoubleTronron</span><span class="sxs-lookup"><span data-stu-id="70912-919">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-920">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="70912-920">StartArrowLength</span></span></td>
<td><span data-ttu-id="70912-921">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="70912-921">VgArrowHeadLength.</span></span> <span data-ttu-id="70912-922">Comprimento da seta para o início da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-922">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="70912-923">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-923">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-924">Short</span><span class="sxs-lookup"><span data-stu-id="70912-924">Short</span></span></li>
<li><span data-ttu-id="70912-925">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="70912-925">Medium (default)</span></span></li>
<li><span data-ttu-id="70912-926">long</span><span class="sxs-lookup"><span data-stu-id="70912-926">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-927">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="70912-927">StartArrowWidth</span></span></td>
<td><span data-ttu-id="70912-928">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="70912-928">VgArrowheadWidth.</span></span> <span data-ttu-id="70912-929">Largura da seta para o início da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-929">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="70912-930">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-930">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-931">Médio Estreito (padrão) Largo</span><span class="sxs-lookup"><span data-stu-id="70912-931">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-932">Peso</span><span class="sxs-lookup"><span data-stu-id="70912-932">Weight</span></span></td>
<td><span data-ttu-id="70912-933"><a href="msdn-online-vml-vglength.md">VgLength.</a></span><span class="sxs-lookup"><span data-stu-id="70912-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="70912-934">Largura da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-934">Width of line.</span></span> <span data-ttu-id="70912-935">Varia de 0 a 1584.</span><span class="sxs-lookup"><span data-stu-id="70912-935">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="70912-936">O atributo DashStyle permite que o usuário especifique um padrão de traço definido personalizado.</span><span class="sxs-lookup"><span data-stu-id="70912-936">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="70912-937">Isso é feito usando uma série de números.</span><span class="sxs-lookup"><span data-stu-id="70912-937">This is done using a series of numbers.</span></span> <span data-ttu-id="70912-938">Os estilos de traço são definidos em termos do comprimento do traço (a parte desenhada do traço) e do comprimento do espaço entre os traços.</span><span class="sxs-lookup"><span data-stu-id="70912-938">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="70912-939">Os comprimentos são relativos à largura da linha; um comprimento de &quot; 1 &quot; é igual à largura da linha.</span><span class="sxs-lookup"><span data-stu-id="70912-939">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="70912-940">O estilo EndCap é aplicado a cada traço, os estilos de seta não são.</span><span class="sxs-lookup"><span data-stu-id="70912-940">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="70912-941">A cadeia de caracteres primeiro define o comprimento do traço e, em seguida, o comprimento do espaço.</span><span class="sxs-lookup"><span data-stu-id="70912-941">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="70912-942">Isso pode ser repetido para formar estilos de traço complexos.</span><span class="sxs-lookup"><span data-stu-id="70912-942">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="70912-943">A cadeia de caracteres sempre deve conter um par de números; se ele contiver um número ímpar de números, o último poderá ser desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="70912-943">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="70912-944">A tabela a seguir lista alguns valores típicos e uma descrição do efeito pretendido.</span><span class="sxs-lookup"><span data-stu-id="70912-944">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="70912-945">&quot;0 implica um ponto que deve ser simétrico de quatro vezes &quot; (com extremidades de arredondamento, ele deve ser um círculo).</span><span class="sxs-lookup"><span data-stu-id="70912-945">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="70912-946">Se a extremidade de linha for Simples, um visualizador deverá escolher um traço do sistema operacional integrado sempre que possível (ou seja, algo rápido de desenhar).</span><span class="sxs-lookup"><span data-stu-id="70912-946">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="70912-947">O exemplo a seguir mostra alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="70912-947">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-948">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-948">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="70912-949">traços curtos (cada traço e o espaço entre é duas vezes a largura da linha)</span><span class="sxs-lookup"><span data-stu-id="70912-949">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-950">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-950">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="70912-951">dot (cada traço é a largura da linha, enquanto cada espaço tem duas vezes a largura da linha)</span><span class="sxs-lookup"><span data-stu-id="70912-951">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-952">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-952">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="70912-953">traço (cada traço é quatro vezes a largura da linha, enquanto cada espaço tem duas vezes a largura da linha)</span><span class="sxs-lookup"><span data-stu-id="70912-953">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-954">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-954">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="70912-955">traço longo</span><span class="sxs-lookup"><span data-stu-id="70912-955">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-956">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-956">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="70912-957">ponto de traço</span><span class="sxs-lookup"><span data-stu-id="70912-957">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-958">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-958">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="70912-959">ponto de traço longo</span><span class="sxs-lookup"><span data-stu-id="70912-959">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-960">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="70912-960">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="70912-961">ponto de traço longo</span><span class="sxs-lookup"><span data-stu-id="70912-961">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="70912-962">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="70912-962">TextPath element</span></span>

<span data-ttu-id="70912-963">Descreve um caminho de vetor com base nos dados de texto, na fonte e nos estilos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="70912-963">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="70912-964">O caminho de texto é distorcido para estar em conformidade com um **elemento Path,** se fornecido.</span><span class="sxs-lookup"><span data-stu-id="70912-964">The text path is warped to conform to a **Path** element if supplied.</span></span>



|   <span data-ttu-id="70912-965">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-965">Attribute</span></span>        |   <span data-ttu-id="70912-966">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-966">Description</span></span>                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-967">FitPath</span><span class="sxs-lookup"><span data-stu-id="70912-967">FitPath</span></span>  | <span data-ttu-id="70912-968">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-968">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-969">Tamanhos do texto para preencher o caminho em que ele está.</span><span class="sxs-lookup"><span data-stu-id="70912-969">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="70912-970">FitShape</span><span class="sxs-lookup"><span data-stu-id="70912-970">FitShape</span></span> | <span data-ttu-id="70912-971">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-971">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-972">Estende o caminho de texto para as bordas da caixa de forma.</span><span class="sxs-lookup"><span data-stu-id="70912-972">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="70912-973">Ativado</span><span class="sxs-lookup"><span data-stu-id="70912-973">On</span></span>       | <span data-ttu-id="70912-974">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-974">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-975">Determina se os caminhos de caractere são exibidos ou não.</span><span class="sxs-lookup"><span data-stu-id="70912-975">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="70912-976">String</span><span class="sxs-lookup"><span data-stu-id="70912-976">String</span></span>   | <span data-ttu-id="70912-977">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70912-977">String.</span></span> <span data-ttu-id="70912-978">O texto a ser renderizar como um caminho de texto.</span><span class="sxs-lookup"><span data-stu-id="70912-978">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="70912-979">Trim</span><span class="sxs-lookup"><span data-stu-id="70912-979">Trim</span></span>     | <span data-ttu-id="70912-980">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-980">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-981">Remove qualquer espaço adicional reservado para ascendentes e descendentes se não for usado.</span><span class="sxs-lookup"><span data-stu-id="70912-981">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="70912-982">Xscale</span><span class="sxs-lookup"><span data-stu-id="70912-982">XScale</span></span>   | <span data-ttu-id="70912-983">[VgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-983">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-984">Use a medida x reta em vez de medir ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="70912-984">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="70912-985">Tipos de dados usados no modelo de objeto VML</span><span class="sxs-lookup"><span data-stu-id="70912-985">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="70912-986">Os tipos de dados a seguir são usados pelo Modelo de Objeto VML.</span><span class="sxs-lookup"><span data-stu-id="70912-986">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="70912-987">Double</span><span class="sxs-lookup"><span data-stu-id="70912-987">Double</span></span>](/windows)
-   [<span data-ttu-id="70912-988">Fixo</span><span class="sxs-lookup"><span data-stu-id="70912-988">Fixed</span></span>](/windows)
-   [<span data-ttu-id="70912-989">Inteiro</span><span class="sxs-lookup"><span data-stu-id="70912-989">Integer</span></span>](/windows)
-   [<span data-ttu-id="70912-990">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="70912-990">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="70912-991">IVgColor</span><span class="sxs-lookup"><span data-stu-id="70912-991">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="70912-992">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="70912-992">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="70912-993">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="70912-993">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="70912-994">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="70912-994">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="70912-995">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="70912-995">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="70912-996">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="70912-996">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="70912-997">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="70912-997">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="70912-998">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="70912-998">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="70912-999">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="70912-999">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="70912-1000">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="70912-1000">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="70912-1001">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="70912-1001">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="70912-1002">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="70912-1002">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="70912-1003">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1003">Length</span></span>](/windows)
-   [<span data-ttu-id="70912-1004">Medida</span><span class="sxs-lookup"><span data-stu-id="70912-1004">Measure</span></span>](/windows)
-   [<span data-ttu-id="70912-1005">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="70912-1005">String</span></span>](/windows)
-   [<span data-ttu-id="70912-1006">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="70912-1006">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="70912-1007">VgRation</span><span class="sxs-lookup"><span data-stu-id="70912-1007">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="70912-1008">VgTriState</span><span class="sxs-lookup"><span data-stu-id="70912-1008">VgTriState</span></span>](/windows)

<span data-ttu-id="70912-1009">**Tipo de dados duplo**</span><span class="sxs-lookup"><span data-stu-id="70912-1009">**Double data type**</span></span>

<span data-ttu-id="70912-1010">Um inteiro de precisão dupla com intervalo de -infinity a infinito.</span><span class="sxs-lookup"><span data-stu-id="70912-1010">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="70912-1011">**Tipo de dados fixo**</span><span class="sxs-lookup"><span data-stu-id="70912-1011">**Fixed data type**</span></span>

<span data-ttu-id="70912-1012">Número de ponto flutuante com intervalo de -32.766,0 a 32.766,0.</span><span class="sxs-lookup"><span data-stu-id="70912-1012">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="70912-1013">**Tipo de dados integer**</span><span class="sxs-lookup"><span data-stu-id="70912-1013">**Integer data type**</span></span>

<span data-ttu-id="70912-1014">Um inteiro com um intervalo de -infinity ao infinito.</span><span class="sxs-lookup"><span data-stu-id="70912-1014">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="70912-1015">**Tipo de dados IVgAdjustments**</span><span class="sxs-lookup"><span data-stu-id="70912-1015">**IVgAdjustments data type**</span></span>

<span data-ttu-id="70912-1016">Coleção de ajustes em uma forma que pode ser usada para alterar as dimensões de uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-1016">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="70912-1017">Os ajustes podem ser usados como espaço reservados temporários ou por qualquer motivo que você usaria variáveis.</span><span class="sxs-lookup"><span data-stu-id="70912-1017">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="70912-1018">Há apenas 8 ajustes na coleção.</span><span class="sxs-lookup"><span data-stu-id="70912-1018">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="70912-1019">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1019">Attribute</span></span> | <span data-ttu-id="70912-1020">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1020">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1021">Exists</span><span class="sxs-lookup"><span data-stu-id="70912-1021">Exists</span></span>     | <span data-ttu-id="70912-1022">[IVgTriState.](msdn-online-vml-vgtristate.md)</span><span class="sxs-lookup"><span data-stu-id="70912-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="70912-1023">Determina se um ajuste especificado existe.</span><span class="sxs-lookup"><span data-stu-id="70912-1023">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="70912-1024">Observe que um índice deve ser usado; ou seja, exists( item ) deve ser usado para recuperar a existência de um item.</span><span class="sxs-lookup"><span data-stu-id="70912-1024">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="70912-1025">Item</span><span class="sxs-lookup"><span data-stu-id="70912-1025">Item</span></span>       | <span data-ttu-id="70912-1026">[Long](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1026">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1027">Matriz de ajustes indexados de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="70912-1027">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="70912-1028">Observe que os ajustes podem ser especificados com moderação; ou seja, os valores de matriz intermediários nem sempre podem ser preenchidos.</span><span class="sxs-lookup"><span data-stu-id="70912-1028">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="70912-1029">Por exemplo, os itens 1, 3 e 5 podem ter valores para um comprimento de 3, com item(0), item(2) e item(4) especificados.</span><span class="sxs-lookup"><span data-stu-id="70912-1029">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="70912-1030">Para ver se existe um item, use o atributo Exists.</span><span class="sxs-lookup"><span data-stu-id="70912-1030">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="70912-1031">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1031">Length</span></span>     | <span data-ttu-id="70912-1032">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1032">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1033">Número de ajustes.</span><span class="sxs-lookup"><span data-stu-id="70912-1033">Number of adjustments.</span></span> <span data-ttu-id="70912-1034">Não pode ser maior que 8.</span><span class="sxs-lookup"><span data-stu-id="70912-1034">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="70912-1035">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1035">Value</span></span>      | <span data-ttu-id="70912-1036">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1036">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1037">Representação de texto de valores numéricos, com vírgulas entre cada número.</span><span class="sxs-lookup"><span data-stu-id="70912-1037">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="70912-1038">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="70912-1038">**IVgColor**</span></span>

<span data-ttu-id="70912-1039">Especifica uma cor.</span><span class="sxs-lookup"><span data-stu-id="70912-1039">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-1040">Atributos</span><span class="sxs-lookup"><span data-stu-id="70912-1040">Attributes</span></span></th>
<th><span data-ttu-id="70912-1041">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1041">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1042">RGB</span><span class="sxs-lookup"><span data-stu-id="70912-1042">RGB</span></span></td>
<td><span data-ttu-id="70912-1043"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="70912-1043"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="70912-1044">Valor RGB (Long) da cor.</span><span class="sxs-lookup"><span data-stu-id="70912-1044">RGB value (Long) of the color.</span></span> <span data-ttu-id="70912-1045">Válido somente se Type for RGB.</span><span class="sxs-lookup"><span data-stu-id="70912-1045">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1046">R</span><span class="sxs-lookup"><span data-stu-id="70912-1046">R</span></span></td>
<td><span data-ttu-id="70912-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="70912-1048">Componente vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="70912-1048">Red component of the color.</span></span> <span data-ttu-id="70912-1049">Pode variar entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="70912-1049">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1050">G</span><span class="sxs-lookup"><span data-stu-id="70912-1050">G</span></span></td>
<td><span data-ttu-id="70912-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="70912-1052">Componente verde da cor.</span><span class="sxs-lookup"><span data-stu-id="70912-1052">Green component of the color.</span></span> <span data-ttu-id="70912-1053">Pode variar entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="70912-1053">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1054">B</span><span class="sxs-lookup"><span data-stu-id="70912-1054">B</span></span></td>
<td><span data-ttu-id="70912-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="70912-1056">Componente azul da cor.</span><span class="sxs-lookup"><span data-stu-id="70912-1056">Blue component of the color.</span></span> <span data-ttu-id="70912-1057">Pode variar entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="70912-1057">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1058">String</span><span class="sxs-lookup"><span data-stu-id="70912-1058">String</span></span></td>
<td><span data-ttu-id="70912-1059"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1059"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="70912-1060">Representação de texto da cor.</span><span class="sxs-lookup"><span data-stu-id="70912-1060">Text representation of the color.</span></span> <span data-ttu-id="70912-1061">Há suporte para os seguintes tipos de cores nomeados:</span><span class="sxs-lookup"><span data-stu-id="70912-1061">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="70912-1062">Preto (#000000)</span><span class="sxs-lookup"><span data-stu-id="70912-1062">Black (#000000)</span></span></li>
<li><span data-ttu-id="70912-1063">Prata (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="70912-1063">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="70912-1064">Cinza (#808080)</span><span class="sxs-lookup"><span data-stu-id="70912-1064">Gray (#808080)</span></span></li>
<li><span data-ttu-id="70912-1065">Branco (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="70912-1065">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="70912-1066">Mário (#800000)</span><span class="sxs-lookup"><span data-stu-id="70912-1066">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="70912-1067">Vermelho (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="70912-1067">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="70912-1068">Roxo (#800080)</span><span class="sxs-lookup"><span data-stu-id="70912-1068">Purple (#800080)</span></span></li>
<li><span data-ttu-id="70912-1069">Fuchsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="70912-1069">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="70912-1070">Verde (#008000)</span><span class="sxs-lookup"><span data-stu-id="70912-1070">Green (#008000)</span></span></li>
<li><span data-ttu-id="70912-1071">Calca (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="70912-1071">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="70912-1072">Verde-verde (#808000)</span><span class="sxs-lookup"><span data-stu-id="70912-1072">Olive (#808000)</span></span></li>
<li><span data-ttu-id="70912-1073">Amarelo (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="70912-1073">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="70912-1074">(#000080)</span><span class="sxs-lookup"><span data-stu-id="70912-1074">Navy (#000080)</span></span></li>
<li><span data-ttu-id="70912-1075">Azul (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="70912-1075">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="70912-1076">Teal (#008080)</span><span class="sxs-lookup"><span data-stu-id="70912-1076">Teal (#008080)</span></span></li>
<li><span data-ttu-id="70912-1077">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="70912-1077">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1078">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-1078">Type</span></span></td>
<td><span data-ttu-id="70912-1079"><strong>VgColorType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1079"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="70912-1080">Tipo de cor.</span><span class="sxs-lookup"><span data-stu-id="70912-1080">Type of color.</span></span> <span data-ttu-id="70912-1081">Um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="70912-1081">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="70912-1082">Mixed</span><span class="sxs-lookup"><span data-stu-id="70912-1082">Mixed</span></span></li>
<li><span data-ttu-id="70912-1083">nomeado</span><span class="sxs-lookup"><span data-stu-id="70912-1083">Named</span></span></li>
<li><span data-ttu-id="70912-1084">RGB</span><span class="sxs-lookup"><span data-stu-id="70912-1084">RGB</span></span></li>
<li><span data-ttu-id="70912-1085">Esquema</span><span class="sxs-lookup"><span data-stu-id="70912-1085">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70912-1086">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="70912-1086">**IVgEquation**</span></span>

<span data-ttu-id="70912-1087">Equações usadas para fórmulas.</span><span class="sxs-lookup"><span data-stu-id="70912-1087">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1088">Operação</span><span class="sxs-lookup"><span data-stu-id="70912-1088">Operation</span></span></td>
<td><span data-ttu-id="70912-1089"><strong>VgEquationOperationType</strong> Nome da operação a ser realizada nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="70912-1089"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="70912-1090">As seguintes operações podem ser usadas em uma equação:</span><span class="sxs-lookup"><span data-stu-id="70912-1090">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-1091">Operação</span><span class="sxs-lookup"><span data-stu-id="70912-1091">Operation</span></span></th>
<th><span data-ttu-id="70912-1092">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1092">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1093">Abs</span><span class="sxs-lookup"><span data-stu-id="70912-1093">Abs</span></span></td>
<td><span data-ttu-id="70912-1094">Valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="70912-1094">Absolute value.</span></span> <br/> <span data-ttu-id="70912-1095"><strong>abs</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="70912-1095"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1096">Atan2</span><span class="sxs-lookup"><span data-stu-id="70912-1096">Atan2</span></span></td>
<td><span data-ttu-id="70912-1097">Aritmética polar – resulta em unidades fd (graus multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="70912-1097">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="70912-1098"><strong>atan2</strong>(p1,v)</span><span class="sxs-lookup"><span data-stu-id="70912-1098"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1099">Cos</span><span class="sxs-lookup"><span data-stu-id="70912-1099">Cos</span></span></td>
<td><span data-ttu-id="70912-1100">Cosseno, argumento em unidades fd (graus multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="70912-1100">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="70912-1101">v \* <strong>cos</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="70912-1101">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1102">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="70912-1102">Cosatan2</span></span></td>
<td><span data-ttu-id="70912-1103">Preserva a precisão total no cálculo intermediário.</span><span class="sxs-lookup"><span data-stu-id="70912-1103">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="70912-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1105">Ellipse</span><span class="sxs-lookup"><span data-stu-id="70912-1105">Ellipse</span></span></td>
<td><span data-ttu-id="70912-1106">Ellipse</span><span class="sxs-lookup"><span data-stu-id="70912-1106">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1107">If</span><span class="sxs-lookup"><span data-stu-id="70912-1107">If</span></span></td>
<td><span data-ttu-id="70912-1108">Teste if Condition.</span><span class="sxs-lookup"><span data-stu-id="70912-1108">If Condition test.</span></span> <span data-ttu-id="70912-1109">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1109">v > 0 <strong>?</strong></span></span> <span data-ttu-id="70912-1110">p1 : p2</span><span class="sxs-lookup"><span data-stu-id="70912-1110">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1111">Max</span><span class="sxs-lookup"><span data-stu-id="70912-1111">Max</span></span></td>
<td><span data-ttu-id="70912-1112">O maior de dois valores.</span><span class="sxs-lookup"><span data-stu-id="70912-1112">The greater of two values.</span></span> <br/> <span data-ttu-id="70912-1113"><strong>max</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="70912-1113"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1114">Mid</span><span class="sxs-lookup"><span data-stu-id="70912-1114">Mid</span></span></td>
<td><span data-ttu-id="70912-1115">Média ( v + p1)/2</span><span class="sxs-lookup"><span data-stu-id="70912-1115">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1116">Min</span><span class="sxs-lookup"><span data-stu-id="70912-1116">Min</span></span></td>
<td><span data-ttu-id="70912-1117">O menor de dois valores.</span><span class="sxs-lookup"><span data-stu-id="70912-1117">The lesser of two values.</span></span> <span data-ttu-id="70912-1118"><strong>min</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="70912-1118"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1119">Mod</span><span class="sxs-lookup"><span data-stu-id="70912-1119">Mod</span></span></td>
<td><span data-ttu-id="70912-1120">Módulo.</span><span class="sxs-lookup"><span data-stu-id="70912-1120">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1121">Produto</span><span class="sxs-lookup"><span data-stu-id="70912-1121">Product</span></span></td>
<td><span data-ttu-id="70912-1122">Usado para multiplicação e divisão.</span><span class="sxs-lookup"><span data-stu-id="70912-1122">Used for multiplication and division.</span></span> <span data-ttu-id="70912-1123">v \* p1 / p2</span><span class="sxs-lookup"><span data-stu-id="70912-1123">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1124">Sin</span><span class="sxs-lookup"><span data-stu-id="70912-1124">Sin</span></span></td>
<td><span data-ttu-id="70912-1125">Seno, argumento em unidades fd (graus multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="70912-1125">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="70912-1126">v \* <strong>sin</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="70912-1126">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1127">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="70912-1127">Sinatan2</span></span></td>
<td><span data-ttu-id="70912-1128">Preserva a precisão total no cálculo intermediário.</span><span class="sxs-lookup"><span data-stu-id="70912-1128">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="70912-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span><span class="sxs-lookup"><span data-stu-id="70912-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1130">Sqrt</span><span class="sxs-lookup"><span data-stu-id="70912-1130">Sqrt</span></span></td>
<td><span data-ttu-id="70912-1131">O resultado é positivo e é a volta para baixo.</span><span class="sxs-lookup"><span data-stu-id="70912-1131">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="70912-1132"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="70912-1132"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1133">Somar</span><span class="sxs-lookup"><span data-stu-id="70912-1133">Sum</span></span></td>
<td><span data-ttu-id="70912-1134">Usado para adição e subtração.</span><span class="sxs-lookup"><span data-stu-id="70912-1134">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="70912-1135">v + p1 p2</span><span class="sxs-lookup"><span data-stu-id="70912-1135">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1136">Sumangle</span><span class="sxs-lookup"><span data-stu-id="70912-1136">Sumangle</span></span></td>
<td><span data-ttu-id="70912-1137">Ângulo existente (dimensionado em 65536), em que p1 e p2 estão em graus.</span><span class="sxs-lookup"><span data-stu-id="70912-1137">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="70912-1138">v + p1 \* 65536 + p2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="70912-1138">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1139">Tan</span><span class="sxs-lookup"><span data-stu-id="70912-1139">Tan</span></span></td>
<td><span data-ttu-id="70912-1140">Tangente, o argumento está em unidades fd (graus multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="70912-1140">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="70912-1141">v \* tan( p1 )</span><span class="sxs-lookup"><span data-stu-id="70912-1141">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1142">Val</span><span class="sxs-lookup"><span data-stu-id="70912-1142">Val</span></span></td>
<td><span data-ttu-id="70912-1143">Define um valor de guia de algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="70912-1143">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1144">Param1</span><span class="sxs-lookup"><span data-stu-id="70912-1144">Param1</span></span></td>
<td><span data-ttu-id="70912-1145"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="70912-1145"><strong>Integer</strong>.</span></span> <span data-ttu-id="70912-1146">O primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70912-1146">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1147">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="70912-1147">Paramtype1</span></span></td>
<td><span data-ttu-id="70912-1148"><strong>VgFormulaParamType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1148"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="70912-1149">O tipo do primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70912-1149">The type of the first parameter.</span></span> <span data-ttu-id="70912-1150">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="70912-1150">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-1151">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-1151">Type</span></span></th>
<th><span data-ttu-id="70912-1152">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1153">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1153">Value</span></span></td>
<td><span data-ttu-id="70912-1154">O parâmetro é um valor simples.</span><span class="sxs-lookup"><span data-stu-id="70912-1154">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1155">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="70912-1155">AdjustmentReference</span></span></td>
<td><span data-ttu-id="70912-1156">O parâmetro é uma referência a um ajuste.</span><span class="sxs-lookup"><span data-stu-id="70912-1156">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="70912-1157">Por exemplo, se o primeiro parâmetro for 1, o valor do primeiro ajuste será usado.</span><span class="sxs-lookup"><span data-stu-id="70912-1157">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1158">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="70912-1158">FormulaReference</span></span></td>
<td><span data-ttu-id="70912-1159">O parâmetro é o resultado de uma referência ao resultado de uma fórmula anterior.</span><span class="sxs-lookup"><span data-stu-id="70912-1159">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="70912-1160">Por exemplo, se o primeiro parâmetro for 2, o resultado da fórmula 2 será usado.</span><span class="sxs-lookup"><span data-stu-id="70912-1160">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1161">Param2</span><span class="sxs-lookup"><span data-stu-id="70912-1161">Param2</span></span></td>
<td><span data-ttu-id="70912-1162"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="70912-1162"><strong>Integer</strong>.</span></span> <span data-ttu-id="70912-1163">O segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70912-1163">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1164">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="70912-1164">Paramtype2</span></span></td>
<td><span data-ttu-id="70912-1165"><strong>VgFormulaParamType</strong> O tipo do parâmetro 2.</span><span class="sxs-lookup"><span data-stu-id="70912-1165"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1166">Val</span><span class="sxs-lookup"><span data-stu-id="70912-1166">Val</span></span></td>
<td><span data-ttu-id="70912-1167"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="70912-1167"><strong>Integer</strong>.</span></span> <span data-ttu-id="70912-1168">O resultado.</span><span class="sxs-lookup"><span data-stu-id="70912-1168">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1169">Valtype2</span><span class="sxs-lookup"><span data-stu-id="70912-1169">Valtype2</span></span></td>
<td><span data-ttu-id="70912-1170"><strong>VgFormulaParamType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1170"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="70912-1171">O tipo do resultado.</span><span class="sxs-lookup"><span data-stu-id="70912-1171">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70912-1172">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="70912-1172">**IVgFixedRectangle**</span></span>

<span data-ttu-id="70912-1173">Especifica um retângulo fixo.</span><span class="sxs-lookup"><span data-stu-id="70912-1173">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="70912-1174">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1174">Attribute</span></span> | <span data-ttu-id="70912-1175">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1175">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1176">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1176">Value</span></span>      | <span data-ttu-id="70912-1177">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1177">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1178">Valor de texto que especifica o caminho.</span><span class="sxs-lookup"><span data-stu-id="70912-1178">Text value specifying the path.</span></span>         |
| <span data-ttu-id="70912-1179">Esquerda</span><span class="sxs-lookup"><span data-stu-id="70912-1179">Left</span></span>       | <span data-ttu-id="70912-1180">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1180">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1181">Coordenada mais à esquerda do retângulo.</span><span class="sxs-lookup"><span data-stu-id="70912-1181">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="70912-1182">Parte superior</span><span class="sxs-lookup"><span data-stu-id="70912-1182">Top</span></span>        | <span data-ttu-id="70912-1183">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1183">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1184">Coordenada superior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="70912-1184">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="70912-1185">Direita</span><span class="sxs-lookup"><span data-stu-id="70912-1185">Right</span></span>      | <span data-ttu-id="70912-1186">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1186">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1187">Coordenada mais à direita do retângulo.</span><span class="sxs-lookup"><span data-stu-id="70912-1187">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="70912-1188">Menor</span><span class="sxs-lookup"><span data-stu-id="70912-1188">Bottom</span></span>     | <span data-ttu-id="70912-1189">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1189">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1190">Coordenada mais inferior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="70912-1190">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="70912-1191">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="70912-1191">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="70912-1192">Matriz de retângulos fixos.</span><span class="sxs-lookup"><span data-stu-id="70912-1192">Array of fixed rectangles.</span></span>



| <span data-ttu-id="70912-1193">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1193">Attribute</span></span> | <span data-ttu-id="70912-1194">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1194">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1195">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1195">Value</span></span>      | <span data-ttu-id="70912-1196">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1196">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1197">Representação de texto da matriz.</span><span class="sxs-lookup"><span data-stu-id="70912-1197">Text representation of array.</span></span>                           |
| <span data-ttu-id="70912-1198">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1198">Length</span></span>     | <span data-ttu-id="70912-1199">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1199">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1200">Número de retângulos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="70912-1200">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="70912-1201">Item</span><span class="sxs-lookup"><span data-stu-id="70912-1201">Item</span></span>       | <span data-ttu-id="70912-1202">[IVgFixedRectangle.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1203">O objeto retângulo no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="70912-1203">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="70912-1204">**Tipo de dados IVgFormula**</span><span class="sxs-lookup"><span data-stu-id="70912-1204">**IVgFormula** data type</span></span>

<span data-ttu-id="70912-1205">Definições para fórmulas que podem variar o caminho de uma forma ou ser usadas para outras finalidades de cálculo.</span><span class="sxs-lookup"><span data-stu-id="70912-1205">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="70912-1206">As fórmulas podem ser baseadas no **atributo Adj** de uma forma, que pode mudar.</span><span class="sxs-lookup"><span data-stu-id="70912-1206">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="70912-1207">As fórmulas também podem referenciar outras fórmulas.</span><span class="sxs-lookup"><span data-stu-id="70912-1207">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="70912-1208">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1208">Attribute</span></span>| <span data-ttu-id="70912-1209">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1209">Description</span></span>                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1210">Eqn</span><span class="sxs-lookup"><span data-stu-id="70912-1210">Eqn</span></span>        | <span data-ttu-id="70912-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1212">Cada fórmula define um único valor como o resultado da avaliação da expressão.</span><span class="sxs-lookup"><span data-stu-id="70912-1212">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="70912-1213">A expressão é definida por esse atributo e tem a forma geral de uma operação seguida por até três argumentos, que podem ser valores de ajuste (por exemplo, 2), os resultados de fórmulas anteriores (por exemplo, ), números fixos ou valores \# @2 predefinidos.</span><span class="sxs-lookup"><span data-stu-id="70912-1213">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="70912-1214">**Tipo de dados IVgFormulas**</span><span class="sxs-lookup"><span data-stu-id="70912-1214">**IVgFormulas data type**</span></span>

<span data-ttu-id="70912-1215">Uma coleção de objetos de fórmula.</span><span class="sxs-lookup"><span data-stu-id="70912-1215">A collection of formula objects.</span></span>



| <span data-ttu-id="70912-1216">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1216">Attribute</span></span> | <span data-ttu-id="70912-1217">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1217">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1218">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1218">Length</span></span>     | <span data-ttu-id="70912-1219">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1219">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1220">Número de objetos de fórmula na coleção.</span><span class="sxs-lookup"><span data-stu-id="70912-1220">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="70912-1221">Item</span><span class="sxs-lookup"><span data-stu-id="70912-1221">Item</span></span>       | <span data-ttu-id="70912-1222">[IVgFormula.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="70912-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1223">Uma fórmula específica.</span><span class="sxs-lookup"><span data-stu-id="70912-1223">A specific formula.</span></span> <span data-ttu-id="70912-1224">Observe que a matriz de fórmulas pode ser herdada para o tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="70912-1224">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="70912-1225">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="70912-1225">**IVgGradientColorArray**</span></span>

<span data-ttu-id="70912-1226">Uma matriz de cores que definem um gradiente (intervalo de cores mesclados).</span><span class="sxs-lookup"><span data-stu-id="70912-1226">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="70912-1227">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1227">Attribute</span></span> | <span data-ttu-id="70912-1228">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1228">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1229">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1229">Value</span></span>      | <span data-ttu-id="70912-1230">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1230">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1231">Especifica a matriz de cores; por exemplo, "vermelho .2; verde .4; preto .7"</span><span class="sxs-lookup"><span data-stu-id="70912-1231">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="70912-1232">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1232">Length</span></span>     | <span data-ttu-id="70912-1233">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1233">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1234">Número de cores na matriz.</span><span class="sxs-lookup"><span data-stu-id="70912-1234">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="70912-1235">Método</span><span class="sxs-lookup"><span data-stu-id="70912-1235">Method</span></span>     | <span data-ttu-id="70912-1236">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1236">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1237">AddColor</span><span class="sxs-lookup"><span data-stu-id="70912-1237">AddColor</span></span>    | <span data-ttu-id="70912-1238">[VgAção .](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="70912-1239">Adiciona nova cor ao ponto de extremidade especificado por fração.</span><span class="sxs-lookup"><span data-stu-id="70912-1239">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="70912-1240">A nova cor é branca por padrão e é o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="70912-1240">The new color is white by default and is the return value.</span></span> <span data-ttu-id="70912-1241">A cor pode ser alterada por referência.</span><span class="sxs-lookup"><span data-stu-id="70912-1241">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="70912-1242">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="70912-1242">RemoveColor</span></span> | <span data-ttu-id="70912-1243">[VgAção .](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="70912-1244">Remove uma cor no ponto de extremidade especificado por fração.</span><span class="sxs-lookup"><span data-stu-id="70912-1244">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="70912-1245">Observação: se 0.0 ou 1.0 não existir, ele será implícito e a cor branca será usada nesse ponto.</span><span class="sxs-lookup"><span data-stu-id="70912-1245">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="70912-1246">**Tipo de dados IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="70912-1246">**IVgPoints datatype**</span></span>

<span data-ttu-id="70912-1247">Matriz de pontos que definem uma forma.</span><span class="sxs-lookup"><span data-stu-id="70912-1247">Array of points that define a shape.</span></span>



| <span data-ttu-id="70912-1248">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1248">Attribute</span></span> | <span data-ttu-id="70912-1249">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1249">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="70912-1250">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1250">Value</span></span>      | <span data-ttu-id="70912-1251">[Cadeia de caracteres](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1251">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1252">Representação de texto da matriz.</span><span class="sxs-lookup"><span data-stu-id="70912-1252">Text representation of array.</span></span>           |
| <span data-ttu-id="70912-1253">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1253">Length</span></span>     | <span data-ttu-id="70912-1254">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1254">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="70912-1255">Número de pontos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="70912-1255">Number of points in this array.</span></span>        |
| <span data-ttu-id="70912-1256">Item</span><span class="sxs-lookup"><span data-stu-id="70912-1256">Item</span></span>       | <span data-ttu-id="70912-1257">[IVgVector2D.](msdn-online-vml-ivgvector2d-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="70912-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="70912-1258">O ponto no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="70912-1258">The point at the specified index.</span></span> |



 

<span data-ttu-id="70912-1259">**Tipo de dados IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="70912-1259">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="70912-1260">Uma matriz usada para distorcer formas, uma matriz de transformação de perspectiva no formato , "*sxx, sxy, syx, syy, px,py* " \[ *s* =scale, *p* =perspective \] .</span><span class="sxs-lookup"><span data-stu-id="70912-1260">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="70912-1261">Se offset estiver em unidades absolutas, *px,py* estão em unidades emu ^-1; caso contrário, eles serão uma fração inversa do tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-1261">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="70912-1262">Atributo</span><span class="sxs-lookup"><span data-stu-id="70912-1262">Attribute</span></span>   | <span data-ttu-id="70912-1263">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1263">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="70912-1264">XtoX</span><span class="sxs-lookup"><span data-stu-id="70912-1264">XtoX</span></span>         | <span data-ttu-id="70912-1265">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1265">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="70912-1266">YtoX</span><span class="sxs-lookup"><span data-stu-id="70912-1266">YtoX</span></span>         | <span data-ttu-id="70912-1267">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1267">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="70912-1268">XtoY</span><span class="sxs-lookup"><span data-stu-id="70912-1268">XtoY</span></span>         | <span data-ttu-id="70912-1269">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1269">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="70912-1270">AaA</span><span class="sxs-lookup"><span data-stu-id="70912-1270">YtoY</span></span>         | <span data-ttu-id="70912-1271">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1271">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="70912-1272">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="70912-1272">PerspectiveX</span></span> | <span data-ttu-id="70912-1273">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1273">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="70912-1274">PerspectiveY</span><span class="sxs-lookup"><span data-stu-id="70912-1274">PerspectiveY</span></span> | <span data-ttu-id="70912-1275">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="70912-1275">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="70912-1276">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="70912-1276">**IVgSkewOffset**</span></span>

<span data-ttu-id="70912-1277">Especifica o deslocamento da distorção.</span><span class="sxs-lookup"><span data-stu-id="70912-1277">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-1278">Atributos</span><span class="sxs-lookup"><span data-stu-id="70912-1278">Attributes</span></span></th>
<th><span data-ttu-id="70912-1279">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1279">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1280">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1280">Value</span></span></td>
<td><span data-ttu-id="70912-1281"><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1281"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="70912-1282">Representação de texto do deslocamento.</span><span class="sxs-lookup"><span data-stu-id="70912-1282">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1283">X</span><span class="sxs-lookup"><span data-stu-id="70912-1283">X</span></span></td>
<td><span data-ttu-id="70912-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="70912-1285">Componente X.</span><span class="sxs-lookup"><span data-stu-id="70912-1285">X component.</span></span> <span data-ttu-id="70912-1286">Percentual ou medida.</span><span class="sxs-lookup"><span data-stu-id="70912-1286">Percentage or measure.</span></span> <span data-ttu-id="70912-1287">Se nenhuma unidade, o tipo ShapeRelative será implícito; caso contrário, o tipo Absoluto está implícito.</span><span class="sxs-lookup"><span data-stu-id="70912-1287">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1288">Y</span><span class="sxs-lookup"><span data-stu-id="70912-1288">Y</span></span></td>
<td><span data-ttu-id="70912-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="70912-1290">Componente Y.</span><span class="sxs-lookup"><span data-stu-id="70912-1290">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1291">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-1291">Type</span></span></td>
<td><span data-ttu-id="70912-1292"><strong>VgSkewTransformType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1292"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="70912-1293">Especifica o tipo de transformação.</span><span class="sxs-lookup"><span data-stu-id="70912-1293">Specifies the type of transformation.</span></span> <span data-ttu-id="70912-1294">Os valores válidos são pontos inteiros que variam entre -infinity e infinity.</span><span class="sxs-lookup"><span data-stu-id="70912-1294">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-1295">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-1295">Type</span></span></th>
<th><span data-ttu-id="70912-1296">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1296">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1297">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="70912-1297">ShapeRelative</span></span></td>
<td><span data-ttu-id="70912-1298">Os valores do deslocamento são percentuais (taxas) do tamanho da forma original; Por exemplo, um valor de 0,5 significa um deslocamento pela metade do tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="70912-1298">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1299">Absoluto</span><span class="sxs-lookup"><span data-stu-id="70912-1299">Absolute</span></span></td>
<td><span data-ttu-id="70912-1300">Os valores são unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="70912-1300">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70912-1301">**Tipo de dados IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="70912-1301">**IVgVector2D data type**</span></span>

<span data-ttu-id="70912-1302">Especifica um vetor bidimensional que consiste em dois **números Double.**</span><span class="sxs-lookup"><span data-stu-id="70912-1302">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70912-1303">Atributos</span><span class="sxs-lookup"><span data-stu-id="70912-1303">Attributes</span></span></th>
<th><span data-ttu-id="70912-1304">Descrição</span><span class="sxs-lookup"><span data-stu-id="70912-1304">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1305">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1305">Value</span></span></td>
<td><span data-ttu-id="70912-1306"><strong>Cadeia de caracteres</strong>.</span><span class="sxs-lookup"><span data-stu-id="70912-1306"><strong>String</strong>.</span></span> <span data-ttu-id="70912-1307">Representação de texto de ambos os números vetoriais separados por um espaço.</span><span class="sxs-lookup"><span data-stu-id="70912-1307">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1308">X</span><span class="sxs-lookup"><span data-stu-id="70912-1308">X</span></span></td>
<td><span data-ttu-id="70912-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="70912-1310">Componente X desse vetor.</span><span class="sxs-lookup"><span data-stu-id="70912-1310">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1311">Y</span><span class="sxs-lookup"><span data-stu-id="70912-1311">Y</span></span></td>
<td><span data-ttu-id="70912-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="70912-1313">Componente Y desse vetor.</span><span class="sxs-lookup"><span data-stu-id="70912-1313">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1314">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-1314">Type</span></span></td>
<td><span data-ttu-id="70912-1315"><strong>VgVectorType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1315"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="70912-1316">Unidades esperadas para esse vetor.</span><span class="sxs-lookup"><span data-stu-id="70912-1316">Expected units for this vector.</span></span> <span data-ttu-id="70912-1317">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-1317">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-1318">Medida</span><span class="sxs-lookup"><span data-stu-id="70912-1318">Measure</span></span></li>
<li><span data-ttu-id="70912-1319">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1319">Length</span></span></li>
<li><span data-ttu-id="70912-1320">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="70912-1320">AngleInDegrees</span></span></li>
<li><span data-ttu-id="70912-1321">Fraction</span><span class="sxs-lookup"><span data-stu-id="70912-1321">Fraction</span></span></li>
<li><span data-ttu-id="70912-1322">Número percentual inteiro</span><span class="sxs-lookup"><span data-stu-id="70912-1322">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70912-1323">**Tipo de dados IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="70912-1323">**IVgVector3D data type**</span></span>

<span data-ttu-id="70912-1324">Especifica um vetor tridimensional que consiste em três **números Double.**</span><span class="sxs-lookup"><span data-stu-id="70912-1324">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70912-1325">Valor</span><span class="sxs-lookup"><span data-stu-id="70912-1325">Value</span></span></td>
<td><span data-ttu-id="70912-1326"><strong>Cadeia de caracteres</strong>.</span><span class="sxs-lookup"><span data-stu-id="70912-1326"><strong>String</strong>.</span></span> <span data-ttu-id="70912-1327">Representação de texto de três números vetoriais separados por um espaço.</span><span class="sxs-lookup"><span data-stu-id="70912-1327">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1328">X</span><span class="sxs-lookup"><span data-stu-id="70912-1328">X</span></span></td>
<td><span data-ttu-id="70912-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="70912-1330">Componente X desse vetor.</span><span class="sxs-lookup"><span data-stu-id="70912-1330">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1331">Y</span><span class="sxs-lookup"><span data-stu-id="70912-1331">Y</span></span></td>
<td><span data-ttu-id="70912-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="70912-1333">Componente Y desse vetor.</span><span class="sxs-lookup"><span data-stu-id="70912-1333">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70912-1334">Z</span><span class="sxs-lookup"><span data-stu-id="70912-1334">Z</span></span></td>
<td><span data-ttu-id="70912-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="70912-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="70912-1336">Componente Z desse vetor.</span><span class="sxs-lookup"><span data-stu-id="70912-1336">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70912-1337">Tipo</span><span class="sxs-lookup"><span data-stu-id="70912-1337">Type</span></span></td>
<td><span data-ttu-id="70912-1338"><strong>VgVectorType.</strong></span><span class="sxs-lookup"><span data-stu-id="70912-1338"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="70912-1339">Unidades esperadas para esse vetor.</span><span class="sxs-lookup"><span data-stu-id="70912-1339">Expected units for this vector.</span></span> <span data-ttu-id="70912-1340">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="70912-1340">Values are:</span></span>
<ul>
<li><span data-ttu-id="70912-1341">Medida</span><span class="sxs-lookup"><span data-stu-id="70912-1341">Measure</span></span></li>
<li><span data-ttu-id="70912-1342">Comprimento</span><span class="sxs-lookup"><span data-stu-id="70912-1342">Length</span></span></li>
<li><span data-ttu-id="70912-1343">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="70912-1343">AngleInDegrees</span></span></li>
<li><span data-ttu-id="70912-1344">Fraction</span><span class="sxs-lookup"><span data-stu-id="70912-1344">Fraction</span></span></li>
<li><span data-ttu-id="70912-1345">Número</span><span class="sxs-lookup"><span data-stu-id="70912-1345">Number</span></span></li>
<li><span data-ttu-id="70912-1346">Percentual</span><span class="sxs-lookup"><span data-stu-id="70912-1346">Percentage</span></span></li>
<li><span data-ttu-id="70912-1347">Integer</span><span class="sxs-lookup"><span data-stu-id="70912-1347">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70912-1348">**Tipo de dados length**</span><span class="sxs-lookup"><span data-stu-id="70912-1348">**Length data type**</span></span>

<span data-ttu-id="70912-1349">Um número de ponto flutuante com um intervalo de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="70912-1349">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="70912-1350">**Medir tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="70912-1350">**Measure data type**</span></span>

<span data-ttu-id="70912-1351">Um número de ponto flutuante de -infinity ao infinito.</span><span class="sxs-lookup"><span data-stu-id="70912-1351">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="70912-1352">**Tipo de dados de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70912-1352">**String data type**</span></span>

<span data-ttu-id="70912-1353">Dados de caractere de qualquer comprimento.</span><span class="sxs-lookup"><span data-stu-id="70912-1353">Character data of any length.</span></span>

<span data-ttu-id="70912-1354">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="70912-1354">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="70912-1355">Modo de renderização para preto e branco.</span><span class="sxs-lookup"><span data-stu-id="70912-1355">Rendering mode for black and white.</span></span> <span data-ttu-id="70912-1356">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="70912-1356">Possible values are:</span></span>

-   <span data-ttu-id="70912-1357">**Cor**</span><span class="sxs-lookup"><span data-stu-id="70912-1357">**Color**</span></span>
-   <span data-ttu-id="70912-1358">**Auto**</span><span class="sxs-lookup"><span data-stu-id="70912-1358">**Auto**</span></span>
-   <span data-ttu-id="70912-1359">**Cinza**</span><span class="sxs-lookup"><span data-stu-id="70912-1359">**GrayScale**</span></span>
-   <span data-ttu-id="70912-1360">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="70912-1360">**LightGrayScale**</span></span>
-   <span data-ttu-id="70912-1361">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="70912-1361">**InverseGray**</span></span>
-   <span data-ttu-id="70912-1362">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="70912-1362">**GrayOutline**</span></span>
-   <span data-ttu-id="70912-1363">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="70912-1363">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="70912-1364">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="70912-1364">**HighContrast**</span></span>
-   <span data-ttu-id="70912-1365">**Preto**</span><span class="sxs-lookup"><span data-stu-id="70912-1365">**Black**</span></span>
-   <span data-ttu-id="70912-1366">**Branca**</span><span class="sxs-lookup"><span data-stu-id="70912-1366">**White**</span></span>
-   <span data-ttu-id="70912-1367">**Não redesenhado**</span><span class="sxs-lookup"><span data-stu-id="70912-1367">**Undrawn**</span></span>

<span data-ttu-id="70912-1368">**Tipo de dados VgAção**</span><span class="sxs-lookup"><span data-stu-id="70912-1368">**VgFraction data type**</span></span>

<span data-ttu-id="70912-1369">Número de ponto flutuante com intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="70912-1369">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="70912-1370">Frações também podem ser especificadas como um percentual; por exemplo, "50%".</span><span class="sxs-lookup"><span data-stu-id="70912-1370">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="70912-1371">**Tipo de dados VgTriState**</span><span class="sxs-lookup"><span data-stu-id="70912-1371">**VgTriState datatype**</span></span>

<span data-ttu-id="70912-1372">Enumeração usada para valores que podem ser um dos três estados:</span><span class="sxs-lookup"><span data-stu-id="70912-1372">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="70912-1373">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="70912-1373">**TRUE**</span></span>
-   <span data-ttu-id="70912-1374">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="70912-1374">**FALSE**</span></span>
-   <span data-ttu-id="70912-1375">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="70912-1375">**MIXED**</span></span>