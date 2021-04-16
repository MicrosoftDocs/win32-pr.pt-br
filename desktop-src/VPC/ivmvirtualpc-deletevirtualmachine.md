---
title: Método IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Exclui uma configuração de máquina virtual.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- DeleteVirtualMachine do método virtual PC
- Método DeleteVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794594"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a><span data-ttu-id="43c16-106">IVMVirtualPC: método eleteVirtualMachine de:D</span><span class="sxs-lookup"><span data-stu-id="43c16-106">IVMVirtualPC::DeleteVirtualMachine method</span></span>

<span data-ttu-id="43c16-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="43c16-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43c16-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="43c16-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43c16-109">Exclui uma configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43c16-109">Deletes a virtual machine configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c16-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43c16-110">Syntax</span></span>


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="43c16-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43c16-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c16-112">*VirtualMachine* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43c16-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c16-113">Um ponteiro para um objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa a configuração da máquina virtual a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="43c16-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object representing the virtual machine configuration to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c16-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43c16-114">Return value</span></span>

<span data-ttu-id="43c16-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="43c16-115">This method can return one of these values.</span></span>



| <span data-ttu-id="43c16-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="43c16-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="43c16-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="43c16-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43c16-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43c16-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="43c16-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="43c16-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="43c16-120"><dt>**S \_ FALSO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="43c16-120"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="43c16-121">Não foi possível encontrar a configuração especificada.</span><span class="sxs-lookup"><span data-stu-id="43c16-121">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="43c16-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="43c16-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="43c16-123">O parâmetro *VirtualMachine* era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="43c16-123">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="43c16-124"><dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="43c16-124"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="43c16-125">A máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="43c16-125">The virtual machine is running.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="43c16-126"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="43c16-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="43c16-127">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="43c16-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="43c16-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="43c16-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="43c16-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="43c16-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="43c16-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="43c16-130">Remarks</span></span>

<span data-ttu-id="43c16-131">Somente as máquinas virtuais interrompidas podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="43c16-131">Only stopped virtual machines can be deleted.</span></span> <span data-ttu-id="43c16-132">Observe que qualquer estado salvo existente ou dados da unidade de desfazer para essa configuração serão excluídos além do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="43c16-132">Note that any existing saved state or undo drive data for this configuration will be deleted in addition to the configuration file.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c16-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43c16-133">Requirements</span></span>



| <span data-ttu-id="43c16-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c16-134">Requirement</span></span> | <span data-ttu-id="43c16-135">Valor</span><span class="sxs-lookup"><span data-stu-id="43c16-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c16-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43c16-136">Minimum supported client</span></span><br/> | <span data-ttu-id="43c16-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="43c16-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43c16-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43c16-138">Minimum supported server</span></span><br/> | <span data-ttu-id="43c16-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="43c16-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="43c16-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="43c16-140">End of client support</span></span><br/>    | <span data-ttu-id="43c16-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43c16-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="43c16-142">Produto</span><span class="sxs-lookup"><span data-stu-id="43c16-142">Product</span></span><br/>                  | <span data-ttu-id="43c16-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43c16-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="43c16-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43c16-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c16-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c16-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="43c16-146">IID</span><span class="sxs-lookup"><span data-stu-id="43c16-146">IID</span></span><br/>                      | <span data-ttu-id="43c16-147">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="43c16-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="43c16-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="43c16-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c16-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="43c16-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

