---
title: Método IVMVirtualPC CreateDifferencingVirtualHardDisk (VPCCOMInterfaces. h)
description: Cria um disco rígido virtual diferencial.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- CreateDifferencingVirtualHardDisk do método virtual PC
- Método CreateDifferencingVirtualHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método CreateDifferencingVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770580"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a><span data-ttu-id="03248-106">Método IVMVirtualPC:: CreateDifferencingVirtualHardDisk</span><span class="sxs-lookup"><span data-stu-id="03248-106">IVMVirtualPC::CreateDifferencingVirtualHardDisk method</span></span>

<span data-ttu-id="03248-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="03248-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="03248-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="03248-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="03248-109">Cria um disco rígido virtual diferencial.</span><span class="sxs-lookup"><span data-stu-id="03248-109">Creates a differencing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="03248-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03248-110">Syntax</span></span>


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="03248-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03248-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03248-112">*imagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03248-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03248-113">O caminho para o novo arquivo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="03248-113">The path to the new disk image file.</span></span> <span data-ttu-id="03248-114">A pasta que a contém será criada se não existir.</span><span class="sxs-lookup"><span data-stu-id="03248-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="03248-115">*ParentPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03248-115">*parentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03248-116">O caminho para o arquivo de imagem de disco pai.</span><span class="sxs-lookup"><span data-stu-id="03248-116">The path to the parent disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="03248-117">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="03248-117">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="03248-118">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a criação da imagem.</span><span class="sxs-lookup"><span data-stu-id="03248-118">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03248-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03248-119">Return value</span></span>

<span data-ttu-id="03248-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="03248-120">This method can return one of these values.</span></span>



| <span data-ttu-id="03248-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="03248-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="03248-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="03248-122">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03248-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03248-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="03248-124">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="03248-124">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="03248-125"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="03248-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="03248-126">Um parâmetro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="03248-126">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="03248-127"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="03248-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="03248-128">O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* ou *ParentPath* .</span><span class="sxs-lookup"><span data-stu-id="03248-128">The system cannot find the path specified by the *imagePath* or *parentPath* parameter.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="03248-129"><dt>**HRESULT \_ Do \_ Win32 (unidade de erro \_ inválida \_ )**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="03248-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="03248-130">O arquivo especificado pelo parâmetro *imagePath* está em um CD-ROM ou DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="03248-130">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="03248-131"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="03248-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="03248-132">O parâmetro *imagePath* ou *ParentPath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="03248-132">The *imagePath* or *parentPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="03248-133"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="03248-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="03248-134">O parâmetro *imagePath* e *ParentPath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="03248-134">Both the *imagePath* and *parentPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="03248-135">Pelo menos um dos parâmetros deve ser um caminho absoluto.</span><span class="sxs-lookup"><span data-stu-id="03248-135">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="03248-136"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="03248-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="03248-137">O caminho especificado pelos parâmetros *imagePath* ou *ParentPath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="03248-137">The path specified by the *imagePath* or *parentPath* parameters is too long.</span></span> <span data-ttu-id="03248-138">O comprimento do caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="03248-138">The length of the path must be less than 260 characters.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="03248-139"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="03248-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="03248-140">O arquivo referenciado pelo parâmetro *imagePath* já existe.</span><span class="sxs-lookup"><span data-stu-id="03248-140">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="03248-141"><dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="03248-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="03248-142">A imagem de disco rígido virtual de expansão dinâmica precisa de pelo menos 8 MB livres no volume do host.</span><span class="sxs-lookup"><span data-stu-id="03248-142">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="03248-143"><dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="03248-143"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="03248-144">O *tamanho* do parâmetro deve ser menor que 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="03248-144">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="03248-145">Se o formato for FAT16, o tamanho deverá ser menor que 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="03248-145">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="03248-146"><dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ pequeno**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="03248-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="03248-147">As imagens de disco rígido virtual formatado e FAT16 não formatados devem ter pelo menos 3 MB.</span><span class="sxs-lookup"><span data-stu-id="03248-147">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="03248-148">As imagens de disco rígido virtual formatado para FAT32 devem ter pelo menos 514 MB.</span><span class="sxs-lookup"><span data-stu-id="03248-148">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="03248-149"><dt>**VM \_ \_Arquivo E \_ muito \_ grande \_ para o \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="03248-149"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="03248-150">O volume do host não poderá dar suporte a um arquivo esse tamanho se a imagem do disco rígido virtual de expansão dinâmica expandir para seu limite completo.</span><span class="sxs-lookup"><span data-stu-id="03248-150">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="03248-151">O tamanho máximo do arquivo para um volume FAT32 é 4 GB.</span><span class="sxs-lookup"><span data-stu-id="03248-151">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="03248-152">O tamanho máximo do arquivo para um volume FAT16 é 2 GB.</span><span class="sxs-lookup"><span data-stu-id="03248-152">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="03248-153"><dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="03248-153"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="03248-154">O disco rígido virtual não pode ser criado depois que o aplicativo inicia o desligamento.</span><span class="sxs-lookup"><span data-stu-id="03248-154">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="03248-155"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="03248-155"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="03248-156">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="03248-156">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="03248-157"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="03248-157"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="03248-158">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="03248-158">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="03248-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="03248-159">Remarks</span></span>

<span data-ttu-id="03248-160">Embora o *imagePath* ou o *ParentPath* possa ser um caminho relativo, pelo menos um deles deve ser um caminho absoluto.</span><span class="sxs-lookup"><span data-stu-id="03248-160">Although either *imagePath* or *parentPath* can be a relative path, at least one of these must be an absolute path.</span></span> <span data-ttu-id="03248-161">Se um parâmetro de caminho for um caminho relativo, ele será considerado relativo ao outro parâmetro de caminho.</span><span class="sxs-lookup"><span data-stu-id="03248-161">If one path parameter is a relative path, it is assumed to be relative to the other path parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="03248-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03248-162">Requirements</span></span>



| <span data-ttu-id="03248-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="03248-163">Requirement</span></span> | <span data-ttu-id="03248-164">Valor</span><span class="sxs-lookup"><span data-stu-id="03248-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="03248-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03248-165">Minimum supported client</span></span><br/> | <span data-ttu-id="03248-166">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="03248-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03248-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03248-167">Minimum supported server</span></span><br/> | <span data-ttu-id="03248-168">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="03248-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="03248-169">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="03248-169">End of client support</span></span><br/>    | <span data-ttu-id="03248-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03248-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="03248-171">Produto</span><span class="sxs-lookup"><span data-stu-id="03248-171">Product</span></span><br/>                  | <span data-ttu-id="03248-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="03248-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="03248-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03248-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="03248-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="03248-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="03248-175">IID</span><span class="sxs-lookup"><span data-stu-id="03248-175">IID</span></span><br/>                      | <span data-ttu-id="03248-176">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="03248-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="03248-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="03248-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03248-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="03248-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

