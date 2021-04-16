---
title: Método IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces. h)
description: Libera um dispositivo USB de uma máquina virtual.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- DetachUSBDevice do método virtual PC
- Método DetachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794596"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a><span data-ttu-id="e38d2-106">IVMVirtualMachine: método etachUSBDevice de:D</span><span class="sxs-lookup"><span data-stu-id="e38d2-106">IVMVirtualMachine::DetachUSBDevice method</span></span>

<span data-ttu-id="e38d2-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e38d2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e38d2-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e38d2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e38d2-109">Libera um dispositivo USB de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e38d2-109">Releases a USB device from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e38d2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e38d2-110">Syntax</span></span>


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="e38d2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e38d2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e38d2-112">*inUSBDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e38d2-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e38d2-113">Um ponteiro [**IVMUSBDevice**](ivmusbdevice.md) que representa o dispositivo USB a ser desanexado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e38d2-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device to be detached from the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e38d2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e38d2-114">Return value</span></span>

<span data-ttu-id="e38d2-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e38d2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e38d2-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e38d2-116">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="e38d2-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e38d2-117">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e38d2-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e38d2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="e38d2-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e38d2-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="e38d2-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e38d2-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                  | <span data-ttu-id="e38d2-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e38d2-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="e38d2-122"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e38d2-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>     | <span data-ttu-id="e38d2-123">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="e38d2-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="e38d2-124"><dt>**VM \_ \_ \_ \_ Falha de desanexação de USB E**</dt> <dt>0xA00400927</dt></span><span class="sxs-lookup"><span data-stu-id="e38d2-124"><dt>**VM\_E\_USB\_DETACH\_FAILED**</dt> <dt>0xA00400927</dt></span></span> </dl> | <span data-ttu-id="e38d2-125">Falha na operação de desanexação.</span><span class="sxs-lookup"><span data-stu-id="e38d2-125">The detach operation failed.</span></span><br/>        |
| <dl> <span data-ttu-id="e38d2-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e38d2-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="e38d2-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e38d2-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="e38d2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e38d2-128">Requirements</span></span>



| <span data-ttu-id="e38d2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e38d2-129">Requirement</span></span> | <span data-ttu-id="e38d2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e38d2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e38d2-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e38d2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e38d2-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e38d2-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e38d2-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e38d2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e38d2-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e38d2-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e38d2-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e38d2-135">End of client support</span></span><br/>    | <span data-ttu-id="e38d2-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e38d2-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e38d2-137">Produto</span><span class="sxs-lookup"><span data-stu-id="e38d2-137">Product</span></span><br/>                  | <span data-ttu-id="e38d2-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e38d2-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e38d2-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e38d2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e38d2-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e38d2-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e38d2-141">IID</span><span class="sxs-lookup"><span data-stu-id="e38d2-141">IID</span></span><br/>                      | <span data-ttu-id="e38d2-142">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e38d2-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e38d2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e38d2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e38d2-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e38d2-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

