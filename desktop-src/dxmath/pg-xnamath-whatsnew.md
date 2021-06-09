---
description: A biblioteca DirectXMath baseia-se na biblioteca SIMD do XNA Math C++ versão 2.x. Aqui, descrevemos como o DirectXMath difere da Matemática XNA e como as versões do DirectXMath diferem.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novidades (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827622"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="c269c-104">Novidades (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="c269c-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="c269c-105">A biblioteca DirectXMath baseia-se na biblioteca [SIMD C++ matemática XNA versão 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span><span class="sxs-lookup"><span data-stu-id="c269c-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span></span> <span data-ttu-id="c269c-106">Aqui, descrevemos como o DirectXMath difere da Matemática XNA e como as versões do DirectXMath diferem.</span><span class="sxs-lookup"><span data-stu-id="c269c-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="c269c-107">Histórico de lançamento</span><span class="sxs-lookup"><span data-stu-id="c269c-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="c269c-108">Diferenças do DirectXMath em relação à matemática XNA</span><span class="sxs-lookup"><span data-stu-id="c269c-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="c269c-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c269c-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="c269c-110">Histórico de versões</span><span class="sxs-lookup"><span data-stu-id="c269c-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="c269c-111">Windows 10 SDK (20348), versão 2104</span><span class="sxs-lookup"><span data-stu-id="c269c-111">Windows 10 SDK (20348), version 2104</span></span></td><td><span data-ttu-id="c269c-112">DirectXMath 3.16</span><span class="sxs-lookup"><span data-stu-id="c269c-112">DirectXMath 3.16</span></span></td>
 </td>
 <tr>
  <td><span data-ttu-id="c269c-113">Windows 10 SDK de Atualização de maio de 2020</span><span class="sxs-lookup"><span data-stu-id="c269c-113">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="c269c-114">DirectXMath 3.14</span><span class="sxs-lookup"><span data-stu-id="c269c-114">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-115">Atualização de outubro de 2018 para o Windows 10 SDK</span><span class="sxs-lookup"><span data-stu-id="c269c-115">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="c269c-116">DirectXMath 3.13</span><span class="sxs-lookup"><span data-stu-id="c269c-116">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-117">SDK do Atualização de abril de 2018 para o Windows 10</span><span class="sxs-lookup"><span data-stu-id="c269c-117">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="c269c-118">Windows 10 Fall Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="c269c-118">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="c269c-119">DirectXMath 3.11</span><span class="sxs-lookup"><span data-stu-id="c269c-119">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-120">SDK do Atualização do Windows 10 para Criadores</span><span class="sxs-lookup"><span data-stu-id="c269c-120">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="c269c-121">DirectXMath 3.10</span><span class="sxs-lookup"><span data-stu-id="c269c-121">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-122">SDK Windows 10 Aniversário do Windows 10</span><span class="sxs-lookup"><span data-stu-id="c269c-122">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="c269c-123">DirectXMath 3.09</span><span class="sxs-lookup"><span data-stu-id="c269c-123">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-124">Windows 10 SDK (novembro de 2015)</span><span class="sxs-lookup"><span data-stu-id="c269c-124">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="c269c-125">DirectXMath 3.08</span><span class="sxs-lookup"><span data-stu-id="c269c-125">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-126">SDK do Windows para Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="c269c-126">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="c269c-127">DirectXMath 3.07</span><span class="sxs-lookup"><span data-stu-id="c269c-127">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-128">SDK do Windows para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c269c-128">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="c269c-129">DirectXMath 3.06</span><span class="sxs-lookup"><span data-stu-id="c269c-129">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="c269c-130">SDK do Windows para Windows 8</span><span class="sxs-lookup"><span data-stu-id="c269c-130">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="c269c-131">DirectXMath 3.03</span><span class="sxs-lookup"><span data-stu-id="c269c-131">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="c269c-132">Confira [versões do DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c269c-132">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="c269c-133">Diferenças do DirectXMath em relação à matemática XNA</span><span class="sxs-lookup"><span data-stu-id="c269c-133">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="c269c-134">Veja como a biblioteca DirectXMath difere principalmente da biblioteca matemática XNA:</span><span class="sxs-lookup"><span data-stu-id="c269c-134">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="c269c-135">DirectXMath é somente C++ (namespaces, sobrecargas, novos modelos e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c269c-135">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="c269c-136">Requer suporte à biblioteca padrão do C++11 (ou seja, stdint.h e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c269c-136">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="c269c-137">Suporte a intrínsecos arm-NEON para a Windows RT de dados.</span><span class="sxs-lookup"><span data-stu-id="c269c-137">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="c269c-138">Nova funcionalidade de cor (conversões de espaço em cores, constantes de cores do .NET).</span><span class="sxs-lookup"><span data-stu-id="c269c-138">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="c269c-139">Tipos de volume delimitador (uma versão do que estava anteriormente no header XNACollision no exemplo de Colisão do SDK do DirectX).</span><span class="sxs-lookup"><span data-stu-id="c269c-139">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="c269c-140">Nenhuma Xbox 360 está disponível.</span><span class="sxs-lookup"><span data-stu-id="c269c-140">No Xbox 360 version is available.</span></span> <span data-ttu-id="c269c-141">O Xbox 360 XDK continua a enviar XNAMath v2.x; remoção de Xbox 360 tipos de dados específicos e variantes de função.</span><span class="sxs-lookup"><span data-stu-id="c269c-141">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="c269c-142">[**XMVectorPermute retrabalhado para**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) otimização aprimorada para intrínsecos SSE e ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="c269c-142">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="c269c-143">O [**tipo XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) é totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="c269c-143">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="c269c-144">Para acessar elementos individuais **do XMMATRIX,** use outros tipos, como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="c269c-144">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c269c-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c269c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c269c-146">Guia de Programação do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="c269c-146">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="c269c-147">Versões do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="c269c-147">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
