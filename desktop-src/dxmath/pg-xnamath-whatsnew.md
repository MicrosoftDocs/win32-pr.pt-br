---
description: A biblioteca DirectXMath baseia-se na biblioteca matemática do XNA C++ SIMD versão 2. x. Aqui, descrevemos como o DirectXMath difere do XNA Math e como as versões do DirectXMath são diferentes.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: O que há de novo (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813511"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="1dbdc-104">O que há de novo (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="1dbdc-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="1dbdc-105">A biblioteca DirectXMath é baseada na [biblioteca de matemática do XNA C++ SIMD versão 2, 4](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="1dbdc-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="1dbdc-106">Aqui, descrevemos como o DirectXMath difere do XNA Math e como as versões do DirectXMath são diferentes.</span><span class="sxs-lookup"><span data-stu-id="1dbdc-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="1dbdc-107">Histórico de rlease</span><span class="sxs-lookup"><span data-stu-id="1dbdc-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="1dbdc-108">Diferenças de DirectXMath do XNA Math</span><span class="sxs-lookup"><span data-stu-id="1dbdc-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="1dbdc-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dbdc-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="1dbdc-110">Histórico de versões</span><span class="sxs-lookup"><span data-stu-id="1dbdc-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="1dbdc-111">SDK de atualização do Windows 10 pode 2020</span><span class="sxs-lookup"><span data-stu-id="1dbdc-111">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="1dbdc-112">DirectXMath 3,14</span><span class="sxs-lookup"><span data-stu-id="1dbdc-112">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-113">SDK de atualização do Windows 10 de outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="1dbdc-113">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="1dbdc-114">DirectXMath 3,13</span><span class="sxs-lookup"><span data-stu-id="1dbdc-114">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-115">SDK de atualização de abril de 2018 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="1dbdc-115">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="1dbdc-116">SDK de atualização dos criadores de outono do Windows 10</span><span class="sxs-lookup"><span data-stu-id="1dbdc-116">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="1dbdc-117">DirectXMath 3,11</span><span class="sxs-lookup"><span data-stu-id="1dbdc-117">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-118">SDK de atualização do Windows 10 para criadores</span><span class="sxs-lookup"><span data-stu-id="1dbdc-118">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="1dbdc-119">DirectXMath 3,10</span><span class="sxs-lookup"><span data-stu-id="1dbdc-119">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-120">SDK de aniversário do Windows 10</span><span class="sxs-lookup"><span data-stu-id="1dbdc-120">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="1dbdc-121">DirectXMath 3, 9</span><span class="sxs-lookup"><span data-stu-id="1dbdc-121">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-122">SDK do Windows 10 (novembro de 2015)</span><span class="sxs-lookup"><span data-stu-id="1dbdc-122">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="1dbdc-123">DirectXMath 3, 8</span><span class="sxs-lookup"><span data-stu-id="1dbdc-123">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-124">SDK do Windows para Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="1dbdc-124">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="1dbdc-125">DirectXMath 3, 7</span><span class="sxs-lookup"><span data-stu-id="1dbdc-125">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-126">SDK do Windows para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1dbdc-126">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="1dbdc-127">DirectXMath 3, 6</span><span class="sxs-lookup"><span data-stu-id="1dbdc-127">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="1dbdc-128">SDK do Windows para Windows 8</span><span class="sxs-lookup"><span data-stu-id="1dbdc-128">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="1dbdc-129">DirectXMath 3, 3</span><span class="sxs-lookup"><span data-stu-id="1dbdc-129">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="1dbdc-130">Consulte [versões do DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1dbdc-130">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="1dbdc-131">Diferenças de DirectXMath do XNA Math</span><span class="sxs-lookup"><span data-stu-id="1dbdc-131">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="1dbdc-132">Veja como a biblioteca DirectXMath é basicamente diferente da biblioteca de matemática do XNA:</span><span class="sxs-lookup"><span data-stu-id="1dbdc-132">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="1dbdc-133">DirectXMath é apenas C++ (namespaces, sobrecargas, novos modelos e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1dbdc-133">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="1dbdc-134">Requer suporte à biblioteca padrão do C++ 11 (ou seja, stdint. h e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1dbdc-134">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="1dbdc-135">O ARM-NEON intrínseco dá suporte para a plataforma Windows RT.</span><span class="sxs-lookup"><span data-stu-id="1dbdc-135">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="1dbdc-136">Nova funcionalidade de cor (conversões de espaço de cor, constantes de cor do .NET).</span><span class="sxs-lookup"><span data-stu-id="1dbdc-136">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="1dbdc-137">Tipos de volume delimitador (uma versão do que estava anteriormente no cabeçalho XNACollision no exemplo de colisão do SDK do DirectX).</span><span class="sxs-lookup"><span data-stu-id="1dbdc-137">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="1dbdc-138">Nenhuma versão do Xbox 360 está disponível.</span><span class="sxs-lookup"><span data-stu-id="1dbdc-138">No Xbox 360 version is available.</span></span> <span data-ttu-id="1dbdc-139">O XDK do Xbox 360 continua a lançar o XNAMath v2. x; remoção de tipos de dados específicos do Xbox 360 e variantes de função.</span><span class="sxs-lookup"><span data-stu-id="1dbdc-139">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="1dbdc-140">[**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) retrabalhada para uma otimização aprimorada para os intrínsecos SSE e ARM-Neon.</span><span class="sxs-lookup"><span data-stu-id="1dbdc-140">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="1dbdc-141">O tipo [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) é totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="1dbdc-141">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="1dbdc-142">Para acessar elementos individuais do **XMMATRIX**, use outros tipos, como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="1dbdc-142">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dbdc-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dbdc-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dbdc-144">Guia de programação do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="1dbdc-144">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="1dbdc-145">Versões do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="1dbdc-145">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
