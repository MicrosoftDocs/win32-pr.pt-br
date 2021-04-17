---
description: Especifica o valor que uma propriedade assume em um determinado momento.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: Estrutura de DEXTER_PARAM (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748614"
---
# <a name="dexter_param-structure"></a><span data-ttu-id="4372b-103">\_Estrutura de parâmetro Dexter</span><span class="sxs-lookup"><span data-stu-id="4372b-103">DEXTER\_PARAM structure</span></span>

> [!Note]  
> <span data-ttu-id="4372b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4372b-104">\[Deprecated.</span></span> <span data-ttu-id="4372b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4372b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4372b-106">Especifica o valor que uma propriedade assume em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="4372b-106">Specifies the value that a property assumes at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4372b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4372b-107">Syntax</span></span>


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a><span data-ttu-id="4372b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4372b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4372b-109">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4372b-109">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="4372b-110">Nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4372b-110">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="4372b-111">**dispID**</span><span class="sxs-lookup"><span data-stu-id="4372b-111">**dispID**</span></span>
</dt> <dd>

<span data-ttu-id="4372b-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4372b-112">Reserved.</span></span> <span data-ttu-id="4372b-113">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="4372b-113">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4372b-114">**nValores**</span><span class="sxs-lookup"><span data-stu-id="4372b-114">**nValues**</span></span>
</dt> <dd>

<span data-ttu-id="4372b-115">Número de valores que a propriedade assume.</span><span class="sxs-lookup"><span data-stu-id="4372b-115">Number of values that the property assumes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4372b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4372b-116">Remarks</span></span>

<span data-ttu-id="4372b-117">O objeto deve dar suporte à interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="4372b-117">The object must support the **IDispatch** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4372b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4372b-118">Requirements</span></span>



| <span data-ttu-id="4372b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4372b-119">Requirement</span></span> | <span data-ttu-id="4372b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4372b-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4372b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4372b-121">Header</span></span><br/> | <dl> <span data-ttu-id="4372b-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4372b-122"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4372b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4372b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4372b-124">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="4372b-124">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="4372b-125">**valor de DEXTER \_**</span><span class="sxs-lookup"><span data-stu-id="4372b-125">**DEXTER\_VALUE**</span></span>](dexter-value.md)
</dt> </dl>

 

 




