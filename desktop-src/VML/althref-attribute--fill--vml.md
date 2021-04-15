---
title: Atributo AltHRef (Fill) (VML)
description: Atributo AltHRef (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454147"
---
# <a name="althref-attribute-fillvml"></a><span data-ttu-id="8a2f9-103">Atributo AltHRef (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="8a2f9-103">AltHRef Attribute (Fill)(VML)</span></span>

<span data-ttu-id="8a2f9-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8a2f9-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8a2f9-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8a2f9-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8a2f9-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8a2f9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8a2f9-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8a2f9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8a2f9-110">Define uma referência alternativa para uma imagem.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-110">Defines an alternate reference for an image.</span></span> <span data-ttu-id="8a2f9-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-111">Read/write.</span></span> <span data-ttu-id="8a2f9-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-112">**String**.</span></span>

<span data-ttu-id="8a2f9-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="8a2f9-113">**Applies To**</span></span>

[<span data-ttu-id="8a2f9-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="8a2f9-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="8a2f9-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="8a2f9-115">**Tag Syntax**</span></span>

<span data-ttu-id="8a2f9-116"><v: *Element* o:althref = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="8a2f9-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="8a2f9-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="8a2f9-117">**Script Syntax**</span></span>

<span data-ttu-id="8a2f9-118">*Element* . althref = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="8a2f9-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="8a2f9-119">*expressão* = de *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="8a2f9-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="8a2f9-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="8a2f9-120">**Remarks**</span></span>

<span data-ttu-id="8a2f9-121">Dá suporte à preservação de dados PICT por meio de roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="8a2f9-122">Na gravação em HTML, a representação alternativa (os dados originais do PICT se o arquivo foi originado do Apple Macintosh) é salva.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-122">On HTML write, the alternate representation (the original PICT data if the file originated from the Apple Macintosh) is saved.</span></span> <span data-ttu-id="8a2f9-123">Em HTML Read, **AltHRef** é favorecedo sobre **src**.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="8a2f9-124">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="8a2f9-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="8a2f9-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="8a2f9-125">**Example**</span></span>

<span data-ttu-id="8a2f9-126">O preenchimento da forma tem um **AltHRef** que aponta para um arquivo chamado myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-126">The fill of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 