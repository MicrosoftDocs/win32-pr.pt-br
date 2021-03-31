---
title: Estrutura de BITS_JOB_PROPERTY_VALUE (Deliveryoptimization. h)
description: A BITS_JOB_PROPERTY_VALUE Union fornece o valor da propriedade da função do trabalho com base no valor da enumeração BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Estrutura de BITS_JOB_PROPERTY_VALUE
- Estrutura de BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085550"
---
# <a name="bits_job_property_value-structure"></a><span data-ttu-id="73889-105">Estrutura de BITS_JOB_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="73889-105">BITS_JOB_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="73889-106">A **BITS_JOB_PROPERTY_VALUE** Union fornece o valor da propriedade da função do trabalho com base no valor da enumeração [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="73889-106">The **BITS_JOB_PROPERTY_VALUE** union provides the property value of the DO job based on the value of the [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="73889-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73889-107">Syntax</span></span>


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="73889-108">Membros</span><span class="sxs-lookup"><span data-stu-id="73889-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="73889-109">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="73889-109">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="73889-110">Esse valor é retornado ao usar a ID de propriedade de enumeração **BITS_JOB_PROPERTY_ID_COST_FLAGS** e é aplicado como a [política de transferência](https://www.bing.com/search?q=transfer+policy) no trabalho.</span><span class="sxs-lookup"><span data-stu-id="73889-110">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_ID_COST_FLAGS** and is applied as the [transfer policy](https://www.bing.com/search?q=transfer+policy) on the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="73889-111">**ClsID**</span><span class="sxs-lookup"><span data-stu-id="73889-111">**ClsID**</span></span>
</dt> <dd>

<span data-ttu-id="73889-112">Esse valor é retornado ao usar a ID de propriedade de enumeração **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** e representa o CLSID do objeto de retorno de chamada a ser registrado no trabalho do.</span><span class="sxs-lookup"><span data-stu-id="73889-112">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** and represents the CLSID of the callback object to register with the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="73889-113">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="73889-113">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="73889-114">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="73889-114">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="73889-115">**UInt64**</span><span class="sxs-lookup"><span data-stu-id="73889-115">**Uint64**</span></span>
</dt> <dd>

<span data-ttu-id="73889-116">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="73889-116">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="73889-117">**Target (destino)**</span><span class="sxs-lookup"><span data-stu-id="73889-117">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="73889-118">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="73889-118">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73889-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73889-119">Requirements</span></span>



| <span data-ttu-id="73889-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="73889-120">Requirement</span></span> | <span data-ttu-id="73889-121">Valor</span><span class="sxs-lookup"><span data-stu-id="73889-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73889-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73889-122">Minimum supported client</span></span><br/> | <span data-ttu-id="73889-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="73889-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="73889-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73889-124">Minimum supported server</span></span><br/> | <span data-ttu-id="73889-125">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="73889-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="73889-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73889-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="73889-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="73889-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73889-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="73889-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73889-129">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="73889-129">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="73889-130">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="73889-130">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





