---
title: Atributo de ID (TextBox) (VML)
description: Atributo de ID (TextBox) (VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823845"
---
# <a name="id-attribute-textboxvml"></a><span data-ttu-id="be254-103">Atributo de ID (TextBox) (VML)</span><span class="sxs-lookup"><span data-stu-id="be254-103">ID Attribute (TextBox)(VML)</span></span>

<span data-ttu-id="be254-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="be254-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="be254-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="be254-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="be254-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="be254-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="be254-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="be254-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="be254-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="be254-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="be254-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="be254-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="be254-110">Um nome que fornece um identificador exclusivo para uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="be254-110">A name that provides a unique identifier for a textbox.</span></span> <span data-ttu-id="be254-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="be254-111">Read/write.</span></span> <span data-ttu-id="be254-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="be254-112">**String**.</span></span>

<span data-ttu-id="be254-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="be254-113">**Applies To**</span></span>

[<span data-ttu-id="be254-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="be254-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="be254-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="be254-115">**Tag Syntax**</span></span>

<span data-ttu-id="be254-116"><v: *Element* ID = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="be254-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="be254-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="be254-117">**Script Syntax**</span></span>

<span data-ttu-id="be254-118">*Element* . ID = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="be254-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="be254-119">*expressão* = de *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="be254-119">*expression*=*element*.id</span></span>

<span data-ttu-id="be254-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="be254-120">**Remarks**</span></span>

<span data-ttu-id="be254-121">Use **ID** para se referir a uma caixa de texto específica.</span><span class="sxs-lookup"><span data-stu-id="be254-121">Use **ID** to refer to a specific textbox.</span></span> <span data-ttu-id="be254-122">Depois de criar uma caixa de texto e fornecer a ela uma ID, você poderá usar o nome da ID quando desejar manipular a caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="be254-122">Once you have created a textbox and given it an ID, you can use the ID name when you want to manipulate the textbox.</span></span>

<span data-ttu-id="be254-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="be254-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="be254-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="be254-124">**Example**</span></span>

<span data-ttu-id="be254-125">A forma tem uma ID de caixa de texto chamada "myTextBox".</span><span class="sxs-lookup"><span data-stu-id="be254-125">The shape has a textbox ID called "mytextbox".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 