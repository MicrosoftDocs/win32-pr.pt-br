---
description: Identifica uma propriedade que deve ser definida em uma transição ou efeito, juntamente com o número de valores distintos que a propriedade assume sobre a duração da transição ou do efeito.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: Estrutura de DEXTER_VALUE (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768603"
---
# <a name="dexter_value-structure"></a><span data-ttu-id="8fc38-103">\_Estrutura de valor Dexter</span><span class="sxs-lookup"><span data-stu-id="8fc38-103">DEXTER\_VALUE structure</span></span>

> [!Note]  
> <span data-ttu-id="8fc38-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8fc38-104">\[Deprecated.</span></span> <span data-ttu-id="8fc38-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8fc38-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8fc38-106">Identifica uma propriedade que deve ser definida em uma transição ou efeito, juntamente com o número de valores distintos que a propriedade assume sobre a duração da transição ou do efeito.</span><span class="sxs-lookup"><span data-stu-id="8fc38-106">Identifies a property that is to be set on a transition or effect, along with the number of distinct values that the property assumes over the duration of the transition or effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc38-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fc38-107">Syntax</span></span>


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a><span data-ttu-id="8fc38-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8fc38-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8fc38-109">**l**</span><span class="sxs-lookup"><span data-stu-id="8fc38-109">**v**</span></span>
</dt> <dd>

<span data-ttu-id="8fc38-110">Valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8fc38-110">Value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="8fc38-111">**RT**</span><span class="sxs-lookup"><span data-stu-id="8fc38-111">**rt**</span></span>
</dt> <dd>

<span data-ttu-id="8fc38-112">Hora em que a propriedade assume o valor, em relação ao início da transição ou efeito.</span><span class="sxs-lookup"><span data-stu-id="8fc38-112">Time at which the property assumes the value, relative to the start of the transition or effect.</span></span>

</dd> <dt>

<span data-ttu-id="8fc38-113">**dwInterp**</span><span class="sxs-lookup"><span data-stu-id="8fc38-113">**dwInterp**</span></span>
</dt> <dd>

<span data-ttu-id="8fc38-114">Sinalizador que indica como a propriedade progride do valor anterior para esse valor.</span><span class="sxs-lookup"><span data-stu-id="8fc38-114">Flag indicating how the property progresses from the previous value to this value.</span></span> <span data-ttu-id="8fc38-115">Deve ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="8fc38-115">Must be one of the following:</span></span>



| <span data-ttu-id="8fc38-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc38-116">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="8fc38-117">Significado</span><span class="sxs-lookup"><span data-stu-id="8fc38-117">Meaning</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <span data-ttu-id="8fc38-118"><dt>**DEXTERF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fc38-118"><dt>**DEXTERF\_JUMP**</dt></span></span> </dl>                      | <span data-ttu-id="8fc38-119">A propriedade salta instantaneamente para o novo valor na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="8fc38-119">The property jumps instantly to the new value at the specified time.</span></span><br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <span data-ttu-id="8fc38-120"><dt>**\_interpolação de DEXTERF**</dt></span><span class="sxs-lookup"><span data-stu-id="8fc38-120"><dt>**DEXTERF\_INTERPOLATE**</dt></span></span> </dl> | <span data-ttu-id="8fc38-121">A propriedade é interpolada linearmente ao longo do tempo do valor anterior.</span><span class="sxs-lookup"><span data-stu-id="8fc38-121">The property is interpolated linearly over time from the previous value.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fc38-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fc38-122">Requirements</span></span>



| <span data-ttu-id="8fc38-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc38-123">Requirement</span></span> | <span data-ttu-id="8fc38-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc38-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc38-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fc38-125">Header</span></span><br/> | <dl> <span data-ttu-id="8fc38-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc38-126"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc38-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fc38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc38-128">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="8fc38-128">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="8fc38-129">**\_parâmetro Dexter**</span><span class="sxs-lookup"><span data-stu-id="8fc38-129">**DEXTER\_PARAM**</span></span>](dexter-param.md)
</dt> </dl>

 

 




