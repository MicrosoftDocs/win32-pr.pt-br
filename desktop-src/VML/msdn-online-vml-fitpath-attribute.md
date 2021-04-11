---
title: Atributo FitPath de VML
description: Atributo FitPath de VML
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805e59a50c63248ed936f6a849869057a34a6e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162405"
---
# <a name="vml-fitpath-attribute"></a><span data-ttu-id="3f4e7-103">Atributo FitPath de VML</span><span class="sxs-lookup"><span data-stu-id="3f4e7-103">VML FitPath Attribute</span></span>

<span data-ttu-id="3f4e7-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f4e7-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f4e7-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f4e7-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f4e7-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3f4e7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f4e7-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3f4e7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f4e7-110">Define se o texto se ajusta ao caminho de uma forma.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-110">Defines whether the text fits the path of a shape.</span></span> <span data-ttu-id="3f4e7-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-111">Read/write.</span></span> <span data-ttu-id="3f4e7-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-112">**VgTriState**.</span></span>

<span data-ttu-id="3f4e7-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3f4e7-113">**Applies To**</span></span>

[<span data-ttu-id="3f4e7-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="3f4e7-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="3f4e7-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3f4e7-115">**Tag Syntax**</span></span>

<span data-ttu-id="3f4e7-116"><v: *Element* fitpath = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="3f4e7-116"><v: *element* fitpath=" *expression* "></span></span>

<span data-ttu-id="3f4e7-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="3f4e7-117">**Script Syntax**</span></span>

<span data-ttu-id="3f4e7-118">*Element* . fitpath = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="3f4e7-118">*element* .fitpath="*expression*"</span></span>

<span data-ttu-id="3f4e7-119">*expressão* = de *elemento*. fitpath</span><span class="sxs-lookup"><span data-stu-id="3f4e7-119">*expression*=*element*.fitpath</span></span>

<span data-ttu-id="3f4e7-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3f4e7-120">**Remarks**</span></span>

<span data-ttu-id="3f4e7-121">Se **for true**, dimensionará o texto para preencher o caminho em que ele se encontra.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-121">If **True**, sizes the text to fill the path it lies out on.</span></span> <span data-ttu-id="3f4e7-122">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-122">The default is **False**.</span></span>

<span data-ttu-id="3f4e7-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="3f4e7-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3f4e7-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3f4e7-124">**Example**</span></span>

<span data-ttu-id="3f4e7-125">O texto se ajustará ao caminho.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-125">The text will fit the path.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 