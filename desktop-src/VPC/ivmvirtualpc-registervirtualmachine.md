---
title: Método IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces. h)
description: Registra uma configuração de máquina virtual existente e recupera o objeto de máquina virtual.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- RegisterVirtualMachine do método virtual PC
- Método RegisterVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método RegisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761171"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a><span data-ttu-id="a4682-106">Método IVMVirtualPC:: RegisterVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a4682-106">IVMVirtualPC::RegisterVirtualMachine method</span></span>

<span data-ttu-id="a4682-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a4682-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a4682-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a4682-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a4682-109">Registra uma configuração de máquina virtual existente e recupera o objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4682-109">Registers an existing virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4682-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4682-110">Syntax</span></span>


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="a4682-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4682-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4682-112">*ConfigurationName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4682-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4682-113">O nome da máquina virtual a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="a4682-113">The name of the virtual machine to be registered.</span></span> <span data-ttu-id="a4682-114">O comprimento do nome não pode exceder 80 caracteres e o comprimento combinado do nome e do caminho não pode exceder os caracteres do **\_ caminho máximo** (260).</span><span class="sxs-lookup"><span data-stu-id="a4682-114">The length of the name cannot exceed 80 characters and the combined length of the name and path cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="a4682-115">O nome especificado pode conter a extensão. vmc.</span><span class="sxs-lookup"><span data-stu-id="a4682-115">The specified name may contain the .vmc extension.</span></span> <span data-ttu-id="a4682-116">Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, o parâmetro *configurationPath* deverá especificar o caminho completo para o arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="a4682-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="a4682-117">*configurationPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4682-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4682-118">O caminho para a pasta que contém o arquivo de configuração existente.</span><span class="sxs-lookup"><span data-stu-id="a4682-118">The path to the folder that contains the existing configuration file.</span></span> <span data-ttu-id="a4682-119">Se o parâmetro *ConfigurationName* for **nulo** ou uma cadeia de caracteres vazia, isso deverá especificar o caminho completo para o arquivo de configuração existente.</span><span class="sxs-lookup"><span data-stu-id="a4682-119">If the *configurationName* parameter is **NULL** or an empty string, this must specify the full path to the existing configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="a4682-120">*VirtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a4682-120">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a4682-121">Um ponteiro para um novo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4682-121">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4682-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4682-122">Return value</span></span>

<span data-ttu-id="a4682-123">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a4682-123">This method can return one of these values.</span></span>



| <span data-ttu-id="a4682-124">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a4682-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="a4682-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4682-125">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a4682-126"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-126"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="a4682-127">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a4682-127">The operation was successful.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="a4682-128"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a4682-128"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="a4682-129">O parâmetro *ConfigurationName* ou *configurationPath* é inválido ou *VirtualMachine* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a4682-129">The *configurationName* or *configurationPath* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="a4682-130"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="a4682-131">O sistema não pode localizar o caminho especificado pelos parâmetros *ConfigurationName* e *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="a4682-131">The system cannot find the path specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="a4682-132"><dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="a4682-133">O sistema não pode localizar o arquivo especificado pelos parâmetros *ConfigurationName* e *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="a4682-133">The system cannot find the file specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="a4682-134"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="a4682-135">O parâmetro *configurationPath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="a4682-135">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="a4682-136"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="a4682-137">O parâmetro *configurationPath* do parâmetro especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="a4682-137">The parameter *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="a4682-138">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="a4682-138">An absolute path is required.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="a4682-139"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="a4682-140">O caminho especificado pelos parâmetros *ConfigurationName* e *configurationPath* resulta em um caminho muito longo.</span><span class="sxs-lookup"><span data-stu-id="a4682-140">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="a4682-141">O comprimento combinado do caminho deve ser menor que o **\_ caminho máximo** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="a4682-141">The combined length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="a4682-142"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="a4682-143">Já existe um arquivo de configuração com este nome neste local.</span><span class="sxs-lookup"><span data-stu-id="a4682-143">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="a4682-144"><dt>**VM \_ O \_ nome da configuração E é \_ \_ muito \_ longo**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-144"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="a4682-145">O parâmetro *ConfigurationName* excede 80 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a4682-145">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="a4682-146"><dt>**VM \_ Nome de config & 0xA0040402 de \_ \_ \_ \_ caracteres inválido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a4682-146"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="a4682-147">O parâmetro *ConfigurationName* contém um caractere inválido (um de " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="a4682-147">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="a4682-148"><dt>**VM \_ E \_ config \_ \_ nome duplicado**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-148"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="a4682-149">Já existe uma máquina virtual com esse nome.</span><span class="sxs-lookup"><span data-stu-id="a4682-149">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="a4682-150"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a4682-150"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="a4682-151">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="a4682-151">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="a4682-152"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a4682-152"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="a4682-153">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a4682-153">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="a4682-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4682-154">Remarks</span></span>

<span data-ttu-id="a4682-155">Os nomes de máquina virtual não diferenciam maiúsculas de minúsculas, por exemplo, "MyVM" e "MyVM" referem-se à mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4682-155">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4682-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4682-156">Requirements</span></span>



| <span data-ttu-id="a4682-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4682-157">Requirement</span></span> | <span data-ttu-id="a4682-158">Valor</span><span class="sxs-lookup"><span data-stu-id="a4682-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4682-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4682-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a4682-160">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a4682-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4682-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4682-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a4682-162">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a4682-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a4682-163">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a4682-163">End of client support</span></span><br/>    | <span data-ttu-id="a4682-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4682-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a4682-165">Produto</span><span class="sxs-lookup"><span data-stu-id="a4682-165">Product</span></span><br/>                  | <span data-ttu-id="a4682-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a4682-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a4682-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4682-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4682-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4682-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a4682-169">IID</span><span class="sxs-lookup"><span data-stu-id="a4682-169">IID</span></span><br/>                      | <span data-ttu-id="a4682-170">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a4682-170">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a4682-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4682-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4682-172">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a4682-172">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

