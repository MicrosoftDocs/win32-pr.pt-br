---
title: Atributo de tipo (forma) (VML)
description: Atributo de tipo (forma) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007706"
---
# <a name="type-attribute-shapevml"></a><span data-ttu-id="188b9-103">Atributo de tipo (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="188b9-103">Type Attribute (Shape)(VML)</span></span>

<span data-ttu-id="188b9-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="188b9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="188b9-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="188b9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="188b9-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="188b9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="188b9-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="188b9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="188b9-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="188b9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="188b9-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="188b9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="188b9-110">Define uma referência à ID de um elemento [ShapeType](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="188b9-110">Defines a reference to the ID of a [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span> <span data-ttu-id="188b9-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="188b9-111">Read/write.</span></span> <span data-ttu-id="188b9-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="188b9-112">**String**.</span></span>

<span data-ttu-id="188b9-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="188b9-113">**Applies To**</span></span>

[<span data-ttu-id="188b9-114">Forma</span><span class="sxs-lookup"><span data-stu-id="188b9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="188b9-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="188b9-115">**Tag Syntax**</span></span>

``` syntax
<v:
          element 
          type=" expression ">
```

<span data-ttu-id="188b9-116">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="188b9-116">**Script Syntax**</span></span>

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

<span data-ttu-id="188b9-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="188b9-117">**Remarks**</span></span>

<span data-ttu-id="188b9-118">Se o atributo **Type** referenciar a ID de um elemento **ShapeType** , os preenchimentos, os caminhos e os traços do **ShapeType** serão usados como modelos para criar a forma.</span><span class="sxs-lookup"><span data-stu-id="188b9-118">If the **Type** attribute references the ID of a **ShapeType** element, the fills, paths, and strokes of the **ShapeType** are used as templates to create the shape.</span></span> <span data-ttu-id="188b9-119">Os valores derivados de **ShapeType** podem ser substituídos por valores de forma individuais.</span><span class="sxs-lookup"><span data-stu-id="188b9-119">Values derived from **ShapeType** can be overridden by individual shape values.</span></span>

<span data-ttu-id="188b9-120">Se usado em marcas, o valor da cadeia de caracteres deve começar com um símbolo de sinal numérico ( \# ).</span><span class="sxs-lookup"><span data-stu-id="188b9-120">If used in tags, the string value must begin with a number sign (\#) symbol.</span></span>

<span data-ttu-id="188b9-121">**Atributo padrão da VML**</span><span class="sxs-lookup"><span data-stu-id="188b9-121">**VML Standard Attribute**</span></span>

<span data-ttu-id="188b9-122">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="188b9-122">**Example**</span></span>

<span data-ttu-id="188b9-123">Uma forma **ShapeType** é criada com o "com MyType" como uma ID.</span><span class="sxs-lookup"><span data-stu-id="188b9-123">A **ShapeType** shape is created with the "mytype" as an ID.</span></span>


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



<span data-ttu-id="188b9-124">Em seguida, se você criar uma forma usando os valores **ShapeType** , a forma terá os atributos da **forma**"com MyType". ou seja, "shape01" terá um preenchimento vermelho com um traço azul.</span><span class="sxs-lookup"><span data-stu-id="188b9-124">Then if you create a shape using the **ShapeType** values, the shape will have the attributes of the "mytype" **ShapeType**; that is, "shape01" will have a red fill with a blue stroke.</span></span>


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="188b9-125">Você pode substituir os valores herdados, por exemplo, alterando a cor para verde.</span><span class="sxs-lookup"><span data-stu-id="188b9-125">You can override the inherited values, for example, by changing the color to green.</span></span>


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="188b9-126">[Exemplo do atributo Type](/previous-versions/bb264099(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="188b9-126">[Type Attribute Example](/previous-versions/bb264099(v=vs.85)).</span></span> <span data-ttu-id="188b9-127">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="188b9-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 