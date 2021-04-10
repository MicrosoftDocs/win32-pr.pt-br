---
description: Tipo de função usado pelas funções de preenchimento de textura.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8c9d9ef610ee10faa069841a05f43c17b0885c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163735"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="e4002-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="e4002-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="e4002-104">Tipo de função usado pelas funções de preenchimento de textura.</span><span class="sxs-lookup"><span data-stu-id="e4002-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4002-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4002-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="e4002-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4002-106">Parameters</span></span>

<span data-ttu-id="e4002-107">pOut-ponteiro para um vetor, que a função usa para retornar seu resultado.</span><span class="sxs-lookup"><span data-stu-id="e4002-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="e4002-108">X, Y, Z e W serão mapeados para R, G, B e A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e4002-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="e4002-109">pTexCoord-ponteiro para um vetor que contém as coordenadas do Texel que está sendo avaliado no momento.</span><span class="sxs-lookup"><span data-stu-id="e4002-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="e4002-110">Os componentes de coordenadas de textura para textura e texturas de volume variam de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="e4002-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="e4002-111">Os componentes da coordenada de textura para texturas de cubo variam de-1 a 1.</span><span class="sxs-lookup"><span data-stu-id="e4002-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="e4002-112">pTexelSize-ponteiro para um vetor que contém as dimensões do Texel atual.</span><span class="sxs-lookup"><span data-stu-id="e4002-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="e4002-113">pData-ponteiro para dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="e4002-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4002-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e4002-114">Return Value</span></span>

<span data-ttu-id="e4002-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e4002-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4002-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4002-116">Remarks</span></span>

<span data-ttu-id="e4002-117">Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4002-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="e4002-118">Caso contrário, podem ocorrer estouros de pilha.</span><span class="sxs-lookup"><span data-stu-id="e4002-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e4002-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4002-119">Header</span></span>                   | <span data-ttu-id="e4002-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="e4002-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="e4002-121">Bibliotecas de importação</span><span class="sxs-lookup"><span data-stu-id="e4002-121">Import Library</span></span>           | <span data-ttu-id="e4002-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="e4002-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="e4002-123">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="e4002-123">Minimum Operating System</span></span> | <span data-ttu-id="e4002-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e4002-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e4002-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4002-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4002-126">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="e4002-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="e4002-127">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="e4002-127">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
