---
title: Método SetParameter IVMGuestOS (VPCCOMInterfaces. h)
description: Define um parâmetro nomeado dentro do sistema operacional convidado.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Método SetParameter Virtual PC
- Método SetParameter Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método SetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499414"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="01ad8-106">Método IVMGuestOS:: SetParameter</span><span class="sxs-lookup"><span data-stu-id="01ad8-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="01ad8-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01ad8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="01ad8-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="01ad8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="01ad8-109">Define um parâmetro nomeado dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="01ad8-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ad8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01ad8-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="01ad8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01ad8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ad8-112">*Inparametrizaname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01ad8-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01ad8-113">O nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="01ad8-113">The parameter name.</span></span> <span data-ttu-id="01ad8-114">Ele deve ter entre 1 e 255 caracteres de comprimento e não pode conter uma barra invertida ( \) caractere.</span><span class="sxs-lookup"><span data-stu-id="01ad8-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="01ad8-115">*Inparametervalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01ad8-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01ad8-116">O valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="01ad8-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ad8-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01ad8-117">Return value</span></span>

<span data-ttu-id="01ad8-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="01ad8-118">This method can return one of these values.</span></span>



| <span data-ttu-id="01ad8-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="01ad8-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="01ad8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="01ad8-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="01ad8-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01ad8-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="01ad8-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="01ad8-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="01ad8-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="01ad8-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="01ad8-124">Um parâmetro não é válido ou não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="01ad8-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="01ad8-125"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="01ad8-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="01ad8-126">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="01ad8-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="01ad8-127"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="01ad8-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="01ad8-128">A máquina virtual (VM) não está em execução.</span><span class="sxs-lookup"><span data-stu-id="01ad8-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="01ad8-129"><dt>**VM \_ E \_ VM em \_ pausa**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="01ad8-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="01ad8-130">A VM está pausada.</span><span class="sxs-lookup"><span data-stu-id="01ad8-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="01ad8-131"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="01ad8-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="01ad8-132">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="01ad8-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="01ad8-133"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="01ad8-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="01ad8-134">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="01ad8-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="01ad8-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="01ad8-135">Remarks</span></span>

<span data-ttu-id="01ad8-136">A VM deve estar em execução e os componentes de integração devem ser instalados quando esse método é invocado.</span><span class="sxs-lookup"><span data-stu-id="01ad8-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="01ad8-137">Esse método só tem suporte em sistemas operacionais convidados baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="01ad8-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="01ad8-138">Com os componentes de integração instalados, a chave a seguir é automaticamente adicionada ao registro do sistema operacional convidado:</span><span class="sxs-lookup"><span data-stu-id="01ad8-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="01ad8-139">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="01ad8-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="01ad8-140">Quando o sistema operacional convidado é iniciado, os seguintes valores de cadeia de caracteres do registro são populados na chave de **parâmetros** :</span><span class="sxs-lookup"><span data-stu-id="01ad8-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="01ad8-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="01ad8-141">**HostName**</span></span>
-   <span data-ttu-id="01ad8-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="01ad8-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="01ad8-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="01ad8-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="01ad8-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="01ad8-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="01ad8-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01ad8-145">Requirements</span></span>



| <span data-ttu-id="01ad8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ad8-146">Requirement</span></span> | <span data-ttu-id="01ad8-147">Valor</span><span class="sxs-lookup"><span data-stu-id="01ad8-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01ad8-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01ad8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="01ad8-149">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01ad8-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01ad8-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01ad8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="01ad8-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="01ad8-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="01ad8-152">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="01ad8-152">End of client support</span></span><br/>    | <span data-ttu-id="01ad8-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="01ad8-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="01ad8-154">Produto</span><span class="sxs-lookup"><span data-stu-id="01ad8-154">Product</span></span><br/>                  | <span data-ttu-id="01ad8-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="01ad8-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="01ad8-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01ad8-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="01ad8-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="01ad8-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="01ad8-158">IID</span><span class="sxs-lookup"><span data-stu-id="01ad8-158">IID</span></span><br/>                      | <span data-ttu-id="01ad8-159">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="01ad8-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="01ad8-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="01ad8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ad8-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="01ad8-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

