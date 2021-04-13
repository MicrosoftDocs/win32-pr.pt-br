---
title: Método getParameter IVMGuestOS (VPCCOMInterfaces. h)
description: Recupera um parâmetro nomeado dentro do sistema operacional convidado.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- PC virtual do método getParameter
- Método getParameter Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método getParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499714"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="ab6e3-106">Método IVMGuestOS:: getParameter</span><span class="sxs-lookup"><span data-stu-id="ab6e3-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="ab6e3-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ab6e3-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ab6e3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ab6e3-109">Recupera um parâmetro nomeado dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6e3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab6e3-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="ab6e3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab6e3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6e3-112">*Inparametrizaname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab6e3-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6e3-113">O nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-113">The parameter name.</span></span> <span data-ttu-id="ab6e3-114">Ele deve ter entre 1 e 255 caracteres de comprimento e não pode conter uma barra invertida ( \) caractere.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="ab6e3-115">*ParameterValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ab6e3-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6e3-116">O valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6e3-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab6e3-117">Return value</span></span>

<span data-ttu-id="ab6e3-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-118">This method can return one of these values.</span></span>



| <span data-ttu-id="ab6e3-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ab6e3-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="ab6e3-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab6e3-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab6e3-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e3-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="ab6e3-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="ab6e3-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e3-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="ab6e3-124">Um parâmetro não é válido ou não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="ab6e3-125"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="ab6e3-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="ab6e3-126">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="ab6e3-127"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e3-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="ab6e3-128">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="ab6e3-129"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e3-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="ab6e3-130">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="ab6e3-131"><dt>**VM \_ E \_ VM em \_ pausa**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e3-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="ab6e3-132">A máquina virtual está pausada.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ab6e3-133"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e3-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="ab6e3-134">Os componentes de integração não estão instalados nesta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="ab6e3-135"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="ab6e3-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="ab6e3-136">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="ab6e3-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab6e3-137">Remarks</span></span>

<span data-ttu-id="ab6e3-138">A máquina virtual deve estar em execução e os componentes de integração devem ser instalados quando esse método é invocado.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="ab6e3-139">Esse método só tem suporte em sistemas operacionais convidados baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="ab6e3-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="ab6e3-140">Com os componentes de integração instalados, a chave a seguir é automaticamente adicionada ao registro do sistema operacional convidado:</span><span class="sxs-lookup"><span data-stu-id="ab6e3-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="ab6e3-141">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="ab6e3-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="ab6e3-142">Quando o sistema operacional convidado é iniciado, os seguintes valores de cadeia de caracteres do registro são populados na chave de **parâmetros** :</span><span class="sxs-lookup"><span data-stu-id="ab6e3-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="ab6e3-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="ab6e3-143">**HostName**</span></span>
-   <span data-ttu-id="ab6e3-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="ab6e3-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="ab6e3-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="ab6e3-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="ab6e3-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="ab6e3-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6e3-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab6e3-147">Requirements</span></span>



| <span data-ttu-id="ab6e3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab6e3-148">Requirement</span></span> | <span data-ttu-id="ab6e3-149">Valor</span><span class="sxs-lookup"><span data-stu-id="ab6e3-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6e3-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab6e3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6e3-151">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ab6e3-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab6e3-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab6e3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6e3-153">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ab6e3-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ab6e3-154">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ab6e3-154">End of client support</span></span><br/>    | <span data-ttu-id="ab6e3-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab6e3-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ab6e3-156">Produto</span><span class="sxs-lookup"><span data-stu-id="ab6e3-156">Product</span></span><br/>                  | <span data-ttu-id="ab6e3-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ab6e3-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ab6e3-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab6e3-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab6e3-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e3-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ab6e3-160">IID</span><span class="sxs-lookup"><span data-stu-id="ab6e3-160">IID</span></span><br/>                      | <span data-ttu-id="ab6e3-161">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="ab6e3-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ab6e3-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab6e3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6e3-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="ab6e3-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

