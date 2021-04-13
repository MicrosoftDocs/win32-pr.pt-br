---
title: Método IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces. h)
description: Cria uma nova configuração de máquina virtual e recupera o objeto de máquina virtual.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- CreateVirtualMachine do método virtual PC
- Método CreateVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método CreateVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455625"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a><span data-ttu-id="b57e4-106">Método IVMVirtualPC:: CreateVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b57e4-106">IVMVirtualPC::CreateVirtualMachine method</span></span>

<span data-ttu-id="b57e4-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b57e4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b57e4-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b57e4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b57e4-109">Cria uma nova configuração de máquina virtual e recupera o objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b57e4-109">Creates a new virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b57e4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b57e4-110">Syntax</span></span>


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="b57e4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b57e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b57e4-112">*ConfigurationName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b57e4-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57e4-113">O nome da máquina virtual a ser criada.</span><span class="sxs-lookup"><span data-stu-id="b57e4-113">The name of the virtual machine to be created.</span></span> <span data-ttu-id="b57e4-114">O comprimento do nome não pode exceder 80 caracteres e o comprimento combinado do nome e do caminho para arquivos VMC e VMCX não pode exceder os caracteres de **\_ caminho máximo** (260).</span><span class="sxs-lookup"><span data-stu-id="b57e4-114">The length of the name cannot exceed 80 characters and the combined length of the name and path to VMC and VMCX files cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="b57e4-115">As extensões de nome de arquivo. VMC e. vmcx serão acrescentadas ao final do nome da máquina virtual quando os arquivos de configuração forem criados.</span><span class="sxs-lookup"><span data-stu-id="b57e4-115">The file name extensions .vmc and .vmcx will be appended to the end of the virtual machine name when the configuration files are created.</span></span> <span data-ttu-id="b57e4-116">Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, o parâmetro *configurationPath* deverá especificar o caminho completo para o arquivo VMC.</span><span class="sxs-lookup"><span data-stu-id="b57e4-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the VMC file.</span></span>

</dd> <dt>

<span data-ttu-id="b57e4-117">*configurationPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b57e4-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57e4-118">O caminho para a pasta que conterá o arquivo VMC.</span><span class="sxs-lookup"><span data-stu-id="b57e4-118">The path to the folder that will contain the VMC file.</span></span> <span data-ttu-id="b57e4-119">Essa pasta será criada se não existir.</span><span class="sxs-lookup"><span data-stu-id="b57e4-119">This folder will be created if it does not exist.</span></span> <span data-ttu-id="b57e4-120">Se *ConfigurationName* for **nulo** ou uma cadeia de caracteres vazia, isso deverá especificar o caminho completo do novo arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="b57e4-120">If *configurationName* is **NULL** or an empty string, this must specify the full path of the new configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="b57e4-121">*VirtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b57e4-121">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b57e4-122">Um ponteiro para um novo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b57e4-122">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b57e4-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b57e4-123">Return value</span></span>

<span data-ttu-id="b57e4-124">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b57e4-124">This method can return one of these values.</span></span>



| <span data-ttu-id="b57e4-125">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b57e4-125">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b57e4-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="b57e4-126">Description</span></span>                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b57e4-127"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-127"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b57e4-128">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b57e4-128">The operation was successful.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="b57e4-129"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b57e4-129"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b57e4-130">O parâmetro *ConfigurationName* ou *configurationPath* não é válido ou o parâmetro *VirtualMachine* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b57e4-130">The *configurationName* or *configurationPath* parameter is not valid, or the *virtualMachine* parameter is **NULL**.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="b57e4-131"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="b57e4-132">O sistema não pode localizar o caminho especificado pelo parâmetro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="b57e4-132">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="b57e4-133"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="b57e4-134">O parâmetro *configurationPath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="b57e4-134">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="b57e4-135"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="b57e4-136">O parâmetro *configurationPath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="b57e4-136">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="b57e4-137">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="b57e4-137">An absolute path is required.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="b57e4-138"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="b57e4-139">O caminho especificado pelos parâmetros *ConfigurationName* e *configurationPath* resulta em um caminho muito longo.</span><span class="sxs-lookup"><span data-stu-id="b57e4-139">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="b57e4-140">O comprimento total do caminho deve ser menor que o **\_ caminho máximo** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="b57e4-140">The total length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="b57e4-141"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="b57e4-142">Já existe um arquivo de configuração com este nome neste local.</span><span class="sxs-lookup"><span data-stu-id="b57e4-142">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="b57e4-143"><dt>**VM \_ E \_ config \_ sem \_ nome**</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-143"><dt>**VM\_E\_CONFIG\_NO\_NAME**</dt> <dt>0xA0040400</dt></span></span> </dl>                       | <span data-ttu-id="b57e4-144">O parâmetro *ConfigurationName* está vazio.</span><span class="sxs-lookup"><span data-stu-id="b57e4-144">The *configurationName* parameter is empty.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="b57e4-145"><dt>**VM \_ O \_ nome da configuração E é \_ \_ muito \_ longo**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-145"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="b57e4-146">O parâmetro *ConfigurationName* excede 80 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="b57e4-146">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="b57e4-147"><dt>**VM \_ Nome de config & 0xA0040402 de \_ \_ \_ \_ caracteres inválido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-147"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="b57e4-148">O parâmetro *ConfigurationName* contém um caractere inválido (um de " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="b57e4-148">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="b57e4-149"><dt>**VM \_ E \_ config \_ \_ nome duplicado**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-149"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="b57e4-150">Já existe uma máquina virtual com esse nome.</span><span class="sxs-lookup"><span data-stu-id="b57e4-150">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="b57e4-151"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-151"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="b57e4-152">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="b57e4-152">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="b57e4-153"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b57e4-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b57e4-154">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b57e4-154">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="b57e4-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="b57e4-155">Remarks</span></span>

<span data-ttu-id="b57e4-156">Os nomes de máquina virtual não diferenciam maiúsculas de minúsculas, por exemplo, "MyVM" e "MyVM" referem-se à mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b57e4-156">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57e4-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b57e4-157">Requirements</span></span>



| <span data-ttu-id="b57e4-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="b57e4-158">Requirement</span></span> | <span data-ttu-id="b57e4-159">Valor</span><span class="sxs-lookup"><span data-stu-id="b57e4-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b57e4-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57e4-160">Minimum supported client</span></span><br/> | <span data-ttu-id="b57e4-161">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b57e4-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b57e4-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57e4-162">Minimum supported server</span></span><br/> | <span data-ttu-id="b57e4-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b57e4-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b57e4-164">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b57e4-164">End of client support</span></span><br/>    | <span data-ttu-id="b57e4-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b57e4-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b57e4-166">Produto</span><span class="sxs-lookup"><span data-stu-id="b57e4-166">Product</span></span><br/>                  | <span data-ttu-id="b57e4-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b57e4-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b57e4-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b57e4-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="b57e4-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b57e4-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b57e4-170">IID</span><span class="sxs-lookup"><span data-stu-id="b57e4-170">IID</span></span><br/>                      | <span data-ttu-id="b57e4-171">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="b57e4-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b57e4-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="b57e4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57e4-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="b57e4-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

