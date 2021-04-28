---
description: LPD3DXFILL3D-tipo de função usado pelas funções de preenchimento de textura.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c711459cffa3430b31ba7c91d77cc9519e6a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114304"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="da70a-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="da70a-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="da70a-104">Tipo de função usado pelas funções de preenchimento de textura.</span><span class="sxs-lookup"><span data-stu-id="da70a-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="da70a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da70a-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="da70a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da70a-106">Parameters</span></span>

<span data-ttu-id="da70a-107">pOut-ponteiro para um vetor, que a função usa para retornar seu resultado.</span><span class="sxs-lookup"><span data-stu-id="da70a-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="da70a-108">X, Y, Z e W serão mapeados para R, G, B e A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="da70a-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="da70a-109">pTexCoord-ponteiro para um vetor que contém as coordenadas do Texel que está sendo avaliado no momento.</span><span class="sxs-lookup"><span data-stu-id="da70a-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="da70a-110">Os componentes de coordenadas de textura para textura e texturas de volume variam de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="da70a-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="da70a-111">Os componentes da coordenada de textura para texturas de cubo variam de-1 a 1.</span><span class="sxs-lookup"><span data-stu-id="da70a-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="da70a-112">pTexelSize-ponteiro para um vetor que contém as dimensões do Texel atual.</span><span class="sxs-lookup"><span data-stu-id="da70a-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="da70a-113">pData-ponteiro para dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="da70a-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="da70a-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="da70a-114">Return Value</span></span>

<span data-ttu-id="da70a-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="da70a-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da70a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="da70a-116">Remarks</span></span>

<span data-ttu-id="da70a-117">Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="da70a-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="da70a-118">Caso contrário, podem ocorrer estouros de pilha.</span><span class="sxs-lookup"><span data-stu-id="da70a-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="da70a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da70a-119">Header</span></span>                   | <span data-ttu-id="da70a-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="da70a-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="da70a-121">Bibliotecas de importação</span><span class="sxs-lookup"><span data-stu-id="da70a-121">Import Library</span></span>           | <span data-ttu-id="da70a-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="da70a-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="da70a-123">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="da70a-123">Minimum Operating System</span></span> | <span data-ttu-id="da70a-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="da70a-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="da70a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da70a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da70a-126">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="da70a-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="da70a-127">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="da70a-127">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
