---
title: Método IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Anexa um dispositivo USB a uma VM.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- AttachUSBDevice do método virtual PC
- Método AttachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009498"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a><span data-ttu-id="00de3-106">Método IVMVirtualMachine:: AttachUSBDevice</span><span class="sxs-lookup"><span data-stu-id="00de3-106">IVMVirtualMachine::AttachUSBDevice method</span></span>

<span data-ttu-id="00de3-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="00de3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="00de3-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="00de3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="00de3-109">Anexa um dispositivo USB a uma máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="00de3-109">Attaches a USB device to a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="00de3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00de3-110">Syntax</span></span>


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="00de3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00de3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00de3-112">*inUSBDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00de3-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00de3-113">Um ponteiro [**IVMUSBDevice**](ivmusbdevice.md) que representa o dispositivo USB conectado ao host.</span><span class="sxs-lookup"><span data-stu-id="00de3-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device connected to the host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00de3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00de3-114">Return value</span></span>

<span data-ttu-id="00de3-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="00de3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="00de3-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="00de3-116">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="00de3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="00de3-117">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00de3-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="00de3-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="00de3-119">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="00de3-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="00de3-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="00de3-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="00de3-121">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="00de3-122"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                        | <span data-ttu-id="00de3-123">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="00de3-123">The VM is not running.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="00de3-124"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="00de3-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                             | <span data-ttu-id="00de3-125">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="00de3-125">The configuration is unknown.</span></span><br/>                                           |
| <dl> <span data-ttu-id="00de3-126"><dt>**VM \_ E \_ adições \_ não \_**</dt> <dt>0xA0040504</dt> disp.</span><span class="sxs-lookup"><span data-stu-id="00de3-126"><dt>**VM\_E\_ADDITIONS\_NOT\_AVAIL**</dt> <dt>0xA0040504</dt></span></span> </dl>                   | <span data-ttu-id="00de3-127">Os componentes de integração não estão disponíveis no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="00de3-127">Integration Components are not available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="00de3-128"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>          | <span data-ttu-id="00de3-129">O recurso USB não está disponível.</span><span class="sxs-lookup"><span data-stu-id="00de3-129">The USB feature is not available.</span></span><br/>                                       |
| <dl> <span data-ttu-id="00de3-130"><dt>**VM \_ \_Erro de \_ \_ Driver do \_ conector USB E**</dt> <dt>0xA00400925</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-130"><dt>**VM\_E\_USB\_CONNECTOR\_DRIVER\_ERROR**</dt> <dt>0xA00400925</dt></span></span> </dl>          | <span data-ttu-id="00de3-131">Ocorreu um erro de driver de conector USB.</span><span class="sxs-lookup"><span data-stu-id="00de3-131">There was a USB Connector driver error.</span></span><br/>                                 |
| <dl> <span data-ttu-id="00de3-132"><dt>**VM \_ \_ \_ Falha na conexão USB E \_ \_ mais \_ dispositivos**</dt> <dt>0xA00400931</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-132"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_MORE\_DEVICES**</dt> <dt>0xA00400931</dt></span></span> </dl>     | <span data-ttu-id="00de3-133">Não é possível anexar mais dispositivos à VM.</span><span class="sxs-lookup"><span data-stu-id="00de3-133">Cannot attach more devices to the VM.</span></span><br/>                                   |
| <dl> <span data-ttu-id="00de3-134"><dt>**VM \_ \_ \_ Falha na conexão de USB E \_ \_ \_ erro de GP**</dt> de <dt>0xA00400932</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-134"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_GP\_ERROR**</dt> <dt>0xA00400932</dt></span></span> </dl>         | <span data-ttu-id="00de3-135">Uma configuração de política de grupo está impedindo o redirecionamento de USB.</span><span class="sxs-lookup"><span data-stu-id="00de3-135">A group policy setting is preventing the USB redirection.</span></span><br/>               |
| <dl> <span data-ttu-id="00de3-136"><dt>**VM \_ Falha de conexão do E \_ USB \_ \_ \_ já \_ atribuída**</dt> <dt>0xA00400933</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-136"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_ALREADY\_ASSIGNED**</dt> <dt>0xA00400933</dt></span></span> </dl> | <span data-ttu-id="00de3-137">Um dispositivo USB já foi anexado por outro cliente.</span><span class="sxs-lookup"><span data-stu-id="00de3-137">A USB device has already been attached by some other client.</span></span><br/>            |
| <dl> <span data-ttu-id="00de3-138"><dt>**VM \_ \_Falha de \_ conexão \_ USB E**</dt> <dt>0xA00400926</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-138"><dt>**VM\_E\_USB\_ATTACH\_FAILED**</dt> <dt>0xA00400926</dt></span></span> </dl>                    | <span data-ttu-id="00de3-139">Falha na operação de anexação.</span><span class="sxs-lookup"><span data-stu-id="00de3-139">The attach operation failed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="00de3-140"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="00de3-140"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="00de3-141">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="00de3-141">An unexpected error has occurred.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="00de3-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00de3-142">Requirements</span></span>



| <span data-ttu-id="00de3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="00de3-143">Requirement</span></span> | <span data-ttu-id="00de3-144">Valor</span><span class="sxs-lookup"><span data-stu-id="00de3-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00de3-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00de3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="00de3-146">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="00de3-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00de3-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00de3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="00de3-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="00de3-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="00de3-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="00de3-149">End of client support</span></span><br/>    | <span data-ttu-id="00de3-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="00de3-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="00de3-151">Produto</span><span class="sxs-lookup"><span data-stu-id="00de3-151">Product</span></span><br/>                  | <span data-ttu-id="00de3-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="00de3-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="00de3-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00de3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="00de3-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="00de3-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="00de3-155">IID</span><span class="sxs-lookup"><span data-stu-id="00de3-155">IID</span></span><br/>                      | <span data-ttu-id="00de3-156">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="00de3-156">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="00de3-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="00de3-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00de3-158">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="00de3-158">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

