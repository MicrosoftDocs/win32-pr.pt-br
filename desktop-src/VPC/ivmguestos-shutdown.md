---
title: Método de desligamento IVMGuestOS (VPCCOMInterfaces. h)
description: Desliga o sistema operacional convidado na VM.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Método de desligamento Virtual PC
- Método de desligamento Virtual PC, interface IVMGuestOS
- Virtual PC de interface IVMGuestOS, método de desligamento
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644790"
---
# <a name="ivmguestosshutdown-method"></a><span data-ttu-id="10b30-106">Método IVMGuestOS:: Shutdown</span><span class="sxs-lookup"><span data-stu-id="10b30-106">IVMGuestOS::Shutdown method</span></span>

<span data-ttu-id="10b30-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="10b30-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="10b30-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="10b30-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="10b30-109">Desliga o sistema operacional convidado na VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="10b30-109">Shuts down the guest operating system in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="10b30-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10b30-110">Syntax</span></span>


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a><span data-ttu-id="10b30-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10b30-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b30-112">*Isforced* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10b30-112">*isForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b30-113">**Variante \_ TRUE** se o desligamento for forçado, **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="10b30-113">**VARIANT\_TRUE** if the shutdown is to be forced, **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="10b30-114">*outShutdownTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="10b30-114">*outShutdownTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="10b30-115">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="10b30-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the shutdown process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b30-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10b30-116">Return value</span></span>

<span data-ttu-id="10b30-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="10b30-117">This method can return one of these values.</span></span>



| <span data-ttu-id="10b30-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="10b30-118">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="10b30-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="10b30-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10b30-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="10b30-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="10b30-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="10b30-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="10b30-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="10b30-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="10b30-123">O parâmetro *outShutdownTask* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="10b30-123">The *outShutdownTask* parameter is **NULL**.</span></span><br/>                    |
| <dl> <span data-ttu-id="10b30-124"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="10b30-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="10b30-125">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="10b30-125">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="10b30-126"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="10b30-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="10b30-127">Não foi possível encontrar a VM.</span><span class="sxs-lookup"><span data-stu-id="10b30-127">The VM could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="10b30-128"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="10b30-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="10b30-129">A VM deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="10b30-129">The VM must be running for this operation.</span></span><br/>                      |
| <dl> <span data-ttu-id="10b30-130"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="10b30-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="10b30-131">O chamador deve ter permissões de acesso de execução para esta VM.</span><span class="sxs-lookup"><span data-stu-id="10b30-131">The caller must have execute access permissions for this VM.</span></span><br/>    |
| <dl> <span data-ttu-id="10b30-132"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="10b30-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="10b30-133">O recurso componentes de integração não está instalado nesta VM.</span><span class="sxs-lookup"><span data-stu-id="10b30-133">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="10b30-134"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="10b30-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="10b30-135">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="10b30-135">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="10b30-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="10b30-136">Remarks</span></span>

<span data-ttu-id="10b30-137">A VM deve estar em execução e o recurso de componentes de integração deve ser instalado quando esse método é invocado.</span><span class="sxs-lookup"><span data-stu-id="10b30-137">The VM must be running and integration components feature must be installed when this method is invoked.</span></span> <span data-ttu-id="10b30-138">Esse método só tem suporte em sistemas operacionais convidados baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="10b30-138">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="10b30-139">Os valores a seguir podem ser retornados por meio da propriedade [**Error**](ivmtask-error.md) do objeto [**IVMTask**](ivmtask.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="10b30-139">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="10b30-140">Código/valor do [**erro**](ivmtask-error.md)</span><span class="sxs-lookup"><span data-stu-id="10b30-140">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="10b30-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="10b30-141">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="10b30-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="10b30-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="10b30-143">O chamador deve ter permissões de acesso de execução para esta VM.</span><span class="sxs-lookup"><span data-stu-id="10b30-143">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="10b30-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="10b30-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="10b30-145">O computador está bloqueado e não pode ser desligado sem a opção Force.</span><span class="sxs-lookup"><span data-stu-id="10b30-145">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="10b30-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="10b30-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="10b30-147">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="10b30-147">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="10b30-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="10b30-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="10b30-149">Um desligamento do sistema está em andamento.</span><span class="sxs-lookup"><span data-stu-id="10b30-149">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="10b30-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b30-150">Requirements</span></span>



| <span data-ttu-id="10b30-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b30-151">Requirement</span></span> | <span data-ttu-id="10b30-152">Valor</span><span class="sxs-lookup"><span data-stu-id="10b30-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b30-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10b30-153">Minimum supported client</span></span><br/> | <span data-ttu-id="10b30-154">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="10b30-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10b30-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10b30-155">Minimum supported server</span></span><br/> | <span data-ttu-id="10b30-156">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="10b30-156">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="10b30-157">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="10b30-157">End of client support</span></span><br/>    | <span data-ttu-id="10b30-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10b30-158">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="10b30-159">Produto</span><span class="sxs-lookup"><span data-stu-id="10b30-159">Product</span></span><br/>                  | <span data-ttu-id="10b30-160">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="10b30-160">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="10b30-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10b30-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b30-162"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b30-162"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="10b30-163">IID</span><span class="sxs-lookup"><span data-stu-id="10b30-163">IID</span></span><br/>                      | <span data-ttu-id="10b30-164">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="10b30-164">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="10b30-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="10b30-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b30-166">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="10b30-166">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

