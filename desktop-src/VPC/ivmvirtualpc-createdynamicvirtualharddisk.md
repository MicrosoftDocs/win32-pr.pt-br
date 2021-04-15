---
title: Método IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces. h)
description: Cria um disco rígido virtual de redimensionamento dinâmico.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- CreateDynamicVirtualHardDisk do método virtual PC
- Método CreateDynamicVirtualHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método CreateDynamicVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d245072fd5b3135decd814a29dd8a87d2b6a956
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369922"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a><span data-ttu-id="9e1b1-106">Método IVMVirtualPC:: CreateDynamicVirtualHardDisk</span><span class="sxs-lookup"><span data-stu-id="9e1b1-106">IVMVirtualPC::CreateDynamicVirtualHardDisk method</span></span>

<span data-ttu-id="9e1b1-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9e1b1-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9e1b1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9e1b1-109">Cria um disco rígido virtual de redimensionamento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-109">Creates a dynamically resizing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1b1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e1b1-110">Syntax</span></span>


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="9e1b1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e1b1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e1b1-112">*imagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e1b1-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e1b1-113">O caminho completo para o novo arquivo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-113">The full path to the new disk image file.</span></span> <span data-ttu-id="9e1b1-114">A pasta que a contém será criada se não existir.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9e1b1-115">*tamanho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e1b1-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e1b1-116">O tamanho da imagem, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-116">The size of the image, in megabytes.</span></span> <span data-ttu-id="9e1b1-117">Esse valor pode ter no máximo 2.088.960 MB (2040GB).</span><span class="sxs-lookup"><span data-stu-id="9e1b1-117">This value can be at most 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="9e1b1-118">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9e1b1-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9e1b1-119">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a criação da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e1b1-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e1b1-120">Return value</span></span>

<span data-ttu-id="9e1b1-121">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-121">This method can return one of these values.</span></span>



| <span data-ttu-id="9e1b1-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9e1b1-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9e1b1-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e1b1-123">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e1b1-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="9e1b1-125">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="9e1b1-126"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="9e1b1-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="9e1b1-127">Um parâmetro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="9e1b1-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="9e1b1-129">O parâmetro *size* é menor ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="9e1b1-130"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="9e1b1-131">O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="9e1b1-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="9e1b1-132"><dt>**HRESULT \_ Do \_ Win32 (unidade de erro \_ inválida \_ )**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="9e1b1-133">O arquivo especificado pelo parâmetro *imagePath* está em um CD-ROM ou DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="9e1b1-134"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="9e1b1-135">O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="9e1b1-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="9e1b1-136"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="9e1b1-137">O parâmetro *imagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="9e1b1-138">Pelo menos um dos parâmetros deve ser um caminho absoluto.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-138">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="9e1b1-139"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="9e1b1-140">O caminho especificado pelo parâmetro *imagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="9e1b1-141">O comprimento do caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-141">The length of the path must be less than 260 characters.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="9e1b1-142"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="9e1b1-143">O arquivo referenciado pelo parâmetro *imagePath* já existe.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="9e1b1-144"><dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="9e1b1-145">A imagem de disco rígido virtual de expansão dinâmica precisa de pelo menos 8 MB livres no volume do host.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="9e1b1-146"><dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="9e1b1-147">O *tamanho* do parâmetro deve ser menor que 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-147">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="9e1b1-148">Se o formato for FAT16, o tamanho deverá ser menor que 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-148">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="9e1b1-149"><dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ pequeno**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="9e1b1-150">As imagens de disco rígido virtual formatado e FAT16 não formatados devem ter pelo menos 3 MB.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="9e1b1-151">As imagens de disco rígido virtual formatado para FAT32 devem ter pelo menos 514 MB.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="9e1b1-152"><dt>**VM \_ \_Arquivo E \_ muito \_ grande \_ para o \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="9e1b1-153">O volume do host não poderá dar suporte a um arquivo esse tamanho se a imagem do disco rígido virtual de expansão dinâmica expandir para seu limite completo.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-153">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="9e1b1-154">O tamanho máximo do arquivo para um volume FAT32 é 4 GB.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="9e1b1-155">O tamanho máximo do arquivo para um volume FAT16 é 2 GB.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="9e1b1-156"><dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="9e1b1-157">O disco rígido virtual não pode ser criado depois que o aplicativo inicia o desligamento.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="9e1b1-158"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="9e1b1-159">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="9e1b1-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="9e1b1-160"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="9e1b1-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="9e1b1-161">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-161">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="9e1b1-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e1b1-162">Requirements</span></span>



| <span data-ttu-id="9e1b1-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e1b1-163">Requirement</span></span> | <span data-ttu-id="9e1b1-164">Valor</span><span class="sxs-lookup"><span data-stu-id="9e1b1-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1b1-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e1b1-165">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1b1-166">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9e1b1-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e1b1-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e1b1-167">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1b1-168">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9e1b1-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9e1b1-169">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9e1b1-169">End of client support</span></span><br/>    | <span data-ttu-id="9e1b1-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e1b1-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9e1b1-171">Produto</span><span class="sxs-lookup"><span data-stu-id="9e1b1-171">Product</span></span><br/>                  | <span data-ttu-id="9e1b1-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9e1b1-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9e1b1-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e1b1-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e1b1-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9e1b1-175">IID</span><span class="sxs-lookup"><span data-stu-id="9e1b1-175">IID</span></span><br/>                      | <span data-ttu-id="9e1b1-176">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="9e1b1-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9e1b1-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e1b1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e1b1-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="9e1b1-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

