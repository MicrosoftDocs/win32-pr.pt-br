---
title: Função WavePrefixCountBits
description: Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as pistas ativas com índices menores que a raia atual.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- HLSL da função WavePrefixCountBits
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008603"
---
# <a name="waveprefixcountbits-function"></a><span data-ttu-id="1ce9c-104">Função WavePrefixCountBits</span><span class="sxs-lookup"><span data-stu-id="1ce9c-104">WavePrefixCountBits function</span></span>

<span data-ttu-id="1ce9c-105">Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as pistas ativas com índices menores que a raia atual.</span><span class="sxs-lookup"><span data-stu-id="1ce9c-105">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce9c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ce9c-106">Syntax</span></span>


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="1ce9c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ce9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ce9c-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="1ce9c-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="1ce9c-109">As variáveis Booleanas especificadas.</span><span class="sxs-lookup"><span data-stu-id="1ce9c-109">The specified boolean variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ce9c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ce9c-110">Return value</span></span>

<span data-ttu-id="1ce9c-111">A soma de todas as variáveis Booleanas especificadas definidas como true em todas as pistas ativas com índices menores que a pista atual.</span><span class="sxs-lookup"><span data-stu-id="1ce9c-111">The sum of all the specified Boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ce9c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ce9c-112">Remarks</span></span>

<span data-ttu-id="1ce9c-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1ce9c-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="1ce9c-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ce9c-114">Examples</span></span>

<span data-ttu-id="1ce9c-115">O código a seguir descreve como implementar uma gravação compactada em um fluxo ordenado em que o número de elementos gravados por Lane é 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="1ce9c-115">The following code describes how to implement a compacted write to an ordered stream where the number of elements written per lane is either 1 or 0.</span></span>

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a><span data-ttu-id="1ce9c-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ce9c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce9c-117">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1ce9c-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="1ce9c-118">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1ce9c-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




