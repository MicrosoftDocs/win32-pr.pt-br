---
title: Atributo de inserção de VML
description: Atributo de inserção de VML
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084621"
---
# <a name="vml-inset-attribute"></a><span data-ttu-id="35a6b-103">Atributo de inserção de VML</span><span class="sxs-lookup"><span data-stu-id="35a6b-103">VML Inset Attribute</span></span>

<span data-ttu-id="35a6b-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="35a6b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="35a6b-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="35a6b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="35a6b-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="35a6b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="35a6b-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="35a6b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="35a6b-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="35a6b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="35a6b-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="35a6b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="35a6b-110">Especifica valores de margem interna para texto de TextBox.</span><span class="sxs-lookup"><span data-stu-id="35a6b-110">Specifies inner margin values for textbox text.</span></span> <span data-ttu-id="35a6b-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="35a6b-111">Read/write.</span></span> <span data-ttu-id="35a6b-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="35a6b-112">**String**.</span></span>

<span data-ttu-id="35a6b-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="35a6b-113">**Applies To**</span></span>

[<span data-ttu-id="35a6b-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="35a6b-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="35a6b-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="35a6b-115">**Tag Syntax**</span></span>

<span data-ttu-id="35a6b-116"><v: *Element* relevo = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="35a6b-116"><v: *element* inset=" *expression* "></span></span>

<span data-ttu-id="35a6b-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="35a6b-117">**Script Syntax**</span></span>

<span data-ttu-id="35a6b-118">*Element* . relevo = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="35a6b-118">*element* .inset="*expression*"</span></span>

<span data-ttu-id="35a6b-119">*expressão* = de *elemento*. relevo</span><span class="sxs-lookup"><span data-stu-id="35a6b-119">*expression*=*element*.inset</span></span>

<span data-ttu-id="35a6b-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="35a6b-120">**Remarks**</span></span>

<span data-ttu-id="35a6b-121">O valor da margem de texto interna é especificado como uma cadeia de caracteres que contém quatro valores, cada um separado por vírgulas ou espaços.</span><span class="sxs-lookup"><span data-stu-id="35a6b-121">The internal text margin value is specified as a string containing four values, each separated by commas or spaces.</span></span> <span data-ttu-id="35a6b-122">Os valores medem a margem interna das bordas esquerda, superior, direita e inferior da caixa especificada pelo atributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) do **caminho**.</span><span class="sxs-lookup"><span data-stu-id="35a6b-122">The values measure inset from the left, top, right, and bottom edges of the box specified by the [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) attribute of **Path**.</span></span> <span data-ttu-id="35a6b-123">Os valores ausentes são definidos como o padrão, que é "0,1 in, 0,05 in, 0,1 in, 0,05 in".</span><span class="sxs-lookup"><span data-stu-id="35a6b-123">Missing values are set to the default, which is "0.1in, 0.05in, 0.1in, 0.05in".</span></span>

<span data-ttu-id="35a6b-124">Para formas giradas em navegadores que não dão suporte à rotação, a caixa delimitadora se ajustará ao múltiplo mais próximo de 90 graus.</span><span class="sxs-lookup"><span data-stu-id="35a6b-124">For rotated shapes in browsers that do not support rotation, the bounding box will snap to the closest multiple of 90 degrees.</span></span>

<span data-ttu-id="35a6b-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="35a6b-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="35a6b-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="35a6b-126">**Example**</span></span>

<span data-ttu-id="35a6b-127">A caixa de texto terá uma margem de margem interna de 10 pixels.</span><span class="sxs-lookup"><span data-stu-id="35a6b-127">The textbox will have an inset margin of 10 pixels.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 