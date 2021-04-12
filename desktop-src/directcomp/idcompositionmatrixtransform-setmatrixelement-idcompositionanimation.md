---
title: Método IDCompositionMatrixTransform setmatrixelement (int, int, IDCompositionAnimation)
description: Anima o valor de um elemento da matriz dessa transformação 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Método setmatrixelement DirectComposition
- Método setmatrixelement DirectComposition, interface IDCompositionMatrixTransform
- IDCompositionMatrixTransform interface DirectComposition, método setmatrixelement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366447"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a><span data-ttu-id="9ed5e-106">Método IDCompositionMatrixTransform:: setmatrixelement (int, int, IDCompositionAnimation \* )</span><span class="sxs-lookup"><span data-stu-id="9ed5e-106">IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation\*) method</span></span>

<span data-ttu-id="9ed5e-107">Anima o valor de um elemento da matriz dessa transformação 2D.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-107">Animates the value of one element of the matrix of this 2D transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed5e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ed5e-108">Syntax</span></span>


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a><span data-ttu-id="9ed5e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ed5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed5e-110">*linha* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="9ed5e-110">*row* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed5e-111">O índice de linha do elemento a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-111">The row index of the element to change.</span></span> <span data-ttu-id="9ed5e-112">Esse valor deve estar entre 0 e 2, inclusive.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-112">This value must be between 0 and 2, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="9ed5e-113">*coluna* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ed5e-113">*column* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed5e-114">O índice de coluna do elemento a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-114">The column index of the element to change.</span></span> <span data-ttu-id="9ed5e-115">Esse valor deve estar entre 0 e 1, inclusive.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-115">This value must be between 0 and 1, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="9ed5e-116">*animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ed5e-116">*animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed5e-117">Uma animação que representa como o valor do elemento especificado muda ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-117">An animation that represents how the value of the specified element changes over time.</span></span> <span data-ttu-id="9ed5e-118">Esse parâmetro não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-118">This parameter must not be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed5e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ed5e-119">Return value</span></span>

<span data-ttu-id="9ed5e-120">Se a função for bem sucedido, ela retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-120">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="9ed5e-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ed5e-121">Otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="9ed5e-122">Consulte [códigos de erro DirectComposition](directcomposition-error-codes.md) para obter uma lista de códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-122">See [DirectComposition Error Codes](directcomposition-error-codes.md) for a list of error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed5e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ed5e-123">Remarks</span></span>

<span data-ttu-id="9ed5e-124">Esse método faz uma cópia da animação especificada.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-124">This method makes a copy of the specified animation.</span></span> <span data-ttu-id="9ed5e-125">Se o objeto referenciado pelo parâmetro de *animação* for alterado depois de chamar esse método, a alteração não afetará o elemento, a menos que esse método seja chamado novamente.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-125">If the object referenced by the *animation* parameter is changed after calling this method, the change does not affect the element unless this method is called again.</span></span> <span data-ttu-id="9ed5e-126">Se o elemento foi animado anteriormente, chamar esse método substituirá a animação anterior pela nova animação.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-126">If the element was previously animated, calling this method replaces the previous animation with the new animation.</span></span>

<span data-ttu-id="9ed5e-127">Esse método falhará se a *animação* for um ponteiro inválido ou se não tiver sido criada pela mesma interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) que a transformação afetada.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-127">This method fails if *animation* is an invalid pointer or if it was not created by the same [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) interface as the affected transform.</span></span> <span data-ttu-id="9ed5e-128">A interface não pode ser uma implementação personalizada; somente interfaces criadas pelo Microsoft DirectComposition podem ser usadas com esse método.</span><span class="sxs-lookup"><span data-stu-id="9ed5e-128">The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ed5e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ed5e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed5e-130">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="9ed5e-130">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 