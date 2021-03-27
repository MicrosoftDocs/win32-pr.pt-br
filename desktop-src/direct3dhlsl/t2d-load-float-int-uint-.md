---
title: 'Função Texture2D:: Load (int, int, uint)'
description: 'Lê os dados de textura e retorna o status da operação. | Função Texture2D:: Load (int, int, uint)'
ms.assetid: 05A12BE2-4604-470B-9EE8-F03F51E6D254
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c591b92b64641e169023f30663d8f5c6ef8a6c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298301"
---
# <a name="texture2dloadintintuint-function"></a><span data-ttu-id="afd96-105">Função Texture2D:: Load (int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="afd96-105">Texture2D::Load(int,int,uint) function</span></span>

<span data-ttu-id="afd96-106">Lê os dados de textura e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="afd96-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd96-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afd96-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="afd96-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afd96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd96-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="afd96-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd96-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="afd96-110">Type: **int**</span></span>

<span data-ttu-id="afd96-111">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="afd96-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="afd96-112">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="afd96-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd96-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="afd96-113">Type: **int**</span></span>

<span data-ttu-id="afd96-114">Um deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="afd96-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="afd96-115">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="afd96-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afd96-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="afd96-116">Type: **uint**</span></span>

<span data-ttu-id="afd96-117">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="afd96-117">The status of the operation.</span></span> <span data-ttu-id="afd96-118">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="afd96-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="afd96-119">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="afd96-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="afd96-120">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="afd96-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd96-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="afd96-121">Return value</span></span>

<span data-ttu-id="afd96-122">Tipo:</span><span class="sxs-lookup"><span data-stu-id="afd96-122">Type:</span></span>

<span data-ttu-id="afd96-123">O tipo de retorno corresponde ao tipo na declaração para o objeto [**Texture2D**](sm5-object-texture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="afd96-123">The return type matches the type in the declaration for the [**Texture2D**](sm5-object-texture2d.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="afd96-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="afd96-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd96-125">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="afd96-125">Load methods</span></span>](texture2d-load.md)
</dt> </dl>

 

 
