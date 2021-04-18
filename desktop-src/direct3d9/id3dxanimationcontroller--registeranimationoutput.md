---
description: Adiciona uma saída de animação ao controlador de animação e registra ponteiros para transformações de Scale (dimensionar, girar e traduzir).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'Método ID3DXAnimationController:: RegisterAnimationOutput (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793230"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a><span data-ttu-id="0286f-103">Método ID3DXAnimationController:: RegisterAnimationOutput</span><span class="sxs-lookup"><span data-stu-id="0286f-103">ID3DXAnimationController::RegisterAnimationOutput method</span></span>

<span data-ttu-id="0286f-104">Adiciona uma saída de animação ao controlador de animação e registra ponteiros para transformações de Scale (dimensionar, girar e traduzir).</span><span class="sxs-lookup"><span data-stu-id="0286f-104">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="0286f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0286f-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="0286f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0286f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0286f-107">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0286f-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0286f-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0286f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0286f-109">Nome da saída da animação.</span><span class="sxs-lookup"><span data-stu-id="0286f-109">Name of the animation output.</span></span>

</dd> <dt>

<span data-ttu-id="0286f-110">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0286f-110">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0286f-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0286f-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0286f-112">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que contém dados de transformação de Srt.</span><span class="sxs-lookup"><span data-stu-id="0286f-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure containing SRT transformation data.</span></span> <span data-ttu-id="0286f-113">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0286f-113">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0286f-114">*pScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0286f-114">*pScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0286f-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0286f-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0286f-116">Ponteiro para um vetor [**D3DXVECTOR3**](d3dxvector3.md) que descreve a escala do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="0286f-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span> <span data-ttu-id="0286f-117">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0286f-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0286f-118">*protação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0286f-118">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0286f-119">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0286f-119">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0286f-120">Ponteiro para um Quaternion [**D3DXQUATERNION**](d3dxquaternion.md) que descreve a rotação do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="0286f-120">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span> <span data-ttu-id="0286f-121">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0286f-121">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0286f-122">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0286f-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0286f-123">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0286f-123">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0286f-124">Ponteiro para um vetor [**D3DXVECTOR3**](d3dxvector3.md) que descreve a tradução do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="0286f-124">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span> <span data-ttu-id="0286f-125">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0286f-125">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0286f-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0286f-126">Return value</span></span>

<span data-ttu-id="0286f-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0286f-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0286f-128">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0286f-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0286f-129">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0286f-129">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0286f-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="0286f-130">Remarks</span></span>

<span data-ttu-id="0286f-131">Se a saída da animação já estiver registrada, pMatrix será preenchido com os dados de transformação de entrada.</span><span class="sxs-lookup"><span data-stu-id="0286f-131">If the animation output is already registered, pMatrix will be filled with the input transformation data.</span></span>

<span data-ttu-id="0286f-132">Os conjuntos de animação criados com [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registram automaticamente todos os conjuntos de animação carregados.</span><span class="sxs-lookup"><span data-stu-id="0286f-132">Animation sets created with [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) automatically register all loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="0286f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0286f-133">Requirements</span></span>



| <span data-ttu-id="0286f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0286f-134">Requirement</span></span> | <span data-ttu-id="0286f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0286f-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0286f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0286f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="0286f-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0286f-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0286f-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0286f-138">Library</span></span><br/> | <dl> <span data-ttu-id="0286f-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0286f-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0286f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0286f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0286f-141">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0286f-141">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
