---
title: Método IVMTask Cancel (VPCCOMInterfaces. h)
description: Cancela a tarefa.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Cancelar método virtual PC
- Método Cancel Virtual PC, interface IVMTask
- IVMTask interface virtual PC, cancelar método
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295895"
---
# <a name="ivmtaskcancel-method"></a><span data-ttu-id="a9da8-106">Método IVMTask:: Cancel</span><span class="sxs-lookup"><span data-stu-id="a9da8-106">IVMTask::Cancel method</span></span>

<span data-ttu-id="a9da8-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9da8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9da8-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9da8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9da8-109">Cancela a tarefa.</span><span class="sxs-lookup"><span data-stu-id="a9da8-109">Cancels the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9da8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9da8-110">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="a9da8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9da8-111">Parameters</span></span>

<span data-ttu-id="a9da8-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a9da8-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9da8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9da8-113">Return value</span></span>

<span data-ttu-id="a9da8-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a9da8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a9da8-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a9da8-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="a9da8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9da8-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a9da8-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9da8-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a9da8-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a9da8-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a9da8-119"><dt>**E \_ FALHA**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="a9da8-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="a9da8-120">A tarefa não pode ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="a9da8-120">The task cannot be canceled.</span></span><br/>      |
| <dl> <span data-ttu-id="a9da8-121"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a9da8-121"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a9da8-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a9da8-122">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a9da8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9da8-123">Requirements</span></span>



| <span data-ttu-id="a9da8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9da8-124">Requirement</span></span> | <span data-ttu-id="a9da8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a9da8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9da8-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9da8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a9da8-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9da8-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9da8-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9da8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a9da8-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a9da8-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9da8-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a9da8-130">End of client support</span></span><br/>    | <span data-ttu-id="a9da8-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9da8-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9da8-132">Produto</span><span class="sxs-lookup"><span data-stu-id="a9da8-132">Product</span></span><br/>                  | <span data-ttu-id="a9da8-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9da8-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9da8-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9da8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9da8-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9da8-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a9da8-136">IID</span><span class="sxs-lookup"><span data-stu-id="a9da8-136">IID</span></span><br/>                      | <span data-ttu-id="a9da8-137">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="a9da8-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="a9da8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9da8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9da8-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="a9da8-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

