---
title: Método de reinicialização IVMGuestOS (VPCCOMInterfaces. h)
description: Reinicia o sistema operacional convidado.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Método de reinicialização Virtual PC
- Método de reinicialização Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, restart Method
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369663"
---
# <a name="ivmguestosrestart-method"></a><span data-ttu-id="31c64-106">Método IVMGuestOS:: Restart</span><span class="sxs-lookup"><span data-stu-id="31c64-106">IVMGuestOS::Restart method</span></span>

<span data-ttu-id="31c64-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="31c64-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="31c64-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="31c64-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="31c64-109">Reinicia o sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="31c64-109">Restarts the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c64-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31c64-110">Syntax</span></span>


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a><span data-ttu-id="31c64-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31c64-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c64-112">Não *forçado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31c64-112">*inForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31c64-113">**Variante \_ TRUE** se uma reinicialização forçada for necessária e **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="31c64-113">**VARIANT\_TRUE** if a forced restart is required and **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="31c64-114">*outRestartTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="31c64-114">*outRestartTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="31c64-115">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso da conclusão da sequência de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="31c64-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the restart sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31c64-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31c64-116">Return value</span></span>

<span data-ttu-id="31c64-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="31c64-117">This method can return one of these values.</span></span>



| <span data-ttu-id="31c64-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="31c64-118">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="31c64-119">Description</span><span class="sxs-lookup"><span data-stu-id="31c64-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31c64-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31c64-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="31c64-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="31c64-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="31c64-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="31c64-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="31c64-123">O parâmetro *outRestartTask* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="31c64-123">The *outRestartTask* parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="31c64-124"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="31c64-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="31c64-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="31c64-125">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="31c64-126"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="31c64-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="31c64-127">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="31c64-127">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="31c64-128"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="31c64-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="31c64-129">A máquina virtual (VM) deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="31c64-129">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="31c64-130"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="31c64-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="31c64-131">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="31c64-131">The configuration is unknown.</span></span><br/>                                   |
| <dl> <span data-ttu-id="31c64-132"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="31c64-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="31c64-133">O recurso componentes de integração não está instalado nesta VM.</span><span class="sxs-lookup"><span data-stu-id="31c64-133">The integration components feature is not installed in this VM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31c64-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="31c64-134">Remarks</span></span>

<span data-ttu-id="31c64-135">Os valores a seguir podem ser retornados por meio da propriedade [**Error**](ivmtask-error.md) do objeto [**IVMTask**](ivmtask.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="31c64-135">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="31c64-136">Código/valor do [**erro**](ivmtask-error.md)</span><span class="sxs-lookup"><span data-stu-id="31c64-136">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="31c64-137">Description</span><span class="sxs-lookup"><span data-stu-id="31c64-137">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31c64-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="31c64-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="31c64-139">O chamador deve ter permissões de acesso de execução para esta VM.</span><span class="sxs-lookup"><span data-stu-id="31c64-139">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="31c64-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="31c64-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="31c64-141">O computador está bloqueado e não pode ser desligado sem a opção Force.</span><span class="sxs-lookup"><span data-stu-id="31c64-141">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="31c64-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="31c64-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="31c64-143">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="31c64-143">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="31c64-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="31c64-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="31c64-145">Um desligamento do sistema está em andamento.</span><span class="sxs-lookup"><span data-stu-id="31c64-145">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="31c64-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31c64-146">Requirements</span></span>



| <span data-ttu-id="31c64-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="31c64-147">Requirement</span></span> | <span data-ttu-id="31c64-148">Valor</span><span class="sxs-lookup"><span data-stu-id="31c64-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c64-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31c64-149">Minimum supported client</span></span><br/> | <span data-ttu-id="31c64-150">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="31c64-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31c64-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31c64-151">Minimum supported server</span></span><br/> | <span data-ttu-id="31c64-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="31c64-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="31c64-153">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="31c64-153">End of client support</span></span><br/>    | <span data-ttu-id="31c64-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31c64-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="31c64-155">Produto</span><span class="sxs-lookup"><span data-stu-id="31c64-155">Product</span></span><br/>                  | <span data-ttu-id="31c64-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="31c64-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="31c64-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31c64-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c64-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="31c64-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="31c64-159">IID</span><span class="sxs-lookup"><span data-stu-id="31c64-159">IID</span></span><br/>                      | <span data-ttu-id="31c64-160">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="31c64-160">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="31c64-161">Consulte também</span><span class="sxs-lookup"><span data-stu-id="31c64-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c64-162">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="31c64-162">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

