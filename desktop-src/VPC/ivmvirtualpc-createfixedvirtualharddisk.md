---
title: Método IVMVirtualPC CreateFixedVirtualHardDisk (VPCCOMInterfaces. h)
description: Cria um disco rígido virtual de tamanho fixo.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- CreateFixedVirtualHardDisk do método virtual PC
- Método CreateFixedVirtualHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método CreateFixedVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1c260611ba3a8b55f87f23d0957c53a304a471
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085649"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a><span data-ttu-id="9c981-106">Método IVMVirtualPC:: CreateFixedVirtualHardDisk</span><span class="sxs-lookup"><span data-stu-id="9c981-106">IVMVirtualPC::CreateFixedVirtualHardDisk method</span></span>

<span data-ttu-id="9c981-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9c981-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9c981-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9c981-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9c981-109">Cria um disco rígido virtual de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="9c981-109">Creates a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c981-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c981-110">Syntax</span></span>


```C++
HRESULT CreateFixedVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="9c981-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c981-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c981-112">*imagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c981-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c981-113">O caminho completo para o novo arquivo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="9c981-113">The full path to the new disk image file.</span></span> <span data-ttu-id="9c981-114">A pasta que a contém será criada se não existir.</span><span class="sxs-lookup"><span data-stu-id="9c981-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9c981-115">*tamanho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c981-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c981-116">O tamanho, em megabytes, da imagem.</span><span class="sxs-lookup"><span data-stu-id="9c981-116">The size, in megabytes, of the image.</span></span> <span data-ttu-id="9c981-117">O tamanho máximo é 2.088.960 MB (2040GB).</span><span class="sxs-lookup"><span data-stu-id="9c981-117">Maximum size is 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="9c981-118">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9c981-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9c981-119">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a criação da imagem.</span><span class="sxs-lookup"><span data-stu-id="9c981-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c981-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c981-120">Return value</span></span>

<span data-ttu-id="9c981-121">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9c981-121">This method can return one of these values.</span></span>



| <span data-ttu-id="9c981-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9c981-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9c981-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c981-123">Description</span></span>                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c981-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="9c981-125">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9c981-125">The operation was successful.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="9c981-126"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="9c981-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="9c981-127">Um parâmetro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9c981-127">A parameter is **NULL**.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="9c981-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="9c981-129">O parâmetro *size* é menor ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="9c981-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="9c981-130"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="9c981-131">O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="9c981-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="9c981-132"><dt>**HRESULT \_ Do \_ Win32 (unidade de erro \_ inválida \_ )**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="9c981-133">O arquivo especificado pelo parâmetro *imagePath* está em um CD-ROM ou DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9c981-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="9c981-134"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="9c981-135">O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="9c981-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="9c981-136"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="9c981-137">O parâmetro *imagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="9c981-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="9c981-138">Pelo menos um dos parâmetros deve ser um caminho absoluto.</span><span class="sxs-lookup"><span data-stu-id="9c981-138">At least one of the parameters must be an absolute path.</span></span><br/>                         |
| <dl> <span data-ttu-id="9c981-139"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="9c981-140">O caminho especificado pelo parâmetro *imagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="9c981-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="9c981-141">O comprimento do caminho deve ser menor que o **\_ caminho máximo** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="9c981-141">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/>                |
| <dl> <span data-ttu-id="9c981-142"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="9c981-143">O arquivo referenciado pelo parâmetro *imagePath* já existe.</span><span class="sxs-lookup"><span data-stu-id="9c981-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="9c981-144"><dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="9c981-145">A imagem de disco rígido virtual de expansão dinâmica precisa de pelo menos 8 MB livres no volume do host.</span><span class="sxs-lookup"><span data-stu-id="9c981-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="9c981-146"><dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="9c981-147">O parâmetro de *tamanho* deve ser menor que 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="9c981-147">The *size* parameter must be less than 2,088,960 MB.</span></span> <span data-ttu-id="9c981-148">Se o formato for FAT16, o parâmetro *size* deverá ser menor que 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="9c981-148">If the format is FAT16, then the *size* parameter must be less than 2000 MB.</span></span><br/>                    |
| <dl> <span data-ttu-id="9c981-149"><dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ pequeno**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="9c981-150">As imagens de disco rígido virtual formatado e FAT16 não formatados devem ter pelo menos 3 MB.</span><span class="sxs-lookup"><span data-stu-id="9c981-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="9c981-151">As imagens de disco rígido virtual formatado para FAT32 devem ter pelo menos 514 MB.</span><span class="sxs-lookup"><span data-stu-id="9c981-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>    |
| <dl> <span data-ttu-id="9c981-152"><dt>**VM \_ \_Arquivo E \_ muito \_ grande \_ para o \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="9c981-153">O volume do host não pode dar suporte a um arquivo com esse tamanho.</span><span class="sxs-lookup"><span data-stu-id="9c981-153">The host volume cannot support a file this size.</span></span> <span data-ttu-id="9c981-154">O tamanho máximo do arquivo para um volume FAT32 é 4 GB.</span><span class="sxs-lookup"><span data-stu-id="9c981-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="9c981-155">O tamanho máximo do arquivo para um volume FAT16 é 2 GB.</span><span class="sxs-lookup"><span data-stu-id="9c981-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="9c981-156"><dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="9c981-157">O disco rígido virtual não pode ser criado depois que o aplicativo inicia o desligamento.</span><span class="sxs-lookup"><span data-stu-id="9c981-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="9c981-158"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9c981-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="9c981-159">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="9c981-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="9c981-160"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="9c981-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="9c981-161">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="9c981-161">An unexpected error has occurred.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="9c981-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c981-162">Requirements</span></span>



| <span data-ttu-id="9c981-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c981-163">Requirement</span></span> | <span data-ttu-id="9c981-164">Valor</span><span class="sxs-lookup"><span data-stu-id="9c981-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c981-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c981-165">Minimum supported client</span></span><br/> | <span data-ttu-id="9c981-166">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9c981-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c981-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c981-167">Minimum supported server</span></span><br/> | <span data-ttu-id="9c981-168">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9c981-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9c981-169">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9c981-169">End of client support</span></span><br/>    | <span data-ttu-id="9c981-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c981-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9c981-171">Produto</span><span class="sxs-lookup"><span data-stu-id="9c981-171">Product</span></span><br/>                  | <span data-ttu-id="9c981-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9c981-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9c981-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c981-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c981-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c981-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9c981-175">IID</span><span class="sxs-lookup"><span data-stu-id="9c981-175">IID</span></span><br/>                      | <span data-ttu-id="9c981-176">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="9c981-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9c981-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c981-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c981-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="9c981-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

