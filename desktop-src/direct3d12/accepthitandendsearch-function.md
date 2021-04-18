---
description: Usado em um sombreador qualquer ocorrência para confirmar a ocorrência atual e, em seguida, parar de Pesquisar mais ocorrências para Ray.
ms.assetid: ''
title: Função AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751747"
---
# <a name="accepthitandendsearch-function"></a><span data-ttu-id="da089-103">Função AcceptHitAndEndSearch</span><span class="sxs-lookup"><span data-stu-id="da089-103">AcceptHitAndEndSearch function</span></span>

<span data-ttu-id="da089-104">Usado em um [sombreador qualquer ocorrência](any-hit-shader.md) para confirmar a ocorrência atual e, em seguida, parar de Pesquisar mais ocorrências para Ray.</span><span class="sxs-lookup"><span data-stu-id="da089-104">Used in an [any hit shader](any-hit-shader.md) to commit the current hit and then stop searching for more hits for the ray.</span></span> <span data-ttu-id="da089-105">Se houver um sombreador de interseção em execução, a execução será interrompida.</span><span class="sxs-lookup"><span data-stu-id="da089-105">If there is an intersection shader running, it's execution stops.</span></span>  <span data-ttu-id="da089-106">A execução passa para o [sombreador de clique mais próximo](closest-hit-shader.md), se habilitado, com a visita mais próxima registrada até agora.</span><span class="sxs-lookup"><span data-stu-id="da089-106">Execution passes to the [closest hit shader](closest-hit-shader.md), if enabled, with the closest hit recorded so far.</span></span>

## <a name="syntax"></a><span data-ttu-id="da089-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da089-107">Syntax</span></span>

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a><span data-ttu-id="da089-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="da089-108">Return Value</span></span>

<span data-ttu-id="da089-109">**void**</span><span class="sxs-lookup"><span data-stu-id="da089-109">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="da089-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="da089-110">Remarks</span></span>

<span data-ttu-id="da089-111">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="da089-111">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="da089-112">**Sombreador resgatável**</span><span class="sxs-lookup"><span data-stu-id="da089-112">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="da089-113">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="da089-113">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="da089-114">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="da089-114">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="da089-115">**Sombreador da geração de raio**</span><span class="sxs-lookup"><span data-stu-id="da089-115">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="da089-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="da089-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da089-117">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="da089-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




