---
title: Atributo ShadowOK de VML
description: Atributo ShadowOK de VML
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007581"
---
# <a name="vml-shadowok-attribute"></a><span data-ttu-id="05e54-103">Atributo ShadowOK de VML</span><span class="sxs-lookup"><span data-stu-id="05e54-103">VML ShadowOK Attribute</span></span>

<span data-ttu-id="05e54-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="05e54-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="05e54-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="05e54-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="05e54-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="05e54-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="05e54-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="05e54-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="05e54-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="05e54-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="05e54-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="05e54-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="05e54-110">Determina se uma sombra será exibida.</span><span class="sxs-lookup"><span data-stu-id="05e54-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="05e54-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="05e54-111">Read/write.</span></span> <span data-ttu-id="05e54-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="05e54-112">**VgTriState**.</span></span>

<span data-ttu-id="05e54-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="05e54-113">**Applies To**</span></span>

[<span data-ttu-id="05e54-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="05e54-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="05e54-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="05e54-115">**Tag Syntax**</span></span>

<span data-ttu-id="05e54-116"><v: *Element* shadowok = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="05e54-116"><v: *element* shadowok=" *expression* "></span></span>

<span data-ttu-id="05e54-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="05e54-117">**Script Syntax**</span></span>

<span data-ttu-id="05e54-118">*Element* . shadowok = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="05e54-118">*element* .shadowok="*expression*"</span></span>

<span data-ttu-id="05e54-119">*expressão* = de *elemento*. shadowok</span><span class="sxs-lookup"><span data-stu-id="05e54-119">*expression*=*element*.shadowok</span></span>

<span data-ttu-id="05e54-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="05e54-120">**Remarks**</span></span>

<span data-ttu-id="05e54-121">Se **for false**, o caminho não poderá ter uma sombra.</span><span class="sxs-lookup"><span data-stu-id="05e54-121">If **False**, the path cannot have a shadow.</span></span> <span data-ttu-id="05e54-122">O padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="05e54-122">The default is **True**.</span></span> <span data-ttu-id="05e54-123">Esse atributo substitui todos os outros atributos de sombra no elemento pai ou **sombra** .</span><span class="sxs-lookup"><span data-stu-id="05e54-123">This attribute overrides all other shadow attributes in the parent or **Shadow** element.</span></span>

<span data-ttu-id="05e54-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="05e54-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="05e54-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="05e54-125">**Example**</span></span>

<span data-ttu-id="05e54-126">A forma não terá uma sombra.</span><span class="sxs-lookup"><span data-stu-id="05e54-126">The shape will not have a shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 