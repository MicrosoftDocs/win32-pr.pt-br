---
title: Método IVMVirtualMachine DiscardUndoDisks (VPCCOMInterfaces. h)
description: Descarta os discos de desfazer virtuais.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- DiscardUndoDisks do método virtual PC
- Método DiscardUndoDisks Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método DiscardUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455255"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a><span data-ttu-id="94982-106">IVMVirtualMachine: método iscardUndoDisks de:D</span><span class="sxs-lookup"><span data-stu-id="94982-106">IVMVirtualMachine::DiscardUndoDisks method</span></span>

<span data-ttu-id="94982-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="94982-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="94982-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="94982-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="94982-109">Descarta os discos de desfazer virtuais.</span><span class="sxs-lookup"><span data-stu-id="94982-109">Discards the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="94982-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94982-110">Syntax</span></span>


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a><span data-ttu-id="94982-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94982-111">Parameters</span></span>

<span data-ttu-id="94982-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="94982-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94982-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94982-113">Return value</span></span>

<span data-ttu-id="94982-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="94982-114">This method can return one of these values.</span></span>



| <span data-ttu-id="94982-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="94982-115">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="94982-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="94982-116">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94982-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="94982-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="94982-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="94982-118">The operation was successful.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="94982-119"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="94982-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="94982-120">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="94982-120">The configuration is unknown.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="94982-121"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="94982-121"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="94982-122">Os discos de desfazer virtuais não podem ser descartados enquanto a máquina virtual está em execução ou em um estado salvo.</span><span class="sxs-lookup"><span data-stu-id="94982-122">The virtual undo disks cannot be discarded while the virtual machine is running or in a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="94982-123"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="94982-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="94982-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="94982-124">An unexpected error has occurred.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="94982-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94982-125">Requirements</span></span>



| <span data-ttu-id="94982-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="94982-126">Requirement</span></span> | <span data-ttu-id="94982-127">Valor</span><span class="sxs-lookup"><span data-stu-id="94982-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="94982-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94982-128">Minimum supported client</span></span><br/> | <span data-ttu-id="94982-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="94982-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94982-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94982-130">Minimum supported server</span></span><br/> | <span data-ttu-id="94982-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="94982-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="94982-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="94982-132">End of client support</span></span><br/>    | <span data-ttu-id="94982-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="94982-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="94982-134">Produto</span><span class="sxs-lookup"><span data-stu-id="94982-134">Product</span></span><br/>                  | <span data-ttu-id="94982-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="94982-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="94982-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94982-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="94982-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="94982-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="94982-138">IID</span><span class="sxs-lookup"><span data-stu-id="94982-138">IID</span></span><br/>                      | <span data-ttu-id="94982-139">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="94982-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="94982-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="94982-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94982-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="94982-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

