---
title: Atributo de impressão de VML
description: Atributo de impressão de VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810276"
---
# <a name="vml-print-attribute"></a><span data-ttu-id="f6146-103">Atributo de impressão de VML</span><span class="sxs-lookup"><span data-stu-id="f6146-103">VML Print Attribute</span></span>

<span data-ttu-id="f6146-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f6146-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f6146-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f6146-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f6146-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f6146-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f6146-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f6146-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f6146-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f6146-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f6146-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f6146-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f6146-110">Determina se a forma será impressa.</span><span class="sxs-lookup"><span data-stu-id="f6146-110">Determines whether the shape will be printed.</span></span> <span data-ttu-id="f6146-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f6146-111">Read/write.</span></span> <span data-ttu-id="f6146-112">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="f6146-112">[VgTriState](msdn-online-vml-vgtristate.md).</span></span>

<span data-ttu-id="f6146-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="f6146-113">**Applies To**</span></span>

[<span data-ttu-id="f6146-114">Forma</span><span class="sxs-lookup"><span data-stu-id="f6146-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f6146-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="f6146-115">**Tag Syntax**</span></span>

<span data-ttu-id="f6146-116"><v: *elemento* Print = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="f6146-116"><v: *element* print=" *expression* "></span></span>

<span data-ttu-id="f6146-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="f6146-117">**Script Syntax**</span></span>

<span data-ttu-id="f6146-118">*elemento* . Print = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="f6146-118">*element* .print="*expression*"</span></span>

<span data-ttu-id="f6146-119">*expressão* = de *elemento*. Print</span><span class="sxs-lookup"><span data-stu-id="f6146-119">*expression*=*element*.print</span></span>

<span data-ttu-id="f6146-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="f6146-120">**Remarks**</span></span>

<span data-ttu-id="f6146-121">Fornecido como uma maneira de especificar se as formas serão impressas.</span><span class="sxs-lookup"><span data-stu-id="f6146-121">Provided as a way to specify whether shapes will be printed.</span></span> <span data-ttu-id="f6146-122">Observe que uma forma ainda pode ser exibida na tela, mesmo que não seja impressa como resultado desse atributo ser **falso**.</span><span class="sxs-lookup"><span data-stu-id="f6146-122">Note that a shape can still be displayed on the screen, even if it is not printed as a result of this attribute being **False**.</span></span> <span data-ttu-id="f6146-123">O valor padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="f6146-123">The default value is **True**.</span></span>

<span data-ttu-id="f6146-124">Esse atributo é usado pelo Microsoft Office, mas não é usado pelo Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f6146-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="f6146-125">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="f6146-125">*Microsoft Office Extensions Attribute*</span></span>

 

 