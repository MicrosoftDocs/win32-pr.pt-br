---
description: Chamado de um sombreador qualquer clique para rejeitar o erro e encerrar o sombreador.
ms.assetid: ''
title: Função IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770563"
---
# <a name="ignorehit-function"></a><span data-ttu-id="4a29a-103">Função IgnoreHit</span><span class="sxs-lookup"><span data-stu-id="4a29a-103">IgnoreHit function</span></span>

<span data-ttu-id="4a29a-104">Chamado de um [sombreador qualquer clique](any-hit-shader.md) para rejeitar o erro e encerrar o sombreador.</span><span class="sxs-lookup"><span data-stu-id="4a29a-104">Called from an [any hit shader](any-hit-shader.md) to reject the hit and end the shader.</span></span> <span data-ttu-id="4a29a-105">A pesquisa de clique continua sem confirmar a distância e os atributos da visita atual.</span><span class="sxs-lookup"><span data-stu-id="4a29a-105">The hit search continues on without committing the distance and attributes for the current hit.</span></span>  <span data-ttu-id="4a29a-106">A chamada [**ReportHit**](reporthit-function.md) no [sombreador de interseção](intersection-shader.md), se houver um, retornará false.</span><span class="sxs-lookup"><span data-stu-id="4a29a-106">The [**ReportHit**](reporthit-function.md) call in the [intersection shader](intersection-shader.md), if there is one, will return false.</span></span>  <span data-ttu-id="4a29a-107">Todas as modificações feitas na carga Ray até esse ponto no sombreador qualquer clique são preservadas.</span><span class="sxs-lookup"><span data-stu-id="4a29a-107">Any modifications made to the ray payload up to this point in the any hit shader are preserved.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a29a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a29a-108">Syntax</span></span>

```
void IgnoreHit();

```


## <a name="return-value"></a><span data-ttu-id="4a29a-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4a29a-109">Return Value</span></span>

<span data-ttu-id="4a29a-110">**void**</span><span class="sxs-lookup"><span data-stu-id="4a29a-110">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="4a29a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a29a-111">Remarks</span></span>

<span data-ttu-id="4a29a-112">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="4a29a-112">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="4a29a-113">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="4a29a-113">**Any Hit Shader**</span></span>](any-hit-shader.md)




## <a name="see-also"></a><span data-ttu-id="4a29a-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a29a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a29a-115">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4a29a-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




