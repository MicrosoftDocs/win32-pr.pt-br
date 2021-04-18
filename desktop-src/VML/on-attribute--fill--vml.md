---
title: No atributo (Fill) (VML)
description: No atributo (Fill) (VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105790457"
---
# <a name="on-attribute-fillvml"></a><span data-ttu-id="21490-103">No atributo (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="21490-103">On Attribute (Fill)(VML)</span></span>

<span data-ttu-id="21490-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="21490-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21490-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="21490-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21490-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="21490-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21490-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="21490-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21490-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21490-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21490-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21490-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21490-110">Determina se o preenchimento será exibido.</span><span class="sxs-lookup"><span data-stu-id="21490-110">Determines whether the fill will be displayed.</span></span> <span data-ttu-id="21490-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="21490-111">Read/write.</span></span> <span data-ttu-id="21490-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="21490-112">**VgTriState**.</span></span>

<span data-ttu-id="21490-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="21490-113">**Applies To**</span></span>

[<span data-ttu-id="21490-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="21490-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="21490-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="21490-115">**Tag Syntax**</span></span>

<span data-ttu-id="21490-116"><v: *Element* em = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="21490-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="21490-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="21490-117">**Script Syntax**</span></span>

<span data-ttu-id="21490-118">*elemento* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="21490-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="21490-119">*expressão* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="21490-119">*expression*=*element*.on</span></span>

<span data-ttu-id="21490-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="21490-120">**Remarks**</span></span>

<span data-ttu-id="21490-121">Se for **false**, o preenchimento não será exibido.</span><span class="sxs-lookup"><span data-stu-id="21490-121">If **False**, the fill is not displayed.</span></span> <span data-ttu-id="21490-122">O padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="21490-122">The default is **True**.</span></span>

<span data-ttu-id="21490-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="21490-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="21490-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="21490-124">**Example**</span></span>

<span data-ttu-id="21490-125">Embora o preenchimento esteja definido como vermelho, ele não é exibido.</span><span class="sxs-lookup"><span data-stu-id="21490-125">Even though the fill is defined to be red, it is not displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 