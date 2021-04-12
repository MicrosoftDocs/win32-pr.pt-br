---
title: Método IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces. h)
description: Remove a conexão de disco rígido especificada da máquina virtual.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- RemoveHardDiskConnection do método virtual PC
- Método RemoveHardDiskConnection Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método RemoveHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369658"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a><span data-ttu-id="bc646-106">Método IVMVirtualMachine:: RemoveHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="bc646-106">IVMVirtualMachine::RemoveHardDiskConnection method</span></span>

<span data-ttu-id="bc646-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bc646-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bc646-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bc646-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bc646-109">Remove a conexão de disco rígido especificada da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc646-109">Removes the specified hard disk connection from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc646-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc646-110">Syntax</span></span>


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="bc646-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc646-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc646-112">*hardDiskConnection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc646-112">*hardDiskConnection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc646-113">Um objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) que representa a conexão de disco rígido a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bc646-113">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object that represents the hard disk connection to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc646-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc646-114">Return value</span></span>

<span data-ttu-id="bc646-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bc646-115">This method can return one of these values.</span></span>



| <span data-ttu-id="bc646-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bc646-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="bc646-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc646-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc646-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bc646-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="bc646-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bc646-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="bc646-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="bc646-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="bc646-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bc646-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="bc646-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bc646-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="bc646-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="bc646-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="bc646-124"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="bc646-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="bc646-125">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="bc646-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="bc646-126"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bc646-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="bc646-127">A unidade especificada não está conectada a este local de barramento.</span><span class="sxs-lookup"><span data-stu-id="bc646-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="bc646-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="bc646-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="bc646-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="bc646-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="bc646-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc646-130">Remarks</span></span>

<span data-ttu-id="bc646-131">Você só pode remover uma conexão de disco rígido existente de uma máquina virtual parada.</span><span class="sxs-lookup"><span data-stu-id="bc646-131">You can only remove an existing hard disk connection from a stopped virtual machine.</span></span> <span data-ttu-id="bc646-132">Uma lista de conexões atualmente anexadas à máquina virtual é obtida pela enumeração da propriedade [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="bc646-132">A list of connections currently attached to the virtual machine is obtained by enumerating the [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc646-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc646-133">Requirements</span></span>



| <span data-ttu-id="bc646-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc646-134">Requirement</span></span> | <span data-ttu-id="bc646-135">Valor</span><span class="sxs-lookup"><span data-stu-id="bc646-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc646-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc646-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bc646-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bc646-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc646-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc646-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bc646-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bc646-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bc646-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bc646-140">End of client support</span></span><br/>    | <span data-ttu-id="bc646-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bc646-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bc646-142">Produto</span><span class="sxs-lookup"><span data-stu-id="bc646-142">Product</span></span><br/>                  | <span data-ttu-id="bc646-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bc646-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bc646-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc646-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc646-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc646-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bc646-146">IID</span><span class="sxs-lookup"><span data-stu-id="bc646-146">IID</span></span><br/>                      | <span data-ttu-id="bc646-147">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="bc646-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bc646-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc646-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc646-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="bc646-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

