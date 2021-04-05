---
title: Método Mergeto IVMHardDisk (VPCCOMInterfaces. h)
description: Mescla um disco rígido virtual diferencial com todos os seus pais.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- PC virtual do método Mergeto
- Método Mergeto Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, método Mergeto
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085651"
---
# <a name="ivmharddiskmergeto-method"></a><span data-ttu-id="6af74-106">Método IVMHardDisk:: Mergeto</span><span class="sxs-lookup"><span data-stu-id="6af74-106">IVMHardDisk::MergeTo method</span></span>

<span data-ttu-id="6af74-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6af74-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6af74-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6af74-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6af74-109">Mescla um disco rígido virtual diferencial com todos os seus pais (até e incluindo o disco rígido virtual pai raiz) em um novo arquivo de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="6af74-109">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af74-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6af74-110">Syntax</span></span>


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="6af74-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6af74-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af74-112">*newDiskImagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6af74-112">*newDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af74-113">O caminho para a nova imagem de disco de destino em que as imagens de disco selecionadas serão mescladas.</span><span class="sxs-lookup"><span data-stu-id="6af74-113">The path to the new target disk image where the selected disk images will be merged.</span></span>

</dd> <dt>

<span data-ttu-id="6af74-114">*newDiskImageType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6af74-114">*newDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af74-115">O tipo de imagem do novo disco de destino.</span><span class="sxs-lookup"><span data-stu-id="6af74-115">The type of new target disk image.</span></span> <span data-ttu-id="6af74-116">Os tipos de imagem permitidos para a nova imagem de disco de destino são **vmDiskType \_ Dynamic** e **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="6af74-116">The image types allowed for the new target disk image are **vmDiskType\_Dynamic** and **vmDiskType\_FixedSize**.</span></span> <span data-ttu-id="6af74-117">Para obter mais informações, consulte [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="6af74-117">For more information, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="6af74-118">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6af74-118">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6af74-119">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="6af74-119">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af74-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6af74-120">Return value</span></span>

<span data-ttu-id="6af74-121">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6af74-121">This method can return one of these values.</span></span>



| <span data-ttu-id="6af74-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6af74-122">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="6af74-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="6af74-123">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6af74-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="6af74-125">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6af74-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="6af74-126"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6af74-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="6af74-127">Um parâmetro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6af74-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="6af74-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="6af74-129">O parâmetro *newDiskImagePath* está vazio.</span><span class="sxs-lookup"><span data-stu-id="6af74-129">The *newDiskImagePath* parameter is empty.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="6af74-130"><dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="6af74-131">O sistema não pode localizar o arquivo especificado pelo parâmetro *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="6af74-131">The system cannot find the file specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="6af74-132"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="6af74-133">O sistema não pode localizar o caminho especificado pelo parâmetro *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="6af74-133">The system cannot find the path specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="6af74-134"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="6af74-135">O parâmetro *newDiskImagePath* contém um caractere inválido (um dos seguintes: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="6af74-135">The *newDiskImagePath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="6af74-136"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="6af74-137">O parâmetro *newDiskImagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="6af74-137">The *newDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6af74-138">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="6af74-138">An absolute path is required.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="6af74-139"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="6af74-140">O caminho especificado pelo parâmetro *newDiskImagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="6af74-140">The path specified by the *newDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="6af74-141">O caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6af74-141">The path must be less than 260 characters.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="6af74-142"><dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="6af74-143">O disco rígido virtual referenciado por este objeto está em uso ou o pai deste disco rígido virtual está em uso.</span><span class="sxs-lookup"><span data-stu-id="6af74-143">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="6af74-144"><dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-144"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="6af74-145">Esse erro é causado porque a imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) não é uma imagem de disco diferencial ou porque o parâmetro *newDiskImageType* não é um dos valores aceitos, **vmDiskType \_ Dynamic** ou **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="6af74-145">This error is caused either because the virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is not a differencing disk image or because the parameter *newDiskImageType* is not one of the accepted values, **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/> |
| <dl> <span data-ttu-id="6af74-146"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="6af74-147">O arquivo referenciado pelo parâmetro *newDiskImagePath* já existe.</span><span class="sxs-lookup"><span data-stu-id="6af74-147">The file referenced by the *newDiskImagePath* parameter already exists.</span></span><br/>                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="6af74-148"><dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="6af74-149">O volume do host não tem espaço suficiente para mesclar este disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="6af74-149">The host volume does not have enough space to merge this virtual hard disk.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="6af74-150"><dt>**VM \_ E \_ \_ caminho pai \_ não \_ encontrado**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-150"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="6af74-151">O pai do disco rígido virtual referenciado por este objeto não existe.</span><span class="sxs-lookup"><span data-stu-id="6af74-151">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="6af74-152"><dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-152"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="6af74-153">A imagem do disco rígido virtual não pode ser mesclada porque o aplicativo está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="6af74-153">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="6af74-154"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6af74-154"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="6af74-155">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6af74-155">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="6af74-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6af74-156">Requirements</span></span>



| <span data-ttu-id="6af74-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af74-157">Requirement</span></span> | <span data-ttu-id="6af74-158">Valor</span><span class="sxs-lookup"><span data-stu-id="6af74-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af74-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6af74-159">Minimum supported client</span></span><br/> | <span data-ttu-id="6af74-160">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6af74-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6af74-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6af74-161">Minimum supported server</span></span><br/> | <span data-ttu-id="6af74-162">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6af74-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6af74-163">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6af74-163">End of client support</span></span><br/>    | <span data-ttu-id="6af74-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6af74-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6af74-165">Produto</span><span class="sxs-lookup"><span data-stu-id="6af74-165">Product</span></span><br/>                  | <span data-ttu-id="6af74-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6af74-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6af74-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6af74-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af74-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6af74-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6af74-169">IID</span><span class="sxs-lookup"><span data-stu-id="6af74-169">IID</span></span><br/>                      | <span data-ttu-id="6af74-170">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="6af74-170">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6af74-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="6af74-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af74-172">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="6af74-172">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

