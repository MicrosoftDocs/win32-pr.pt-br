---
title: Atributo de ID (VML)
description: Atributo de ID (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454155"
---
# <a name="id-attribute-vml"></a><span data-ttu-id="c308e-103">Atributo de ID (VML)</span><span class="sxs-lookup"><span data-stu-id="c308e-103">ID Attribute (VML)</span></span>

<span data-ttu-id="c308e-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c308e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c308e-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c308e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c308e-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c308e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c308e-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c308e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c308e-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c308e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c308e-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c308e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c308e-110">Fornece um identificador exclusivo para um elemento.</span><span class="sxs-lookup"><span data-stu-id="c308e-110">Provides a unique identifier for an element.</span></span> <span data-ttu-id="c308e-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c308e-111">Read/write.</span></span> <span data-ttu-id="c308e-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="c308e-112">**String**.</span></span>

<span data-ttu-id="c308e-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c308e-113">**Applies To**</span></span>

<span data-ttu-id="c308e-114">Todos os elementos de VML.</span><span class="sxs-lookup"><span data-stu-id="c308e-114">All VML elements.</span></span>

<span data-ttu-id="c308e-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c308e-115">**Tag Syntax**</span></span>

<span data-ttu-id="c308e-116"><v: *ElementName* ID = " *idname* " ></span><span class="sxs-lookup"><span data-stu-id="c308e-116"><v: *elementname* id=" *idname* "></span></span>

<span data-ttu-id="c308e-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="c308e-117">**Script Syntax**</span></span>

<span data-ttu-id="c308e-118">*ElementName* . ID = " *idname* "</span><span class="sxs-lookup"><span data-stu-id="c308e-118">*elementname* .id =" *idname* "</span></span>

<span data-ttu-id="c308e-119">*expressão* = de *ElementName*. ID</span><span class="sxs-lookup"><span data-stu-id="c308e-119">*expression*=*elementname*.id</span></span>

<span data-ttu-id="c308e-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c308e-120">**Remarks**</span></span>

<span data-ttu-id="c308e-121">Use **ID** para se referir a um elemento específico.</span><span class="sxs-lookup"><span data-stu-id="c308e-121">Use **ID** to refer to a specific element.</span></span> <span data-ttu-id="c308e-122">Depois de criar uma forma e dada a ela uma ID, você pode usar o nome da ID quando desejar manipular o elemento.</span><span class="sxs-lookup"><span data-stu-id="c308e-122">Once you have created a shape and given it an ID, you can use the ID name when you want to manipulate the element.</span></span>

<span data-ttu-id="c308e-123">A **ID** é necessária para usar o elemento [ShapeType](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c308e-123">**ID** is required to use the [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span>

<span data-ttu-id="c308e-124">Quando a VML é gerada por Microsoft Office, se um nome de modelo de objeto for atribuído à forma, a **ID** será definida com esse nome.</span><span class="sxs-lookup"><span data-stu-id="c308e-124">When VML is generated by Microsoft Office, if an object model name is assigned to the shape, then **ID** is set to this name.</span></span> <span data-ttu-id="c308e-125">Se o nome do modelo de objeto não estiver definido, o nome será gerado usando o *SPID* (ID de forma interna) mais um prefixo (S para Shape, M para Shape mestre, T para ShapeType).</span><span class="sxs-lookup"><span data-stu-id="c308e-125">If the object model name is not set, then the name is generated using the *Spid* (internal shape ID) plus a prefix (S for shape, M for master shape, T for shapetype).</span></span>

<span data-ttu-id="c308e-126">*Atributo padrão da VML*.</span><span class="sxs-lookup"><span data-stu-id="c308e-126">*VML Standard Attribute*.</span></span>

<span data-ttu-id="c308e-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c308e-127">**Example**</span></span>

<span data-ttu-id="c308e-128">Para alterar os atributos de uma forma, você deve primeiro dar uma ID à forma; por exemplo, "myRect".</span><span class="sxs-lookup"><span data-stu-id="c308e-128">To change the attributes of a shape, you must first give the shape an ID; for example, "myrect".</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



<span data-ttu-id="c308e-129">[Exemplo de atributo de ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span><span class="sxs-lookup"><span data-stu-id="c308e-129">[ID Attribute Example](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span></span> <span data-ttu-id="c308e-130">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="c308e-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 