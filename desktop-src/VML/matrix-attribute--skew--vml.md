---
title: Atributo de matriz (distorção) (VML)
description: Atributo de matriz (distorção) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008072"
---
# <a name="matrix-attribute-skewvml"></a><span data-ttu-id="f1e7d-103">Atributo de matriz (distorção) (VML)</span><span class="sxs-lookup"><span data-stu-id="f1e7d-103">Matrix Attribute (Skew)(VML)</span></span>

<span data-ttu-id="f1e7d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f1e7d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f1e7d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f1e7d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f1e7d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f1e7d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f1e7d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f1e7d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f1e7d-110">Define uma transformação de perspectiva de uma distorção.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-110">Defines a perspective transform of a skew.</span></span> <span data-ttu-id="f1e7d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-111">Read/write.</span></span> <span data-ttu-id="f1e7d-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-112">**String**.</span></span>

<span data-ttu-id="f1e7d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="f1e7d-113">**Applies To**</span></span>

[<span data-ttu-id="f1e7d-114">Inclinar</span><span class="sxs-lookup"><span data-stu-id="f1e7d-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="f1e7d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="f1e7d-115">**Tag Syntax**</span></span>

<span data-ttu-id="f1e7d-116"><o: *Element* matriz = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f1e7d-116"><o: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="f1e7d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="f1e7d-117">**Script Syntax**</span></span>

<span data-ttu-id="f1e7d-118">*Element* . Matrix = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="f1e7d-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="f1e7d-119">*expressão* = de *elemento*. Matrix</span><span class="sxs-lookup"><span data-stu-id="f1e7d-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="f1e7d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="f1e7d-120">**Remarks**</span></span>

<span data-ttu-id="f1e7d-121">A matriz é uma cadeia de caracteres no formato "Sxx, SXY, syx, syy, px, py", em que s é escala, p é perspectiva e x e y são valores x e y.</span><span class="sxs-lookup"><span data-stu-id="f1e7d-121">The matrix is a string in the form "sxx, sxy, syx, syy, px, py" where s is scale, p is perspective, and x and y are x and y values.</span></span> <span data-ttu-id="f1e7d-122">Se o [deslocamento](offset-attribute--skew--vml.md) estiver em unidades absolutas, PX e py estão nas [unidades](msdn-online-vml-units.md) da UME ^-1 (caso contrário, eles são uma fração inversa do tamanho da forma).</span><span class="sxs-lookup"><span data-stu-id="f1e7d-122">If [Offset](offset-attribute--skew--vml.md) is in absolute units, then px and py are in emu^-1 [units](msdn-online-vml-units.md) (otherwise they are an inverse fraction of the shape size).</span></span> <span data-ttu-id="f1e7d-123">O valor padrão é "1, 0, 0, 1, 0, 0".</span><span class="sxs-lookup"><span data-stu-id="f1e7d-123">The default value is "1,0,0,1,0,0".</span></span>

<span data-ttu-id="f1e7d-124">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="f1e7d-124">*Microsoft Office Extensions Attribute*</span></span>

 

 