---
title: Atributo limo de VML
description: Atributo limo de VML
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366077"
---
# <a name="vml-limo-attribute"></a><span data-ttu-id="0b2ce-103">Atributo limo de VML</span><span class="sxs-lookup"><span data-stu-id="0b2ce-103">VML Limo Attribute</span></span>

<span data-ttu-id="0b2ce-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0b2ce-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0b2ce-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0b2ce-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0b2ce-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0b2ce-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0b2ce-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0b2ce-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0b2ce-110">Define um ponto de ampliação no caminho.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-110">Defines a stretch point on the path.</span></span> <span data-ttu-id="0b2ce-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-111">Read/write.</span></span> <span data-ttu-id="0b2ce-112">**Vector2D**.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-112">**Vector2D**.</span></span>

<span data-ttu-id="0b2ce-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0b2ce-113">**Applies To**</span></span>

[<span data-ttu-id="0b2ce-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b2ce-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="0b2ce-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0b2ce-115">**Tag Syntax**</span></span>

<span data-ttu-id="0b2ce-116"><v: *Element* limo = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="0b2ce-116"><v: *element* limo=" *expression* "></span></span>

<span data-ttu-id="0b2ce-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="0b2ce-117">**Script Syntax**</span></span>

<span data-ttu-id="0b2ce-118">*Element* . limo = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="0b2ce-118">*element* .limo="*expression*"</span></span>

<span data-ttu-id="0b2ce-119">*expressão* = de *elemento*. limo</span><span class="sxs-lookup"><span data-stu-id="0b2ce-119">*expression*=*element*.limo</span></span>

<span data-ttu-id="0b2ce-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0b2ce-120">**Remarks**</span></span>

<span data-ttu-id="0b2ce-121">O valor padrão é "0 0".</span><span class="sxs-lookup"><span data-stu-id="0b2ce-121">The default value is "0 0".</span></span> <span data-ttu-id="0b2ce-122">Limo stretchs são pontos na borda de uma forma que definem onde e como uma forma pode ser ampliada por um usuário em um editor gráfico.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-122">Limo stretches are points on a shape's edge that define where and how a shape may be stretched by a user in a graphical editor.</span></span>

<span data-ttu-id="0b2ce-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="0b2ce-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0b2ce-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0b2ce-124">**Example**</span></span>

<span data-ttu-id="0b2ce-125">Um ponto de ampliação limo é definido em meio ao longo da linha horizontal.</span><span class="sxs-lookup"><span data-stu-id="0b2ce-125">A limo stretch point is defined halfway along the horizontal line.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 