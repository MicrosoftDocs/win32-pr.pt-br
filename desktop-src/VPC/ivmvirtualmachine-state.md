---
title: Propriedade de estado IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o estado atual da máquina virtual.
ms.assetid: a4214dfc-09d2-4d6b-a053-e75e99063411
keywords:
- Propriedade de estado Virtual PC
- Propriedade de estado Virtual PC, interface IVMVirtualMachine
- Virtual PC interface IVMVirtualMachine, propriedade State
topic_type:
- apiref
api_name:
- IVMVirtualMachine.State
- IVMVirtualMachine.get_State
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11616f2a88b9238da11a4edec00c048e69885a07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918935"
---
# <a name="ivmvirtualmachinestate-property"></a><span data-ttu-id="5f198-106">Propriedade IVMVirtualMachine:: State</span><span class="sxs-lookup"><span data-stu-id="5f198-106">IVMVirtualMachine::State property</span></span>

<span data-ttu-id="5f198-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f198-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5f198-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5f198-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5f198-109">Recupera o estado atual da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5f198-109">Retrieves the current state of the virtual machine.</span></span>

<span data-ttu-id="5f198-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5f198-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f198-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f198-111">Syntax</span></span>


```C++
HRESULT get_State(
  [out, retval] VMVMState *virtualMachineState
);
```



## <a name="property-value"></a><span data-ttu-id="5f198-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5f198-112">Property value</span></span>

<span data-ttu-id="5f198-113">O estado atual da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5f198-113">The current state of the virtual machine.</span></span> <span data-ttu-id="5f198-114">Para obter uma lista de valores, consulte [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="5f198-114">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f198-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5f198-115">Error codes</span></span>



| <span data-ttu-id="5f198-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="5f198-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="5f198-117">Significado</span><span class="sxs-lookup"><span data-stu-id="5f198-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5f198-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5f198-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5f198-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5f198-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="5f198-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="5f198-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5f198-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5f198-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="5f198-122"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5f198-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="5f198-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="5f198-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="5f198-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="5f198-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5f198-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="5f198-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5f198-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f198-126">Requirements</span></span>



| <span data-ttu-id="5f198-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f198-127">Requirement</span></span> | <span data-ttu-id="5f198-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5f198-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f198-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f198-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5f198-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5f198-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f198-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f198-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5f198-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5f198-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5f198-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5f198-133">End of client support</span></span><br/>    | <span data-ttu-id="5f198-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f198-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5f198-135">Produto</span><span class="sxs-lookup"><span data-stu-id="5f198-135">Product</span></span><br/>                  | <span data-ttu-id="5f198-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5f198-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5f198-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f198-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f198-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f198-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5f198-139">IID</span><span class="sxs-lookup"><span data-stu-id="5f198-139">IID</span></span><br/>                      | <span data-ttu-id="5f198-140">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="5f198-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5f198-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f198-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f198-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="5f198-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

