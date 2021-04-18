---
description: O DirectXMath fornece uma solução matemática otimizada para o Windows.
ms.assetid: c2a64435-b2fb-3638-2eea-3ed52f4c7cd5
title: Guia de programação do DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df406787776f9fa5d1786e6ed6c5998e27a1c059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780081"
---
# <a name="directxmath-programming-guide"></a><span data-ttu-id="cc616-103">Guia de programação do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="cc616-103">DirectXMath programming guide</span></span>

<span data-ttu-id="cc616-104">O DirectXMath fornece uma solução matemática otimizada para o Windows.</span><span class="sxs-lookup"><span data-stu-id="cc616-104">DirectXMath provides a math solution optimized for Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cc616-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="cc616-105">In this section</span></span>



| <span data-ttu-id="cc616-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="cc616-106">Topic</span></span>                                                             | <span data-ttu-id="cc616-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc616-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc616-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="cc616-108">Getting Started</span></span>](pg-xnamath-getting-started.md)<br/>      | <span data-ttu-id="cc616-109">A biblioteca DirectXMath implementa uma interface ideal e portátil para operações de algebra aritméticos e lineares em vetores de ponto flutuante de precisão simples (2D, 3D e 4D) ou matrizes (3 × 3 e 4 × 4).</span><span class="sxs-lookup"><span data-stu-id="cc616-109">The DirectXMath Library implements an optimal and portable interface for arithmetic and linear algebra operations on single-precision floating-point vectors (2D, 3D, and 4D) or matrices (3×3 and 4×4).</span></span> <br/>                                                    |
| [<span data-ttu-id="cc616-110">Novidades</span><span class="sxs-lookup"><span data-stu-id="cc616-110">What's New</span></span>](pg-xnamath-whatsnew.md)<br/>                  | <span data-ttu-id="cc616-111">A biblioteca DirectXMath é baseada na [biblioteca de matemática do XNA C++ SIMD versão 2, 4](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="cc616-111">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="cc616-112">Aqui, descrevemos como o DirectXMath difere do XNA Math e como as versões do DirectXMath são diferentes.</span><span class="sxs-lookup"><span data-stu-id="cc616-112">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span> <br/> |
| [<span data-ttu-id="cc616-113">Migração de código</span><span class="sxs-lookup"><span data-stu-id="cc616-113">Code Migration</span></span>](pg-xnamath-migration.md)<br/>             | <span data-ttu-id="cc616-114">Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática do XNA para a biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="cc616-114">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="cc616-115">Trabalhando com D3DXMath</span><span class="sxs-lookup"><span data-stu-id="cc616-115">Working with D3DXMath</span></span>](pg-xnamath-migration-d3dx.md)<br/> | <span data-ttu-id="cc616-116">D3DXMath é uma biblioteca auxiliar matemática para aplicativos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cc616-116">D3DXMath is a math helper library for Direct3D applications.</span></span> <br/>                                                                                                                                                                                                |
| [<span data-ttu-id="cc616-117">Otimização de código</span><span class="sxs-lookup"><span data-stu-id="cc616-117">Code Optimization</span></span>](pg-xnamath-optimizing.md)<br/>         | <span data-ttu-id="cc616-118">Este tópico descreve as considerações e as estratégias de otimização com a biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="cc616-118">This topic describes optimization considerations and strategies with the DirectXMath Library.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="cc616-119">Elementos internos da biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc616-119">Library Internals</span></span>](pg-xnamath-internals.md)<br/>          | <span data-ttu-id="cc616-120">Este tópico descreve o design interno da biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="cc616-120">This topic describes the internal design of the DirectXMath library.</span></span><br/>                                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="cc616-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc616-121">Related Topics</span></span>

<dl> <dt>

<span data-ttu-id="cc616-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[Referência de programação DirectXMath](ovw-xnamath-reference.md)</span><span class="sxs-lookup"><span data-stu-id="cc616-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath Programming Reference](ovw-xnamath-reference.md)</span></span>
<span data-ttu-id="cc616-123"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cc616-123"></dt> <dd></dd> </dl></span></span>

## <a name="related-topics"></a><span data-ttu-id="cc616-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc616-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc616-125">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="cc616-125">DirectXMath</span></span>](directxmath-portal.md)
</dt> </dl>

 

 




