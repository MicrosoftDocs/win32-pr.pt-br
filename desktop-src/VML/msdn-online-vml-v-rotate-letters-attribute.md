---
title: Atributo da VML V-Rotate-Letters
description: Atributo da VML V-Rotate-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084578"
---
# <a name="vml-v-rotate-letters-attribute"></a><span data-ttu-id="cf764-103">Atributo da VML V-Rotate-Letters</span><span class="sxs-lookup"><span data-stu-id="cf764-103">VML V-Rotate-Letters Attribute</span></span>

<span data-ttu-id="cf764-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cf764-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cf764-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="cf764-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cf764-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="cf764-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cf764-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="cf764-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cf764-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cf764-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cf764-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cf764-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cf764-110">Determina se as letras do texto são giradas.</span><span class="sxs-lookup"><span data-stu-id="cf764-110">Determines whether the letters of the text are rotated.</span></span> <span data-ttu-id="cf764-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cf764-111">Read/write.</span></span> <span data-ttu-id="cf764-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="cf764-112">**VgTriState**.</span></span>

<span data-ttu-id="cf764-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="cf764-113">**Applies To**</span></span>

[<span data-ttu-id="cf764-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="cf764-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="cf764-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="cf764-115">**Tag Syntax**</span></span>

<span data-ttu-id="cf764-116"><v: *elemento* Style = "v-Rotate-Letters: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cf764-116"><v: *element* style="v-rotate-letters: *expression* "></span></span>

<span data-ttu-id="cf764-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="cf764-117">**Script Syntax**</span></span>

<span data-ttu-id="cf764-118">*elemento* . Style. v-Rotate-Letters = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="cf764-118">*element* .style.v-rotate-letters="*expression*"</span></span>

<span data-ttu-id="cf764-119">*expressão* = de *elemento*. Style. v-Rotate-Letters</span><span class="sxs-lookup"><span data-stu-id="cf764-119">*expression*=*element*.style.v-rotate-letters</span></span>

<span data-ttu-id="cf764-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="cf764-120">**Remarks**</span></span>

<span data-ttu-id="cf764-121">Se **for true**, as letras do texto serão giradas 90 graus.</span><span class="sxs-lookup"><span data-stu-id="cf764-121">If **True**, the letters of the text are rotated 90 degrees.</span></span> <span data-ttu-id="cf764-122">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="cf764-122">The default value is **False**.</span></span>

<span data-ttu-id="cf764-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="cf764-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="cf764-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="cf764-124">**Example**</span></span>

<span data-ttu-id="cf764-125">As letras são giradas 90 graus.</span><span class="sxs-lookup"><span data-stu-id="cf764-125">The letters are rotated 90 degrees.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 