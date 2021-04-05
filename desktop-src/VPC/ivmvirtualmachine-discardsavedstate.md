---
title: Método IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces. h)
description: Descarta todas as informações de estado salvas de uma máquina virtual salva.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- DiscardSavedState do método virtual PC
- Método DiscardSavedState Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método DiscardSavedState
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009497"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a><span data-ttu-id="d8fc6-106">IVMVirtualMachine: método iscardSavedState de:D</span><span class="sxs-lookup"><span data-stu-id="d8fc6-106">IVMVirtualMachine::DiscardSavedState method</span></span>

<span data-ttu-id="d8fc6-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d8fc6-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d8fc6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d8fc6-109">Descarta todas as informações de estado salvas de uma máquina virtual salva.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-109">Discards any saved state information for a saved virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8fc6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8fc6-110">Syntax</span></span>


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a><span data-ttu-id="d8fc6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8fc6-111">Parameters</span></span>

<span data-ttu-id="d8fc6-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8fc6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8fc6-113">Return value</span></span>

<span data-ttu-id="d8fc6-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d8fc6-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d8fc6-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="d8fc6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8fc6-116">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8fc6-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8fc6-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="d8fc6-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-118">The operation was successful.</span></span><br/>                               |
| <dl> <span data-ttu-id="d8fc6-119"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d8fc6-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="d8fc6-120">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-120">The configuration is unknown.</span></span><br/>                               |
| <dl> <span data-ttu-id="d8fc6-121"><dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="d8fc6-121"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>           | <span data-ttu-id="d8fc6-122">A máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-122">The virtual machine is running.</span></span><br/>                             |
| <dl> <span data-ttu-id="d8fc6-123"><dt>**VM \_ E \_ VM \_ não \_ 0xA00400501 \_ estado salvo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d8fc6-123"><dt>**VM\_E\_VM\_NO\_SAVED\_STATE**</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="d8fc6-124">A máquina virtual não está em execução, mas não tem estado salvo.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-124">The virtual machine is not running, but has no saved state.</span></span><br/> |
| <dl> <span data-ttu-id="d8fc6-125"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="d8fc6-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="d8fc6-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-126">An unexpected error has occurred.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="d8fc6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8fc6-127">Requirements</span></span>



| <span data-ttu-id="d8fc6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8fc6-128">Requirement</span></span> | <span data-ttu-id="d8fc6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d8fc6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fc6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8fc6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8fc6-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d8fc6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8fc6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8fc6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8fc6-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d8fc6-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d8fc6-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d8fc6-134">End of client support</span></span><br/>    | <span data-ttu-id="d8fc6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8fc6-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d8fc6-136">Produto</span><span class="sxs-lookup"><span data-stu-id="d8fc6-136">Product</span></span><br/>                  | <span data-ttu-id="d8fc6-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d8fc6-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d8fc6-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8fc6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8fc6-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8fc6-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d8fc6-140">IID</span><span class="sxs-lookup"><span data-stu-id="d8fc6-140">IID</span></span><br/>                      | <span data-ttu-id="d8fc6-141">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d8fc6-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d8fc6-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8fc6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8fc6-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d8fc6-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

