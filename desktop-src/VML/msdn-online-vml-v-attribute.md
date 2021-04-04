---
title: Atributo da VML V
description: Atributo da VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084639"
---
# <a name="vml-v-attribute"></a><span data-ttu-id="6d311-103">Atributo da VML V</span><span class="sxs-lookup"><span data-stu-id="6d311-103">VML V Attribute</span></span>

<span data-ttu-id="6d311-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6d311-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6d311-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="6d311-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6d311-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="6d311-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6d311-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="6d311-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6d311-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6d311-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6d311-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6d311-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6d311-110">Define os comandos que compõem um caminho.</span><span class="sxs-lookup"><span data-stu-id="6d311-110">Defines the commands that make up a path.</span></span> <span data-ttu-id="6d311-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6d311-111">Read/write.</span></span> <span data-ttu-id="6d311-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="6d311-112">**String**.</span></span>

<span data-ttu-id="6d311-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="6d311-113">**Applies To**</span></span>

[<span data-ttu-id="6d311-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="6d311-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="6d311-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="6d311-115">**Tag Syntax**</span></span>

<span data-ttu-id="6d311-116"><v: *Element* v = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="6d311-116"><v: *element* v=" *expression* "></span></span>

<span data-ttu-id="6d311-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="6d311-117">**Script Syntax**</span></span>

<span data-ttu-id="6d311-118">*elemento* . v = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="6d311-118">*element* .v="*expression*"</span></span>

<span data-ttu-id="6d311-119">*expressão* = de *elemento*. v</span><span class="sxs-lookup"><span data-stu-id="6d311-119">*expression*=*element*.v</span></span>

<span data-ttu-id="6d311-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="6d311-120">**Remarks**</span></span>

<span data-ttu-id="6d311-121">Substitui o atributo **path** de uma forma.</span><span class="sxs-lookup"><span data-stu-id="6d311-121">Overrides the **Path** attribute of a shape.</span></span> <span data-ttu-id="6d311-122">As coordenadas podem ser números fixos, números relativos ou referências a fórmulas (usando o formato " @n ", em que n é um número de fórmula; por exemplo, " @2 " refere-se à segunda fórmula na matriz de fórmulas).</span><span class="sxs-lookup"><span data-stu-id="6d311-122">Coordinates can be fixed numbers, relative numbers, or references to formulas (by using the format of "@n" where n is a formula number; for example, "@2" refers to the second formula in the formula array).</span></span>

<span data-ttu-id="6d311-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="6d311-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="6d311-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="6d311-124">**Example**</span></span>

<span data-ttu-id="6d311-125">Um retângulo é criado usando o atributo **V** .</span><span class="sxs-lookup"><span data-stu-id="6d311-125">A rectangle is created using the **V** attribute.</span></span> <span data-ttu-id="6d311-126">Observe que uma letra minúscula L (comando **LineTo** ) é usada após o primeiro conjunto de coordenadas delimitadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6d311-126">Note that a lowercase letter L (**lineto** command) is used after the first set of comma-delimited coordinates.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 