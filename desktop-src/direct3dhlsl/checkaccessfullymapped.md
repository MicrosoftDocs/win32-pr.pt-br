---
title: Função CheckAccessFullyMapped
description: Determina se todos os valores de uma operação de exemplo, de coleta ou de carregamento acessaram blocos mapeados em um recurso de lado.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- HLSL da função CheckAccessFullyMapped
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641617"
---
# <a name="checkaccessfullymapped-function"></a><span data-ttu-id="bcf0c-104">Função CheckAccessFullyMapped</span><span class="sxs-lookup"><span data-stu-id="bcf0c-104">CheckAccessFullyMapped function</span></span>

<span data-ttu-id="bcf0c-105">Determina se todos os valores de uma operação de **exemplo**, de **coleta** ou de **carregamento** acessaram blocos mapeados em um [recurso de lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="bcf0c-105">Determines whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf0c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcf0c-106">Syntax</span></span>

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a><span data-ttu-id="bcf0c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcf0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf0c-108">*status* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="bcf0c-108">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf0c-109">Tipo: **\_ apenas uint**</span><span class="sxs-lookup"><span data-stu-id="bcf0c-109">Type: **uint\_only**</span></span>

<span data-ttu-id="bcf0c-110">O valor de status que é retornado de uma operação de **exemplo**, de **coleta** ou de **carregamento** .</span><span class="sxs-lookup"><span data-stu-id="bcf0c-110">The status value that is returned from a **Sample**, **Gather**, or **Load** operation.</span></span> <span data-ttu-id="bcf0c-111">Como não é possível acessar esse valor de status diretamente, você precisa passá-lo para **CheckAccessFullyMapped**.</span><span class="sxs-lookup"><span data-stu-id="bcf0c-111">Because you can't access this status value directly, you need to pass it to **CheckAccessFullyMapped**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf0c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcf0c-112">Return value</span></span>

<span data-ttu-id="bcf0c-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="bcf0c-113">Type: **bool**</span></span>

<span data-ttu-id="bcf0c-114">Retorna um valor **booliano** que indica se todos os valores de uma operação de **exemplo**, **coleta** ou **carregamento** acessaram blocos mapeados em um [recurso de lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="bcf0c-114">Returns a **Boolean** value that indicates whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bcf0c-115">Retorna **true** se todos os valores da operação acessaram blocos mapeados; caso contrário, retornará **false** se algum valor tiver sido obtido de um bloco não mapeado.</span><span class="sxs-lookup"><span data-stu-id="bcf0c-115">Returns **TRUE** if all values from the operation accessed mapped tiles; otherwise, returns **FALSE** if any values were taken from an unmapped tile.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf0c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcf0c-116">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="bcf0c-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bcf0c-117">Minimum Shader Model</span></span>

<span data-ttu-id="bcf0c-118">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bcf0c-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bcf0c-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bcf0c-119">Shader Model</span></span>                                                                | <span data-ttu-id="bcf0c-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bcf0c-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bcf0c-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="bcf0c-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="bcf0c-122">sim</span><span class="sxs-lookup"><span data-stu-id="bcf0c-122">yes</span></span>       |



 

<span data-ttu-id="bcf0c-123">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="bcf0c-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="bcf0c-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="bcf0c-124">Vertex</span></span> | <span data-ttu-id="bcf0c-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bcf0c-125">Hull</span></span> | <span data-ttu-id="bcf0c-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="bcf0c-126">Domain</span></span> | <span data-ttu-id="bcf0c-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="bcf0c-127">Geometry</span></span> | <span data-ttu-id="bcf0c-128">16x16</span><span class="sxs-lookup"><span data-stu-id="bcf0c-128">Pixel</span></span> | <span data-ttu-id="bcf0c-129">Computação</span><span class="sxs-lookup"><span data-stu-id="bcf0c-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bcf0c-130">x</span><span class="sxs-lookup"><span data-stu-id="bcf0c-130">x</span></span>     | <span data-ttu-id="bcf0c-131">x</span><span class="sxs-lookup"><span data-stu-id="bcf0c-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bcf0c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcf0c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf0c-133">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="bcf0c-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 