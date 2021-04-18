---
description: Protótipo de função usado pelo D3DXComputeIMTFromSignal para descrever um sinal definido pelo usuário em um u, espaço v de malha de entrada. A função avalia um sinal de procedimento de uSignalDimension de dimensão na coordenada u, v fornecida.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808297"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="15ea3-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="15ea3-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="15ea3-105">Protótipo de função usado pelo [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) para descrever um sinal definido pelo usuário em um u, espaço v de malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="15ea3-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="15ea3-106">A função avalia um sinal de procedimento de uSignalDimension de dimensão na coordenada u, v fornecida.</span><span class="sxs-lookup"><span data-stu-id="15ea3-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ea3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15ea3-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="15ea3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15ea3-108">Parameters</span></span>

<span data-ttu-id="15ea3-109">\[em \] UV-um ponteiro para um vetor que contém a coordenada de textura de vértice.</span><span class="sxs-lookup"><span data-stu-id="15ea3-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="15ea3-110">\[em \] uPrimitiveId-o índice do triângulo de entrada na malha para a qual o sinal deve ser calculado.</span><span class="sxs-lookup"><span data-stu-id="15ea3-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="15ea3-111">\[em \] uSignalDimension-o número de floats para armazenar na matriz de dados de sinal (pfSignalOut).</span><span class="sxs-lookup"><span data-stu-id="15ea3-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="15ea3-112">\[em \] pUserData-o ponteiro pUserData passado para [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="15ea3-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="15ea3-113">\[out \] pfSignalOut-uma matriz de floats que contém os dados de sinal.</span><span class="sxs-lookup"><span data-stu-id="15ea3-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="15ea3-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="15ea3-114">Return Value</span></span>

<span data-ttu-id="15ea3-115">Essa função deve ser implementada para retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15ea3-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ea3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="15ea3-116">Remarks</span></span>

<span data-ttu-id="15ea3-117">Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="15ea3-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="15ea3-118">Caso contrário, podem ocorrer estouros de pilha.</span><span class="sxs-lookup"><span data-stu-id="15ea3-118">Otherwise, stack overflows can occur.</span></span>



|                |             |
|----------------|-------------|
| <span data-ttu-id="15ea3-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15ea3-119">Header</span></span>         | <span data-ttu-id="15ea3-120">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="15ea3-120">d3dx9mesh.h</span></span> |
| <span data-ttu-id="15ea3-121">Bibliotecas de importação</span><span class="sxs-lookup"><span data-stu-id="15ea3-121">Import Library</span></span> | <span data-ttu-id="15ea3-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="15ea3-122">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="15ea3-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15ea3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15ea3-124">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="15ea3-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
