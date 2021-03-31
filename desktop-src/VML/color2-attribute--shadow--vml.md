---
title: Atributo Color2 (sombra) (VML)
description: Atributo Color2 (sombra) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641573"
---
# <a name="color2-attribute-shadowvml"></a><span data-ttu-id="2fb05-103">Atributo Color2 (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="2fb05-103">Color2 Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="2fb05-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2fb05-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2fb05-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="2fb05-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2fb05-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="2fb05-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2fb05-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="2fb05-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2fb05-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2fb05-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2fb05-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2fb05-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2fb05-110">Define a segunda cor de uma sombra.</span><span class="sxs-lookup"><span data-stu-id="2fb05-110">Defines the second color of a shadow.</span></span> <span data-ttu-id="2fb05-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2fb05-111">Read/write.</span></span> <span data-ttu-id="2fb05-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="2fb05-112">**VgColor**.</span></span>

<span data-ttu-id="2fb05-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="2fb05-113">**Applies To**</span></span>

[<span data-ttu-id="2fb05-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="2fb05-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="2fb05-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="2fb05-115">**Tag Syntax**</span></span>

<span data-ttu-id="2fb05-116"><v: *Element* color2 = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="2fb05-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="2fb05-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="2fb05-117">**Script Syntax**</span></span>

<span data-ttu-id="2fb05-118">*Element* . color2 = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="2fb05-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="2fb05-119">*expressão* = de *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="2fb05-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="2fb05-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="2fb05-120">**Remarks**</span></span>

<span data-ttu-id="2fb05-121">Use uma segunda cor para criar efeitos de sombra especiais.</span><span class="sxs-lookup"><span data-stu-id="2fb05-121">Use a second color to create special shadow effects.</span></span> <span data-ttu-id="2fb05-122">Consulte o atributo [Type](type-attribute--shadow--vml.md) para obter mais informações sobre as segundas cores.</span><span class="sxs-lookup"><span data-stu-id="2fb05-122">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second colors.</span></span>

<span data-ttu-id="2fb05-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="2fb05-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="2fb05-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="2fb05-124">**Example**</span></span>

<span data-ttu-id="2fb05-125">A sombra tem azul para uma segunda cor.</span><span class="sxs-lookup"><span data-stu-id="2fb05-125">The shadow has blue for a second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 