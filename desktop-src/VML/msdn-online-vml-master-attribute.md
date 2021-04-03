---
title: Atributo mestre da VML
description: Atributo mestre da VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084881"
---
# <a name="vml-master-attribute"></a><span data-ttu-id="4e02a-103">Atributo mestre da VML</span><span class="sxs-lookup"><span data-stu-id="4e02a-103">VML Master Attribute</span></span>

<span data-ttu-id="4e02a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4e02a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4e02a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="4e02a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4e02a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="4e02a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4e02a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="4e02a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4e02a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4e02a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4e02a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4e02a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4e02a-110">Determina se um elemento **ShapeType** é um elemento mestre.</span><span class="sxs-lookup"><span data-stu-id="4e02a-110">Determines whether a **ShapeType** element is a master element.</span></span> <span data-ttu-id="4e02a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4e02a-111">Read/write.</span></span> <span data-ttu-id="4e02a-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="4e02a-112">**VgTriState**.</span></span>

<span data-ttu-id="4e02a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="4e02a-113">**Applies To**</span></span>

[<span data-ttu-id="4e02a-114">Formatype</span><span class="sxs-lookup"><span data-stu-id="4e02a-114">ShapeType</span></span>](msdn-online-vml-shapetype-element.md)

<span data-ttu-id="4e02a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="4e02a-115">**Tag Syntax**</span></span>

<span data-ttu-id="4e02a-116"><v: *Element* o:Master = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="4e02a-116"><v: *element* o:master=" *expression* "></span></span>

<span data-ttu-id="4e02a-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="4e02a-117">**Remarks**</span></span>

<span data-ttu-id="4e02a-118">Se **for true**, a forma **ShapeType** será renderizada pelo mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="4e02a-118">If **True**, the **ShapeType** shape is rendered by the rendering engine.</span></span> <span data-ttu-id="4e02a-119">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="4e02a-119">The default value is **False**.</span></span>

<span data-ttu-id="4e02a-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="4e02a-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="4e02a-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="4e02a-121">**Example**</span></span>

<span data-ttu-id="4e02a-122">O elemento **formatype** é uma forma mestra.</span><span class="sxs-lookup"><span data-stu-id="4e02a-122">The **ShapeType** element is a master shape.</span></span>


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 