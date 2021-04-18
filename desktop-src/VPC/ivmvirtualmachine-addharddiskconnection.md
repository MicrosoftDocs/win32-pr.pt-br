---
title: Método IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
description: Adiciona uma nova conexão de disco rígido à máquina virtual.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- AddHardDiskConnection do método virtual PC
- Método AddHardDiskConnection Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748734"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a><span data-ttu-id="6066e-106">Método IVMVirtualMachine:: AddHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="6066e-106">IVMVirtualMachine::AddHardDiskConnection method</span></span>

<span data-ttu-id="6066e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6066e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6066e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6066e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6066e-109">Adiciona uma nova conexão de disco rígido à VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="6066e-109">Adds a new hard disk connection to the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="6066e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6066e-110">Syntax</span></span>


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="6066e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6066e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6066e-112">*hardDiskPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6066e-112">*hardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6066e-113">O caminho completo do arquivo de disco rígido virtual (VHD) a ser conectado.</span><span class="sxs-lookup"><span data-stu-id="6066e-113">The full path of the virtual hard disk (VHD) file to connect.</span></span>

</dd> <dt>

<span data-ttu-id="6066e-114">*busNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6066e-114">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6066e-115">O barramento ao qual a unidade será anexada.</span><span class="sxs-lookup"><span data-stu-id="6066e-115">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="6066e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6066e-116">Value</span></span>                                                                        | <span data-ttu-id="6066e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="6066e-117">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="6066e-118"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-118"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6066e-119">A unidade será anexada ao primeiro barramento.</span><span class="sxs-lookup"><span data-stu-id="6066e-119">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="6066e-120"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-120"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6066e-121">A unidade será anexada ao segundo barramento.</span><span class="sxs-lookup"><span data-stu-id="6066e-121">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6066e-122">*deviceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6066e-122">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6066e-123">O dispositivo ao qual a unidade será anexada.</span><span class="sxs-lookup"><span data-stu-id="6066e-123">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="6066e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6066e-124">Value</span></span>                                                                        | <span data-ttu-id="6066e-125">Significado</span><span class="sxs-lookup"><span data-stu-id="6066e-125">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6066e-126"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-126"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6066e-127">A unidade será anexada ao primeiro dispositivo no barramento.</span><span class="sxs-lookup"><span data-stu-id="6066e-127">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="6066e-128"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-128"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6066e-129">A unidade será anexada ao segundo dispositivo no barramento.</span><span class="sxs-lookup"><span data-stu-id="6066e-129">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6066e-130">*hardDiskConnection* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6066e-130">*hardDiskConnection* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6066e-131">Um objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="6066e-131">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6066e-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6066e-132">Return value</span></span>

<span data-ttu-id="6066e-133">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6066e-133">This method can return one of these values.</span></span>



| <span data-ttu-id="6066e-134">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6066e-134">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="6066e-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="6066e-135">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6066e-136"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-136"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="6066e-137">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6066e-137">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="6066e-138"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6066e-138"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="6066e-139">O parâmetro *hardDiskConnection* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6066e-139">The *hardDiskConnection* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6066e-140"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-140"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="6066e-141">Um parâmetro *hardDiskPath* é **nulo** ou o parâmetro *busNumber* ou *deviceNumber* não é válido.</span><span class="sxs-lookup"><span data-stu-id="6066e-141">A *hardDiskPath* parameter is **NULL** or the *busNumber* or *deviceNumber* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6066e-142"><dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="6066e-143">O sistema não pode localizar o arquivo especificado pelo parâmetro *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="6066e-143">The system cannot find the file specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="6066e-144"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="6066e-145">O sistema não pode localizar o caminho especificado pelo parâmetro *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="6066e-145">The system cannot find the path specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="6066e-146"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="6066e-147">O parâmetro *hardDiskPath* contém um caractere inválido (um de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="6066e-147">The *hardDiskPath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6066e-148"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="6066e-149">O parâmetro *hardDiskPath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="6066e-149">The *hardDiskPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6066e-150">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="6066e-150">An absolute path is required.</span></span><br/>                                                |
| <dl> <span data-ttu-id="6066e-151"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-151"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="6066e-152">O caminho especificado pelo parâmetro *hardDiskPath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="6066e-152">The path specified by the *hardDiskPath* parameter is too long.</span></span> <span data-ttu-id="6066e-153">O caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6066e-153">The path must be less than 260 characters.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6066e-154"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6066e-154"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                              | <span data-ttu-id="6066e-155">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="6066e-155">The configuration is unknown.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="6066e-156"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-156"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>                   | <span data-ttu-id="6066e-157">A VM está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="6066e-157">The VM is in a running or saved state.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="6066e-158"><dt>**VM \_ \_ \_ Barramento de unidade E \_ loc \_ in \_ usar**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-158"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl>                | <span data-ttu-id="6066e-159">O local do barramento especificado está em uso.</span><span class="sxs-lookup"><span data-stu-id="6066e-159">The specified bus location is in use.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="6066e-160"><dt>**VM \_ E \_ \_ \_ arquivo HD inválido**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-160"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="6066e-161">O VHD é maior que 127 GB e não pode ser conectado ao barramento IDE.</span><span class="sxs-lookup"><span data-stu-id="6066e-161">The VHD is greater than 127 GB and cannot be connected to the IDE bus.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="6066e-162"><dt>**VM \_ E \_ \_ \_ \_ tipo de disco HD sem suporte**</dt> <dt>0xA00400686</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-162"><dt>**VM\_E\_UNSUPPORTED\_HD\_DISK\_TYPE**</dt> <dt>0xA00400686</dt></span></span> </dl>             | <span data-ttu-id="6066e-163">O parâmetro *hardDiskPath* refere-se a um VHD vinculado ou a um VHD diferencial para um VHD vinculado.</span><span class="sxs-lookup"><span data-stu-id="6066e-163">The *hardDiskPath* parameter refers to a linked VHD or a differencing VHD to a linked VHD.</span></span> <span data-ttu-id="6066e-164">VHDs vinculados não podem ser anexados a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="6066e-164">Linked VHDs cannot be attached to virtual machines.</span></span><br/> |
| <dl> <span data-ttu-id="6066e-165"><dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-165"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="6066e-166">O VHD especificado já está conectado a outro local de barramento para esta VM.</span><span class="sxs-lookup"><span data-stu-id="6066e-166">The specified VHD is already connected to another bus location for this VM.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="6066e-167"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6066e-167"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="6066e-168">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6066e-168">An unexpected error has occurred.</span></span><br/>                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6066e-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="6066e-169">Remarks</span></span>

<span data-ttu-id="6066e-170">Você só pode adicionar uma nova conexão de disco rígido a uma máquina virtual parada.</span><span class="sxs-lookup"><span data-stu-id="6066e-170">You can only add a new hard disk connection to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="6066e-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6066e-171">Requirements</span></span>



| <span data-ttu-id="6066e-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="6066e-172">Requirement</span></span> | <span data-ttu-id="6066e-173">Valor</span><span class="sxs-lookup"><span data-stu-id="6066e-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6066e-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6066e-174">Minimum supported client</span></span><br/> | <span data-ttu-id="6066e-175">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6066e-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6066e-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6066e-176">Minimum supported server</span></span><br/> | <span data-ttu-id="6066e-177">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6066e-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6066e-178">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6066e-178">End of client support</span></span><br/>    | <span data-ttu-id="6066e-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6066e-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6066e-180">Produto</span><span class="sxs-lookup"><span data-stu-id="6066e-180">Product</span></span><br/>                  | <span data-ttu-id="6066e-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6066e-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6066e-182">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6066e-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="6066e-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6066e-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6066e-184">IID</span><span class="sxs-lookup"><span data-stu-id="6066e-184">IID</span></span><br/>                      | <span data-ttu-id="6066e-185">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6066e-185">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6066e-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="6066e-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6066e-187">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="6066e-187">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

