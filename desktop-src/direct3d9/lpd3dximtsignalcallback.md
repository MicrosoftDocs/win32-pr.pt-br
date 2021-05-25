---
description: Protótipo de função usado por D3DXComputeIMTFromSignal para descrever um sinal definido pelo usuário no espaço u,v de uma malha de entrada. A função avalia um sinal de procedimento da dimensão uSignalDimension na coordenada u,v fornecida.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342831"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="0dc3c-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="0dc3c-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="0dc3c-105">Protótipo de função usado por [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) para descrever um sinal definido pelo usuário no espaço u,v de uma malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="0dc3c-106">A função avalia um sinal de procedimento da dimensão uSignalDimension na coordenada u,v fornecida.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc3c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0dc3c-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="0dc3c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0dc3c-108">Parameters</span></span>

<span data-ttu-id="0dc3c-109">\[in \] uv – um ponteiro para um vetor que contém a coordenada de textura do vértice.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="0dc3c-110">\[em uPrimitiveId – o índice do triângulo de entrada na malha para o \] qual o sinal deve ser calculado.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="0dc3c-111">\[em uSignalDimension – o número de floats a armazenar na matriz de dados \] de sinal (pfSignalOut).</span><span class="sxs-lookup"><span data-stu-id="0dc3c-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="0dc3c-112">\[em \] pUserData – o ponteiro pUserData passado para [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="0dc3c-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="0dc3c-113">\[out \] pfSignalOut – uma matriz de floats, que contém os dados de sinal.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dc3c-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0dc3c-114">Return Value</span></span>

<span data-ttu-id="0dc3c-115">Essa função deve ser implementada para retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc3c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dc3c-116">Remarks</span></span>

<span data-ttu-id="0dc3c-117">Especifique a convenção de chamada Tipos de [**Dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="0dc3c-118">Caso contrário, podem ocorrer estouros de pilha.</span><span class="sxs-lookup"><span data-stu-id="0dc3c-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="0dc3c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc3c-119">Requirement</span></span>               | <span data-ttu-id="0dc3c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc3c-120">Value</span></span>            |
|----------------|-------------|
| <span data-ttu-id="0dc3c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0dc3c-121">Header</span></span>         | <span data-ttu-id="0dc3c-122">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="0dc3c-122">d3dx9mesh.h</span></span> |
| <span data-ttu-id="0dc3c-123">Bibliotecas de importação</span><span class="sxs-lookup"><span data-stu-id="0dc3c-123">Import Library</span></span> | <span data-ttu-id="0dc3c-124">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="0dc3c-124">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="0dc3c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0dc3c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dc3c-126">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="0dc3c-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
