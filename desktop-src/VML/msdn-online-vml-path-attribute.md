---
title: Atributo de caminho VML
description: Atributo de caminho VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823968"
---
# <a name="vml-path-attribute"></a><span data-ttu-id="0262a-103">Atributo de caminho VML</span><span class="sxs-lookup"><span data-stu-id="0262a-103">VML Path Attribute</span></span>

<span data-ttu-id="0262a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0262a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0262a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0262a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0262a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0262a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0262a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0262a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0262a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0262a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0262a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0262a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0262a-110">Especifica a linha que compõe as bordas de uma forma.</span><span class="sxs-lookup"><span data-stu-id="0262a-110">Specifies the line that makes up the edges of a shape.</span></span> <span data-ttu-id="0262a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0262a-111">Read/write.</span></span> <span data-ttu-id="0262a-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="0262a-112">**String**.</span></span>

<span data-ttu-id="0262a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0262a-113">**Applies To**</span></span>

[<span data-ttu-id="0262a-114">Forma</span><span class="sxs-lookup"><span data-stu-id="0262a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0262a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0262a-115">**Tag Syntax**</span></span>

<span data-ttu-id="0262a-116"><v: *Element* caminho = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0262a-116"><v: *element* path=" *expression* "></span></span>

<span data-ttu-id="0262a-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="0262a-117">**Script Syntax**</span></span>

<span data-ttu-id="0262a-118">*elemento* . Path = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="0262a-118">*element* .path="*expression*"</span></span>

<span data-ttu-id="0262a-119">*expressão* = de *elemento*. Path</span><span class="sxs-lookup"><span data-stu-id="0262a-119">*expression*=*element*.path</span></span>

<span data-ttu-id="0262a-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0262a-120">**Remarks**</span></span>

<span data-ttu-id="0262a-121">Se uma forma contiver o elemento [path](msdn-online-vml-path-element.md) , os comandos Path do elemento Path têm precedência sobre o valor do atributo Shape.</span><span class="sxs-lookup"><span data-stu-id="0262a-121">If a shape contains the [Path](msdn-online-vml-path-element.md) element, the path commands of the Path element take precedence over the shape attribute value.</span></span> <span data-ttu-id="0262a-122">Consulte o tópico elemento **path** para obter detalhes sobre o conjunto de comandos usado para caminhos.</span><span class="sxs-lookup"><span data-stu-id="0262a-122">See the **Path** element topic for details on the command set used for paths.</span></span>

<span data-ttu-id="0262a-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="0262a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0262a-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0262a-124">**Example**</span></span>

<span data-ttu-id="0262a-125">Um caminho quadrado fechado é definido na cadeia de caracteres do atributo Path.</span><span class="sxs-lookup"><span data-stu-id="0262a-125">A closed square path is defined in the string of the path attribute.</span></span> <span data-ttu-id="0262a-126">Um ponto inicial é definido com `m` (usado para o comando **MoveTo** ) em 1, 1 e uma linha é desenhada com `l` (a letra "L" usada para a **linha** de comando) da posição inicial (1, 1) para os outros três pontos (em ordem): 1.200; 200.200; 200, 1.</span><span class="sxs-lookup"><span data-stu-id="0262a-126">An initial point is defined with `m` (used for the **moveto** command) at 1,1 and a line is drawn with `l` (the letter "L" used for the command **lineto**) from the starting position (1,1) to the other three points (in order): 1,200; 200,200; 200,1.</span></span> <span data-ttu-id="0262a-127">A linha é fechada com `x` (**Close**) e terminada com `e` (**end**).</span><span class="sxs-lookup"><span data-stu-id="0262a-127">The line is closed with `x` (**close**) and ended with `e` (**end**).</span></span> <span data-ttu-id="0262a-128">Observe que as coordenadas são fornecidas no espaço de coordenadas relativo e que o tamanho real é determinado pela **largura** e **altura**.</span><span class="sxs-lookup"><span data-stu-id="0262a-128">Note that coordinates are given in the relative coordinate space and that the real size is determined by the **width** and **height**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="0262a-129">[Exemplo de atributo path](/previous-versions/bb264089(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0262a-129">[Path Attribute Example](/previous-versions/bb264089(v=vs.85)).</span></span> <span data-ttu-id="0262a-130">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="0262a-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 