---
title: Atributo gama da VML
description: Atributo gama da VML
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084711"
---
# <a name="vml-gamma-attribute"></a><span data-ttu-id="1f1a7-103">Atributo gama da VML</span><span class="sxs-lookup"><span data-stu-id="1f1a7-103">VML Gamma Attribute</span></span>

<span data-ttu-id="1f1a7-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1f1a7-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1f1a7-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1f1a7-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1f1a7-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1f1a7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1f1a7-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1f1a7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1f1a7-110">Define a quantidade de contraste para uma imagem.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-110">Defines the amount of contrast for an image.</span></span> <span data-ttu-id="1f1a7-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-111">Read/write.</span></span> <span data-ttu-id="1f1a7-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-112">**VgNumber**.</span></span>

<span data-ttu-id="1f1a7-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1f1a7-113">**Applies To**</span></span>

[<span data-ttu-id="1f1a7-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="1f1a7-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="1f1a7-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1f1a7-115">**Tag Syntax**</span></span>

<span data-ttu-id="1f1a7-116"><v: *Element* gama = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1f1a7-116"><v: *element* gamma=" *expression* "></span></span>

<span data-ttu-id="1f1a7-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1f1a7-117">**Script Syntax**</span></span>

<span data-ttu-id="1f1a7-118">*Element* . gama = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1f1a7-118">*element* .gamma="*expression*"</span></span>

<span data-ttu-id="1f1a7-119">*expressão* = de *elemento*. gama</span><span class="sxs-lookup"><span data-stu-id="1f1a7-119">*expression*=*element*.gamma</span></span>

<span data-ttu-id="1f1a7-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1f1a7-120">**Remarks**</span></span>

<span data-ttu-id="1f1a7-121">Diminuir o gama abaixo 1 modifica uma imagem para torná-la mais contrastantivo, enquanto valores maiores que 1 diminuem o contraste.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-121">Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast.</span></span> <span data-ttu-id="1f1a7-122">Os valores úteis são de 0,3 a aproximadamente 3.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-122">Useful values are from 0.3 to about 3.</span></span> <span data-ttu-id="1f1a7-123">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="1f1a7-123">The default value is 0.</span></span>

<span data-ttu-id="1f1a7-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="1f1a7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="1f1a7-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1f1a7-125">**Example**</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 