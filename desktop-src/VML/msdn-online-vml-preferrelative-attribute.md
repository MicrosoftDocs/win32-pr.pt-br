---
title: Atributo PreferRelative de VML
description: Atributo PreferRelative de VML
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007642"
---
# <a name="vml-preferrelative-attribute"></a><span data-ttu-id="0c176-103">Atributo PreferRelative de VML</span><span class="sxs-lookup"><span data-stu-id="0c176-103">VML PreferRelative Attribute</span></span>

<span data-ttu-id="0c176-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0c176-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0c176-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0c176-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0c176-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0c176-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0c176-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0c176-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0c176-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0c176-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0c176-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0c176-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0c176-110">Determina se o tamanho original de um objeto é salvo após a reformatação.</span><span class="sxs-lookup"><span data-stu-id="0c176-110">Determines whether the original size of an object is saved after reformatting.</span></span> <span data-ttu-id="0c176-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0c176-111">Read/write.</span></span> <span data-ttu-id="0c176-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="0c176-112">**VgTriState**.</span></span>

<span data-ttu-id="0c176-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0c176-113">**Applies To**</span></span>

[<span data-ttu-id="0c176-114">Forma</span><span class="sxs-lookup"><span data-stu-id="0c176-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0c176-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0c176-115">**Tag Syntax**</span></span>

<span data-ttu-id="0c176-116"><v: *Element* o:preferrelative = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="0c176-116"><v: *element* o:preferrelative=" *expression* "></span></span>

<span data-ttu-id="0c176-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0c176-117">**Remarks**</span></span>

<span data-ttu-id="0c176-118">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="0c176-118">The default is **False**.</span></span> <span data-ttu-id="0c176-119">Se **for true**, o tamanho original do objeto será armazenado e todo o redimensionamento será baseado em uma porcentagem desse tamanho original.</span><span class="sxs-lookup"><span data-stu-id="0c176-119">If **True**, the original size of the object will be stored and all resizing will be based on a percentage of that original size.</span></span> <span data-ttu-id="0c176-120">Caso contrário, cada redimensionamento redefinirá a escala para 100%.</span><span class="sxs-lookup"><span data-stu-id="0c176-120">Otherwise, each resizing will reset the scale to 100%.</span></span>

<span data-ttu-id="0c176-121">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="0c176-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="0c176-122">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0c176-122">**Example**</span></span>

<span data-ttu-id="0c176-123">Se a forma for redimensionada, o tamanho original não será armazenado.</span><span class="sxs-lookup"><span data-stu-id="0c176-123">If the shape is resized, the original size will not be stored.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 