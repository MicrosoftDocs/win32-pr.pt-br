---
title: Atributo de ID (sombra) (VML)
description: Atributo de ID (sombra) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641360"
---
# <a name="id-attribute-shadowvml"></a><span data-ttu-id="41f7d-103">Atributo de ID (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="41f7d-103">ID Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="41f7d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="41f7d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="41f7d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="41f7d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="41f7d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="41f7d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="41f7d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="41f7d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="41f7d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="41f7d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="41f7d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="41f7d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="41f7d-110">Especifica um nome que fornece um identificador exclusivo para uma sombra.</span><span class="sxs-lookup"><span data-stu-id="41f7d-110">Specifies a name that provides a unique identifier for a shadow.</span></span> <span data-ttu-id="41f7d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="41f7d-111">Read/write.</span></span> <span data-ttu-id="41f7d-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="41f7d-112">**String**.</span></span>

<span data-ttu-id="41f7d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="41f7d-113">**Applies To**</span></span>

[<span data-ttu-id="41f7d-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="41f7d-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="41f7d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="41f7d-115">**Tag Syntax**</span></span>

<span data-ttu-id="41f7d-116"><v: *Element* ID = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="41f7d-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="41f7d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="41f7d-117">**Script Syntax**</span></span>

<span data-ttu-id="41f7d-118">*Element* . ID = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="41f7d-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="41f7d-119">*expressão* = de *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="41f7d-119">*expression*=*element*.id</span></span>

<span data-ttu-id="41f7d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="41f7d-120">**Remarks**</span></span>

<span data-ttu-id="41f7d-121">Use **ID** para fazer referência a uma sombra específica.</span><span class="sxs-lookup"><span data-stu-id="41f7d-121">Use **ID** to refer to a specific shadow.</span></span> <span data-ttu-id="41f7d-122">Depois de criar uma sombra e dada a ela uma ID, você pode usar o nome da ID quando desejar manipular a sombra.</span><span class="sxs-lookup"><span data-stu-id="41f7d-122">Once you have created a shadow and given it an ID, you can use the ID name when you want to manipulate the shadow.</span></span>

<span data-ttu-id="41f7d-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="41f7d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="41f7d-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="41f7d-124">**Example**</span></span>

<span data-ttu-id="41f7d-125">A forma tem uma ID de sombra chamada "MyShadow".</span><span class="sxs-lookup"><span data-stu-id="41f7d-125">The shape has a shadow ID called "myshadow".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 