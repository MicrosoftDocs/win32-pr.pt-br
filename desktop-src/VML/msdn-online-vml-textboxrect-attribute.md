---
title: Atributo TextBoxRect de VML
description: Atributo TextBoxRect de VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007616"
---
# <a name="vml-textboxrect-attribute"></a><span data-ttu-id="1a6e3-103">Atributo TextBoxRect de VML</span><span class="sxs-lookup"><span data-stu-id="1a6e3-103">VML TextBoxRect Attribute</span></span>

<span data-ttu-id="1a6e3-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1a6e3-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1a6e3-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1a6e3-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1a6e3-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1a6e3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1a6e3-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1a6e3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1a6e3-110">Define uma ou mais caixas de texto dentro de uma forma.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-110">Defines one or more text boxes inside a shape.</span></span> <span data-ttu-id="1a6e3-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-111">Read/write.</span></span> <span data-ttu-id="1a6e3-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-112">**String**.</span></span>

<span data-ttu-id="1a6e3-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1a6e3-113">**Applies To**</span></span>

[<span data-ttu-id="1a6e3-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="1a6e3-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="1a6e3-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1a6e3-115">**Tag Syntax**</span></span>

<span data-ttu-id="1a6e3-116"><v: *Element* textboxrect = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="1a6e3-116"><v: *element* textboxrect=" *expression* "></span></span>

<span data-ttu-id="1a6e3-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1a6e3-117">**Script Syntax**</span></span>

<span data-ttu-id="1a6e3-118">*Element* . textboxrect = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1a6e3-118">*element* .textboxrect="*expression*"</span></span>

<span data-ttu-id="1a6e3-119">*expressão* = de *elemento*. textboxrect</span><span class="sxs-lookup"><span data-stu-id="1a6e3-119">*expression*=*element*.textboxrect</span></span>

<span data-ttu-id="1a6e3-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1a6e3-120">**Remarks**</span></span>

<span data-ttu-id="1a6e3-121">Uma caixa de texto é definida por um ou mais conjuntos de números que especificam (na ordem) os pontos esquerdo, superior, direito e inferior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-121">A textbox is defined by one or more sets of numbers specifying (in order) the left, top, right, and bottom points of the rectangle.</span></span> <span data-ttu-id="1a6e3-122">Vários conjuntos são delimitados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-122">Multiple sets are delimited by a semicolon.</span></span> <span data-ttu-id="1a6e3-123">O valor padrão é o mesmo valor de dimensão que o retângulo que o contém.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-123">The default value is the same dimension value as the containing rectangle.</span></span> <span data-ttu-id="1a6e3-124">Se mais de uma caixa de texto for definida, os conjuntos de quádruplo delimitados por vírgula que definem cada caixa de texto serão separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-124">If more than one textbox is defined, the comma-delimited quadruple sets that define each textbox are separated by semicolons.</span></span> <span data-ttu-id="1a6e3-125">Normalmente, as caixas de Textsão fornecidas em conjuntos de 1, 2, 3 ou 6 retângulos em uma forma.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-125">Normally textboxes come in sets of 1, 2, 3, or 6 rectangles on a shape.</span></span>

<span data-ttu-id="1a6e3-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="1a6e3-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="1a6e3-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1a6e3-127">**Example**</span></span>

<span data-ttu-id="1a6e3-128">Uma caixa de texto de 95 unidades por 95 unidades é definida e colocou 5 unidades dentro do canto superior esquerdo da forma.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-128">A textbox of 95 units by 95 units is defined and placed 5 units inside the top left corner of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 