---
title: Atributo de matriz (sombra) (VML)
description: Atributo de matriz (sombra) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366620"
---
# <a name="matrix-attribute-shadowvml"></a><span data-ttu-id="f1d1e-103">Atributo de matriz (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="f1d1e-103">Matrix Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="f1d1e-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f1d1e-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f1d1e-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f1d1e-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f1d1e-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f1d1e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f1d1e-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f1d1e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f1d1e-110">Define uma transformação de perspectiva para uma sombra.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-110">Defines a perspective transform for a shadow.</span></span> <span data-ttu-id="f1d1e-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-111">Read/write.</span></span> <span data-ttu-id="f1d1e-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-112">**String**.</span></span>

<span data-ttu-id="f1d1e-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="f1d1e-113">**Applies To**</span></span>

[<span data-ttu-id="f1d1e-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="f1d1e-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="f1d1e-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="f1d1e-115">**Tag Syntax**</span></span>

<span data-ttu-id="f1d1e-116"><v: *Element* matriz = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f1d1e-116"><v: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="f1d1e-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="f1d1e-117">**Script Syntax**</span></span>

<span data-ttu-id="f1d1e-118">*Element* . Matrix = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="f1d1e-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="f1d1e-119">*expressão* = de *elemento*. Matrix</span><span class="sxs-lookup"><span data-stu-id="f1d1e-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="f1d1e-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="f1d1e-120">**Remarks**</span></span>

<span data-ttu-id="f1d1e-121">Uma matriz de transformação de perspectiva no formato "Sxx, SXY, syx, syy, px, py", em que s = Scale e p = Perspective.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-121">A perspective transform matrix in the form "sxx,sxy,syx,syy,px,py" where s= scale and p = perspective.</span></span> <span data-ttu-id="f1d1e-122">Se o deslocamento estiver em unidades absolutas, então px, py estão em unidades de 1/emu; caso contrário, eles são uma fração inversa do tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-122">If offset is in absolute units then px, py are in 1/emu units; otherwise they are an inverse fraction of the shape size.</span></span>

<span data-ttu-id="f1d1e-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="f1d1e-123">*VML Standard Attribute*</span></span>

 

 