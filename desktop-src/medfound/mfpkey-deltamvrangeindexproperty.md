---
description: Especifica o método usado para codificar as informações de vetor de movimento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: Propriedade MFPKEY_DELTAMVRANGEINDEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505735"
---
# <a name="mfpkey_deltamvrangeindex-property"></a><span data-ttu-id="31539-103">\_Propriedade MFPKEY DELTAMVRANGEINDEX</span><span class="sxs-lookup"><span data-stu-id="31539-103">MFPKEY\_DELTAMVRANGEINDEX Property</span></span>

<span data-ttu-id="31539-104">Especifica o método usado para codificar as informações de vetor de movimento.</span><span class="sxs-lookup"><span data-stu-id="31539-104">Specifies the method used to encode the motion vector information.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="31539-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="31539-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="31539-106">g \_ wszWMVCDeltaMVRangeIndex</span><span class="sxs-lookup"><span data-stu-id="31539-106">g\_wszWMVCDeltaMVRangeIndex</span></span>

## <a name="data-type"></a><span data-ttu-id="31539-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="31539-107">Data Type</span></span>

<span data-ttu-id="31539-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="31539-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="31539-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="31539-109">Default Value</span></span>

<span data-ttu-id="31539-110">0</span><span class="sxs-lookup"><span data-stu-id="31539-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="31539-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="31539-111">Remarks</span></span>

<span data-ttu-id="31539-112">Se essa propriedade for definida, o codificador aumentará o intervalo de vetor de movimento Delta nos campos.</span><span class="sxs-lookup"><span data-stu-id="31539-112">If this property is set, the encoder increases the delta motion vector range in fields.</span></span> <span data-ttu-id="31539-113">As informações de vetor de movimento são válidas somente para campos entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="31539-113">Motion vector information is valid only for interlaced fields.</span></span>

<span data-ttu-id="31539-114">Essa propriedade pode ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="31539-114">This property may be set to one of the following values:</span></span>



| <span data-ttu-id="31539-115">Valor</span><span class="sxs-lookup"><span data-stu-id="31539-115">Value</span></span> | <span data-ttu-id="31539-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="31539-116">Description</span></span>                                                                          |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31539-117">0</span><span class="sxs-lookup"><span data-stu-id="31539-117">0</span></span>     | <span data-ttu-id="31539-118">Use o intervalo de vetor de movimento Delta existente.</span><span class="sxs-lookup"><span data-stu-id="31539-118">Use the existing delta motion vector range.</span></span>                                          |
| <span data-ttu-id="31539-119">1</span><span class="sxs-lookup"><span data-stu-id="31539-119">1</span></span>     | <span data-ttu-id="31539-120">Dobrar o intervalo de vetor de movimento Delta na direção horizontal.</span><span class="sxs-lookup"><span data-stu-id="31539-120">Double the delta motion vector range in the horizontal direction.</span></span>                    |
| <span data-ttu-id="31539-121">2</span><span class="sxs-lookup"><span data-stu-id="31539-121">2</span></span>     | <span data-ttu-id="31539-122">Dobrar o intervalo de vetor de movimento Delta na direção vertical.</span><span class="sxs-lookup"><span data-stu-id="31539-122">Double the delta motion vector range in the vertical direction.</span></span>                      |
| <span data-ttu-id="31539-123">3</span><span class="sxs-lookup"><span data-stu-id="31539-123">3</span></span>     | <span data-ttu-id="31539-124">Dobrar o intervalo de vetor de movimento Delta nas direções horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="31539-124">Double the delta motion vector range in both the horizontal and vertical directions.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="31539-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31539-125">Requirements</span></span>



| <span data-ttu-id="31539-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="31539-126">Requirement</span></span> | <span data-ttu-id="31539-127">Valor</span><span class="sxs-lookup"><span data-stu-id="31539-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31539-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31539-128">Minimum supported client</span></span><br/> | <span data-ttu-id="31539-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31539-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31539-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31539-130">Minimum supported server</span></span><br/> | <span data-ttu-id="31539-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31539-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31539-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31539-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="31539-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31539-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31539-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="31539-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31539-135">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31539-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




