---
title: 'Função Texture2DMS:: Load (int, int, int, uint)'
description: 'Lê os dados de textura e retorna o status da operação. | Função Texture2DMS:: Load (int, int, int, uint)'
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298063"
---
# <a name="texture2dmsloadintintintuint-function"></a><span data-ttu-id="4d8f9-105">Função Texture2DMS:: Load (int, int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="4d8f9-105">Texture2DMS::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="4d8f9-106">Lê os dados de textura e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="4d8f9-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8f9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d8f9-107">Syntax</span></span>


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="4d8f9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d8f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8f9-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4d8f9-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8f9-110">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="4d8f9-110">Type: **int2**</span></span>

<span data-ttu-id="4d8f9-111">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="4d8f9-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="4d8f9-112">*sampleindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d8f9-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8f9-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d8f9-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4d8f9-114">O índice de exemplo.</span><span class="sxs-lookup"><span data-stu-id="4d8f9-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="4d8f9-115">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d8f9-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8f9-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="4d8f9-116">Type: **int2**</span></span>

<span data-ttu-id="4d8f9-117">Um deslocamento aplicado às coordenadas de textura antes do carregamento.</span><span class="sxs-lookup"><span data-stu-id="4d8f9-117">An offset applied to the texture coordinates before loading.</span></span>

</dd> <dt>

<span data-ttu-id="4d8f9-118">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4d8f9-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8f9-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4d8f9-119">Type: **uint**</span></span>

<span data-ttu-id="4d8f9-120">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="4d8f9-120">The status of the operation.</span></span> <span data-ttu-id="4d8f9-121">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4d8f9-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4d8f9-122">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4d8f9-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4d8f9-123">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="4d8f9-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8f9-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d8f9-124">Return value</span></span>

<span data-ttu-id="4d8f9-125">Tipo:</span><span class="sxs-lookup"><span data-stu-id="4d8f9-125">Type:</span></span>

<span data-ttu-id="4d8f9-126">O tipo de retorno corresponde ao tipo na declaração para o objeto [**Texture2DMS**](sm5-object-texture2dms.md) .</span><span class="sxs-lookup"><span data-stu-id="4d8f9-126">The return type matches the type in the declaration for the [**Texture2DMS**](sm5-object-texture2dms.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d8f9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d8f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8f9-128">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="4d8f9-128">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="4d8f9-129">**Texture2DMS**</span><span class="sxs-lookup"><span data-stu-id="4d8f9-129">**Texture2DMS**</span></span>](sm5-object-texture2dms.md)
</dt> </dl>

 

 
