---
title: Método de logoff IVMGuestOS (VPCCOMInterfaces. h)
description: Faz logoff de todos os usuários do sistema operacional convidado.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Método de logoff Virtual PC
- Método de logoff Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método logoff
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009727"
---
# <a name="ivmguestoslogoff-method"></a><span data-ttu-id="82e56-106">Método IVMGuestOS:: logoff</span><span class="sxs-lookup"><span data-stu-id="82e56-106">IVMGuestOS::Logoff method</span></span>

<span data-ttu-id="82e56-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="82e56-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82e56-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="82e56-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82e56-109">Faz logoff de todos os usuários do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="82e56-109">Logs off all users from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e56-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82e56-110">Syntax</span></span>


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a><span data-ttu-id="82e56-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82e56-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e56-112">*outLogoffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="82e56-112">*outLogoffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="82e56-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso da conclusão da sequência de logoff.</span><span class="sxs-lookup"><span data-stu-id="82e56-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the logoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e56-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82e56-114">Return value</span></span>

<span data-ttu-id="82e56-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="82e56-115">This method can return one of these values.</span></span>



| <span data-ttu-id="82e56-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="82e56-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="82e56-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="82e56-117">Description</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82e56-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82e56-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="82e56-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="82e56-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="82e56-120"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="82e56-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="82e56-121">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="82e56-121">An unexpected error has occurred.</span></span><br/>                                            |
| <dl> <span data-ttu-id="82e56-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="82e56-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="82e56-123">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="82e56-123">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="82e56-124"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="82e56-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="82e56-125">O chamador deve ter permissões de acesso de execução para esta VM.</span><span class="sxs-lookup"><span data-stu-id="82e56-125">The caller must have execute access permissions for this VM.</span></span><br/>                 |
| <dl> <span data-ttu-id="82e56-126"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="82e56-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="82e56-127">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="82e56-127">The operation did not complete in a timely manner.</span></span><br/>                           |
| <dl> <span data-ttu-id="82e56-128"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="82e56-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="82e56-129">O recurso componentes de integração não está instalado nesta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82e56-129">The integration components feature is not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="82e56-130"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="82e56-130"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="82e56-131">A máquina virtual (VM) deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="82e56-131">The virtual machine (VM) must be running for this operation.</span></span><br/>                 |
| <dl> <span data-ttu-id="82e56-132"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="82e56-132"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="82e56-133">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="82e56-133">The configuration is unknown.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="82e56-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="82e56-134">Remarks</span></span>

<span data-ttu-id="82e56-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) é retornado por meio da propriedade [**Error**](ivmtask-error.md) do objeto [**IVMTask**](ivmtask.md) retornado não há nenhuma sessão de logon no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="82e56-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) is returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object there are no logon sessions in the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="82e56-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82e56-136">Requirements</span></span>



| <span data-ttu-id="82e56-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e56-137">Requirement</span></span> | <span data-ttu-id="82e56-138">Valor</span><span class="sxs-lookup"><span data-stu-id="82e56-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e56-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82e56-139">Minimum supported client</span></span><br/> | <span data-ttu-id="82e56-140">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="82e56-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82e56-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82e56-141">Minimum supported server</span></span><br/> | <span data-ttu-id="82e56-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="82e56-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82e56-143">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="82e56-143">End of client support</span></span><br/>    | <span data-ttu-id="82e56-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82e56-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82e56-145">Produto</span><span class="sxs-lookup"><span data-stu-id="82e56-145">Product</span></span><br/>                  | <span data-ttu-id="82e56-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82e56-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82e56-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82e56-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="82e56-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="82e56-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="82e56-149">IID</span><span class="sxs-lookup"><span data-stu-id="82e56-149">IID</span></span><br/>                      | <span data-ttu-id="82e56-150">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="82e56-150">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="82e56-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="82e56-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e56-152">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="82e56-152">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

