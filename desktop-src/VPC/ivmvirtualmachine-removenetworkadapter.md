---
title: Método IVMVirtualMachine RemoveNetworkAdapter (VPCCOMInterfaces. h)
description: Remove uma interface de rede da máquina virtual.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- RemoveNetworkAdapter do método virtual PC
- Método RemoveNetworkAdapter Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método RemoveNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455690"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a><span data-ttu-id="f2426-106">Método IVMVirtualMachine:: RemoveNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="f2426-106">IVMVirtualMachine::RemoveNetworkAdapter method</span></span>

<span data-ttu-id="f2426-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2426-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2426-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2426-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2426-109">Remove uma interface de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f2426-109">Removes a network interface from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2426-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2426-110">Syntax</span></span>


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="f2426-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2426-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2426-112">*adaptador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2426-112">*networkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2426-113">Um objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que representa o adaptador de rede a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f2426-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2426-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2426-114">Return value</span></span>

<span data-ttu-id="f2426-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="f2426-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f2426-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f2426-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="f2426-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2426-117">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="f2426-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2426-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="f2426-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f2426-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="f2426-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f2426-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="f2426-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f2426-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="f2426-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f2426-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="f2426-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="f2426-123">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="f2426-124"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="f2426-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="f2426-125">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="f2426-125">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="f2426-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="f2426-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="f2426-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f2426-127">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="f2426-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2426-128">Remarks</span></span>

<span data-ttu-id="f2426-129">Você só pode remover uma interface de rede existente de uma máquina virtual que está parada.</span><span class="sxs-lookup"><span data-stu-id="f2426-129">You can only remove an existing network interface from a virtual machine that is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2426-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2426-130">Requirements</span></span>



| <span data-ttu-id="f2426-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2426-131">Requirement</span></span> | <span data-ttu-id="f2426-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f2426-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2426-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2426-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2426-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f2426-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2426-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2426-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2426-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f2426-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2426-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f2426-137">End of client support</span></span><br/>    | <span data-ttu-id="f2426-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2426-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2426-139">Produto</span><span class="sxs-lookup"><span data-stu-id="f2426-139">Product</span></span><br/>                  | <span data-ttu-id="f2426-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2426-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2426-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2426-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2426-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2426-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2426-143">IID</span><span class="sxs-lookup"><span data-stu-id="f2426-143">IID</span></span><br/>                      | <span data-ttu-id="f2426-144">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="f2426-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f2426-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2426-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2426-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="f2426-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

