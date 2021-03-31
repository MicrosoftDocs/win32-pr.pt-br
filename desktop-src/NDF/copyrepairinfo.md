---
title: Função CopyRepairInfo (Ndattributils. h)
description: Cria uma cópia de uma estrutura RepairInfo.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- NDF da função CopyRepairInfo
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918230"
---
# <a name="copyrepairinfo-function"></a><span data-ttu-id="69b1a-104">Função CopyRepairInfo</span><span class="sxs-lookup"><span data-stu-id="69b1a-104">CopyRepairInfo function</span></span>

<span data-ttu-id="69b1a-105">A função **CopyRepairInfo** cria uma cópia de uma estrutura [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="69b1a-105">The **CopyRepairInfo** function creates a copy of a [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b1a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69b1a-106">Syntax</span></span>


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="69b1a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69b1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b1a-108">*Dest* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="69b1a-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69b1a-109">Tipo: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="69b1a-109">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="69b1a-110">A estrutura a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="69b1a-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="69b1a-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69b1a-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b1a-112">Tipo: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="69b1a-112">Type: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="69b1a-113">A estrutura existente a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="69b1a-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b1a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69b1a-114">Return value</span></span>

<span data-ttu-id="69b1a-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="69b1a-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="69b1a-116">Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="69b1a-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="69b1a-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="69b1a-117">Return code</span></span>                                                                                   | <span data-ttu-id="69b1a-118">Description</span><span class="sxs-lookup"><span data-stu-id="69b1a-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69b1a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69b1a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="69b1a-120">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="69b1a-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="69b1a-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="69b1a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="69b1a-122">Um ou mais parâmetros não foram fornecidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="69b1a-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="69b1a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="69b1a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="69b1a-124">Não há memória suficiente disponível para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="69b1a-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="69b1a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b1a-125">Requirements</span></span>



| <span data-ttu-id="69b1a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b1a-126">Requirement</span></span> | <span data-ttu-id="69b1a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="69b1a-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b1a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b1a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="69b1a-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="69b1a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69b1a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b1a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="69b1a-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="69b1a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="69b1a-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69b1a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b1a-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b1a-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b1a-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="69b1a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b1a-135">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="69b1a-135">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





