---
title: Atributo on (TextPath) (VML)
description: Atributo on (TextPath) (VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499145"
---
# <a name="on-attribute-textpathvml"></a><span data-ttu-id="eeb7b-103">Atributo on (TextPath) (VML)</span><span class="sxs-lookup"><span data-stu-id="eeb7b-103">On Attribute (TextPath)(VML)</span></span>

<span data-ttu-id="eeb7b-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eeb7b-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eeb7b-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eeb7b-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eeb7b-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="eeb7b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eeb7b-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="eeb7b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eeb7b-110">Define se o texto é exibido.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-110">Defines whether the text is displayed.</span></span> <span data-ttu-id="eeb7b-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-111">Read/write.</span></span> <span data-ttu-id="eeb7b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-112">**VgTriState**.</span></span>

<span data-ttu-id="eeb7b-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-113">**Applies To**</span></span>

[<span data-ttu-id="eeb7b-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="eeb7b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="eeb7b-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-115">**Tag Syntax**</span></span>

<span data-ttu-id="eeb7b-116"><v: *Element* em = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="eeb7b-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="eeb7b-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-117">**Script Syntax**</span></span>

<span data-ttu-id="eeb7b-118">*elemento* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="eeb7b-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="eeb7b-119">*expressão* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="eeb7b-119">*expression*=*element*.on</span></span>

<span data-ttu-id="eeb7b-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-120">**Remarks**</span></span>

<span data-ttu-id="eeb7b-121">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-121">Default is **False**.</span></span> <span data-ttu-id="eeb7b-122">Esse valor deve ser definido como **true** para exibir o texto em um caminho de texto.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-122">This value must be set to **True** to display text on a text path.</span></span>

<span data-ttu-id="eeb7b-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="eeb7b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="eeb7b-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-124">**Example**</span></span>

<span data-ttu-id="eeb7b-125">O texto no caminho de texto será exibido.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-125">The text on the text path will be displayed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 