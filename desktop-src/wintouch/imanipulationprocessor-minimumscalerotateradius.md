---
title: Propriedade IManipulationProcessor MinimumScaleRotateRadius
description: Especifica a grande quantidade de contatos de distância em um gesto de escala ou de giro precisar ser para disparar a manipulação.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Propriedade MinimumScaleRotateRadius Windows Touch
- Propriedade MinimumScaleRotateRadius Windows Touch, interface IManipulationProcessor
- IManipulationProcessor interface Windows Touch, Propriedade MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638608"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a><span data-ttu-id="96aab-106">Propriedade IManipulationProcessor:: MinimumScaleRotateRadius</span><span class="sxs-lookup"><span data-stu-id="96aab-106">IManipulationProcessor::MinimumScaleRotateRadius property</span></span>

<span data-ttu-id="96aab-107">Especifica a grande quantidade de contatos de distância em um gesto de escala ou de giro precisar ser para disparar a manipulação.</span><span class="sxs-lookup"><span data-stu-id="96aab-107">Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.</span></span>

<span data-ttu-id="96aab-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="96aab-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="96aab-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96aab-109">Syntax</span></span>


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a><span data-ttu-id="96aab-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="96aab-110">Property value</span></span>

<span data-ttu-id="96aab-111">Especifica a distância mínima entre os contatos para disparar gestos de escala ou de giro.</span><span class="sxs-lookup"><span data-stu-id="96aab-111">Specifies the minimum distance between contacts to trigger scale or rotate gestures.</span></span>

## <a name="error-codes"></a><span data-ttu-id="96aab-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="96aab-112">Error codes</span></span>

## <a name="remarks"></a><span data-ttu-id="96aab-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="96aab-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96aab-114">Essa propriedade é definida em centipixels (100ths de um pixel).</span><span class="sxs-lookup"><span data-stu-id="96aab-114">This property is set in centipixels (100ths of a pixel).</span></span>

 

<span data-ttu-id="96aab-115">Definir esse valor fará com que o processador de manipulação ignore gestos com um raio muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="96aab-115">Setting this value will make the manipulation processor ignore gestures that have too small of a radius.</span></span> <span data-ttu-id="96aab-116">Isso será útil se você quiser impedir que um usuário manipule um objeto em um raio muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="96aab-116">This is useful if you want to prevent a user from manipulating an object to too small of a radius.</span></span> <span data-ttu-id="96aab-117">Por exemplo, se você estiver usando um processador de manipulação com um círculo e quiser garantir que ele mantenha um raio maior que 100 pixels, você definirá esse valor como 10000.</span><span class="sxs-lookup"><span data-stu-id="96aab-117">For example, if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater than 100 pixels, you would set this value to 10000.</span></span>

## <a name="examples"></a><span data-ttu-id="96aab-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96aab-118">Examples</span></span>


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a><span data-ttu-id="96aab-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="96aab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96aab-120">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="96aab-120">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




