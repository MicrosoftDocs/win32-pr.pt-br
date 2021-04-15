---
title: Atributo adj
description: Atributo adj
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760801"
---
# <a name="adj-attribute"></a><span data-ttu-id="bf81c-103">Atributo adj</span><span class="sxs-lookup"><span data-stu-id="bf81c-103">Adj Attribute</span></span>

<span data-ttu-id="bf81c-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bf81c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bf81c-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="bf81c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bf81c-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="bf81c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bf81c-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="bf81c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bf81c-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bf81c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bf81c-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bf81c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bf81c-110">Especifica um valor de ajuste usado para definir valores para uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="bf81c-110">Specifies an adjustment value used to define values for a formula.</span></span> <span data-ttu-id="bf81c-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bf81c-111">Read/write.</span></span> <span data-ttu-id="bf81c-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="bf81c-112">**String**.</span></span>

<span data-ttu-id="bf81c-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="bf81c-113">**Applies To**</span></span>

[<span data-ttu-id="bf81c-114">Forma</span><span class="sxs-lookup"><span data-stu-id="bf81c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="bf81c-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="bf81c-115">**Tag Syntax**</span></span>

<span data-ttu-id="bf81c-116"><v: *Element* adj = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="bf81c-116"><v: *element* adj=" *expression* "></span></span>

<span data-ttu-id="bf81c-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="bf81c-117">**Script Syntax**</span></span>

<span data-ttu-id="bf81c-118">*Element* . adj = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="bf81c-118">*element* .adj="*expression*"</span></span>

<span data-ttu-id="bf81c-119">*expressão* = de *elemento*. adj</span><span class="sxs-lookup"><span data-stu-id="bf81c-119">*expression*=*element*.adj</span></span>

<span data-ttu-id="bf81c-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="bf81c-120">**Remarks**</span></span>

<span data-ttu-id="bf81c-121">O **adj** é usado para fornecer pontos ajustáveis para uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="bf81c-121">**Adj** is used to provide adjustable points for a formula.</span></span> <span data-ttu-id="bf81c-122">Se usado em marcas, **adj** é uma cadeia de caracteres delimitada por vírgula de até 8 valores.</span><span class="sxs-lookup"><span data-stu-id="bf81c-122">If used in tags, **Adj** is a comma-delimited string of up to 8 values.</span></span> <span data-ttu-id="bf81c-123">Alguns valores podem ser omitidos.</span><span class="sxs-lookup"><span data-stu-id="bf81c-123">Some values may be omitted.</span></span> <span data-ttu-id="bf81c-124">Por exemplo, "0, 1, 2,, 4, 5,, 7" seria uma cadeia de caracteres válida, mas o quarto e o sétimo itens não teriam valores (itens são contados a partir de 0).</span><span class="sxs-lookup"><span data-stu-id="bf81c-124">For example, "0,1,2,,4,5,,7" would be a valid string but the fourth and seventh items would not have values (items are counted starting from 0).</span></span>

<span data-ttu-id="bf81c-125">Para scripts, **adj** usa o tipo de dados [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="bf81c-125">For scripting, **Adj** uses the [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) data type.</span></span>

<span data-ttu-id="bf81c-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="bf81c-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="bf81c-127">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="bf81c-127">**See Also**</span></span>

[<span data-ttu-id="bf81c-128">Fórmula</span><span class="sxs-lookup"><span data-stu-id="bf81c-128">Formula</span></span>](msdn-online-vml-formulas-element.md)

<span data-ttu-id="bf81c-129">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="bf81c-129">**Example**</span></span>

<span data-ttu-id="bf81c-130">Um quadrado simples é criado com ajustes.</span><span class="sxs-lookup"><span data-stu-id="bf81c-130">A simple square is created with adjustments.</span></span> <span data-ttu-id="bf81c-131">Primeiro, a cadeia de caracteres de **adj** é criada para definir oito valores de ajuste.</span><span class="sxs-lookup"><span data-stu-id="bf81c-131">First the **Adj** string is created to define eight adjustment values.</span></span> <span data-ttu-id="bf81c-132">Em seguida, cada valor de ajuste é referenciado por uma das oito fórmulas, com cada valor de ajuste precedido por um símbolo de sinal de número ( \# ).</span><span class="sxs-lookup"><span data-stu-id="bf81c-132">Then each adjustment value is referenced by one of the eight formulas, with each adjustment value preceeded by a number sign (\#) symbol.</span></span> <span data-ttu-id="bf81c-133">Por fim, um caminho é definido por uma cadeia de caracteres que faz referência às fórmulas, com cada fórmula precedida pelo símbolo de arroba (@).</span><span class="sxs-lookup"><span data-stu-id="bf81c-133">Finally a path is defined by a string that references the formulas, with each formula preceeded by the "at" sign (@) symbol.</span></span>


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



<span data-ttu-id="bf81c-134">[Exemplo de atributo adj](/previous-versions/bb229662(v=vs.85)) (requer o Microsoft Internet Explorer 5 ou superior).</span><span class="sxs-lookup"><span data-stu-id="bf81c-134">[Adj Attribute Example](/previous-versions/bb229662(v=vs.85)) (Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 