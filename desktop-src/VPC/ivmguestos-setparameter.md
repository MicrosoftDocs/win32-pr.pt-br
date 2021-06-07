---
title: Método IVMGuestOS SetParameter (VPCCOMInterfaces.h)
description: Define um parâmetro nomeado dentro do sistema operacional convidado.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Computador Virtual do método SetParameter
- Método SetParameter Pc Virtual, interface IVMGuestOS
- INTERFACE IVMGuestOS pc virtual, método SetParameter
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
ms.openlocfilehash: 2cc99d9b38ab43327b4a435c4128378d49682935
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386705"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="62e18-106">Método IVMGuestOS::SetParameter</span><span class="sxs-lookup"><span data-stu-id="62e18-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="62e18-107">\[O Computador Virtual do Windows não está mais disponível para uso a partir Windows 8.</span><span class="sxs-lookup"><span data-stu-id="62e18-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="62e18-108">Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="62e18-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="62e18-109">Define um parâmetro nomeado dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="62e18-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e18-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62e18-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="62e18-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62e18-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e18-112">*inParameterName* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="62e18-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62e18-113">O nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="62e18-113">The parameter name.</span></span> <span data-ttu-id="62e18-114">Ele deve ter entre 1 e 255 caracteres e não pode conter um caractere de invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="62e18-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\\) character.</span></span>

</dd> <dt>

<span data-ttu-id="62e18-115">*inParameterValue* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="62e18-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62e18-116">O valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="62e18-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e18-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62e18-117">Return value</span></span>

<span data-ttu-id="62e18-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="62e18-118">This method can return one of these values.</span></span>



| <span data-ttu-id="62e18-119">Valor/código de retorno</span><span class="sxs-lookup"><span data-stu-id="62e18-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="62e18-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="62e18-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="62e18-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="62e18-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="62e18-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="62e18-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="62e18-124">Um parâmetro não é válido ou não especificado.</span><span class="sxs-lookup"><span data-stu-id="62e18-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="62e18-125"><dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="62e18-126">A operação não foi concluída em tempo hábil.</span><span class="sxs-lookup"><span data-stu-id="62e18-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="62e18-127"><dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="62e18-128">A VM (máquina virtual) não está em execução.</span><span class="sxs-lookup"><span data-stu-id="62e18-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="62e18-129"><dt>**VM \_ E \_ VM \_ PAUSADA**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="62e18-130">A VM está em pausa.</span><span class="sxs-lookup"><span data-stu-id="62e18-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="62e18-131"><dt>**VM \_ O \_ RECURSO DE \_ ADIÇÕES E NÃO \_ \_ É**</dt> <dt>0XA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="62e18-132">Os componentes de integração não estão instalados nessa VM.</span><span class="sxs-lookup"><span data-stu-id="62e18-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="62e18-133"><dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="62e18-134">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="62e18-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="62e18-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="62e18-135">Remarks</span></span>

<span data-ttu-id="62e18-136">A VM deve estar em execução e os componentes de integração devem ser instalados quando esse método é invocado.</span><span class="sxs-lookup"><span data-stu-id="62e18-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="62e18-137">Esse método só tem suporte para sistemas operacionais convidados baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="62e18-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="62e18-138">Com os componentes de integração instalados, a seguinte chave é adicionada automaticamente ao registro do sistema operacional convidado:</span><span class="sxs-lookup"><span data-stu-id="62e18-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="62e18-139">**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="62e18-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="62e18-140">Quando o sistema operacional convidado é iniciado, os seguintes valores de cadeia de caracteres do Registro são preenchidos na **chave Parâmetros:**</span><span class="sxs-lookup"><span data-stu-id="62e18-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="62e18-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="62e18-141">**HostName**</span></span>
-   <span data-ttu-id="62e18-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="62e18-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="62e18-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="62e18-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="62e18-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="62e18-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="62e18-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62e18-145">Requirements</span></span>



| <span data-ttu-id="62e18-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e18-146">Requirement</span></span> | <span data-ttu-id="62e18-147">Valor</span><span class="sxs-lookup"><span data-stu-id="62e18-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62e18-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62e18-148">Minimum supported client</span></span><br/> | <span data-ttu-id="62e18-149">Somente aplicativos \[ da área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="62e18-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62e18-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62e18-150">Minimum supported server</span></span><br/> | <span data-ttu-id="62e18-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62e18-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="62e18-152">Fim do suporte ao cliente</span><span class="sxs-lookup"><span data-stu-id="62e18-152">End of client support</span></span><br/>    | <span data-ttu-id="62e18-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="62e18-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="62e18-154">Produto</span><span class="sxs-lookup"><span data-stu-id="62e18-154">Product</span></span><br/>                  | <span data-ttu-id="62e18-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="62e18-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="62e18-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="62e18-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e18-157"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="62e18-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="62e18-158">IID</span><span class="sxs-lookup"><span data-stu-id="62e18-158">IID</span></span><br/>                      | <span data-ttu-id="62e18-159">IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="62e18-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="62e18-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="62e18-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e18-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="62e18-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

