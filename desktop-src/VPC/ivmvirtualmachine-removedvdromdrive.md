---
title: Método IVMVirtualMachine RemoveDVDROMDrive (VPCCOMInterfaces. h)
description: Remove a unidade de CD ou DVD especificada da máquina virtual.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- RemoveDVDROMDrive do método virtual PC
- Método RemoveDVDROMDrive Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método RemoveDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0962b388c318d5abebdbd7a021a4466e644a28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085695"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a><span data-ttu-id="86905-106">Método IVMVirtualMachine:: RemoveDVDROMDrive</span><span class="sxs-lookup"><span data-stu-id="86905-106">IVMVirtualMachine::RemoveDVDROMDrive method</span></span>

<span data-ttu-id="86905-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86905-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="86905-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="86905-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="86905-109">Remove a unidade de CD ou DVD especificada da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="86905-109">Removes the specified CD or DVD drive from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="86905-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86905-110">Syntax</span></span>


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="86905-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86905-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86905-112">*dvdDrive* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86905-112">*dvdDrive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86905-113">A unidade a ser removida.</span><span class="sxs-lookup"><span data-stu-id="86905-113">The drive to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86905-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86905-114">Return value</span></span>

<span data-ttu-id="86905-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="86905-115">This method can return one of these values.</span></span>



| <span data-ttu-id="86905-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="86905-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="86905-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="86905-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="86905-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="86905-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="86905-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="86905-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="86905-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="86905-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="86905-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="86905-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="86905-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="86905-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="86905-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="86905-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="86905-124"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="86905-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="86905-125">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="86905-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="86905-126"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="86905-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="86905-127">A unidade especificada não está conectada a este local de barramento.</span><span class="sxs-lookup"><span data-stu-id="86905-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="86905-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="86905-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="86905-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="86905-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="86905-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="86905-130">Remarks</span></span>

<span data-ttu-id="86905-131">Você só pode remover uma unidade de CD ou DVD existente de uma máquina virtual parada.</span><span class="sxs-lookup"><span data-stu-id="86905-131">You can only remove an existing CD or DVD drive from a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="86905-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86905-132">Requirements</span></span>



| <span data-ttu-id="86905-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="86905-133">Requirement</span></span> | <span data-ttu-id="86905-134">Valor</span><span class="sxs-lookup"><span data-stu-id="86905-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86905-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86905-135">Minimum supported client</span></span><br/> | <span data-ttu-id="86905-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="86905-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86905-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86905-137">Minimum supported server</span></span><br/> | <span data-ttu-id="86905-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="86905-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="86905-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="86905-139">End of client support</span></span><br/>    | <span data-ttu-id="86905-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86905-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="86905-141">Produto</span><span class="sxs-lookup"><span data-stu-id="86905-141">Product</span></span><br/>                  | <span data-ttu-id="86905-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="86905-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="86905-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86905-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="86905-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="86905-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="86905-145">IID</span><span class="sxs-lookup"><span data-stu-id="86905-145">IID</span></span><br/>                      | <span data-ttu-id="86905-146">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="86905-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="86905-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="86905-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86905-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="86905-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

