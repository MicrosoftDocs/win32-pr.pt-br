---
title: Método Convert de IVMHardDisk (VPCCOMInterfaces. h)
description: Converte um disco rígido virtual de tamanho fixo em um disco rígido virtual de expansão dinâmica ou converte um disco rígido virtual de expansão dinâmica em um disco rígido virtual de tamanho fixo.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Converter o método virtual PC
- Converter método virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Método Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455842"
---
# <a name="ivmharddiskconvert-method"></a><span data-ttu-id="59eae-106">Método IVMHardDisk:: Convert</span><span class="sxs-lookup"><span data-stu-id="59eae-106">IVMHardDisk::Convert method</span></span>

<span data-ttu-id="59eae-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59eae-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59eae-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59eae-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59eae-109">Converte um disco rígido virtual de tamanho fixo em um disco rígido virtual de expansão dinâmica ou converte um disco rígido virtual de expansão dinâmica em um disco rígido virtual de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="59eae-109">Converts a fixed-size virtual hard disk to a dynamically expanding virtual hard disk or converts a dynamically expanding virtual hard disk to a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="59eae-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59eae-110">Syntax</span></span>


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a><span data-ttu-id="59eae-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59eae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59eae-112">*convertedDiskImagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59eae-112">*convertedDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59eae-113">O caminho para o arquivo de imagem de disco de destino.</span><span class="sxs-lookup"><span data-stu-id="59eae-113">The path to the target disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="59eae-114">*convertedDiskImageType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59eae-114">*convertedDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59eae-115">O tipo da imagem do disco de destino.</span><span class="sxs-lookup"><span data-stu-id="59eae-115">The type of the target disk image.</span></span> <span data-ttu-id="59eae-116">Para obter uma lista de valores, consulte [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="59eae-116">For a list of values, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="59eae-117">*convertTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="59eae-117">*convertTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="59eae-118">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de conversão.</span><span class="sxs-lookup"><span data-stu-id="59eae-118">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the conversion process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59eae-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59eae-119">Return value</span></span>

<span data-ttu-id="59eae-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="59eae-120">This method can return one of these values.</span></span>



| <span data-ttu-id="59eae-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="59eae-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="59eae-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="59eae-122">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59eae-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="59eae-124">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="59eae-124">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="59eae-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="59eae-126">O parâmetro *convertedDiskImagePath* está vazio ou não tem a extensão. vhd no nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="59eae-126">The *convertedDiskImagePath* parameter is empty or missing the .vhd extension on the file name.</span></span><br/>                                      |
| <dl> <span data-ttu-id="59eae-127"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="59eae-127"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="59eae-128">Um parâmetro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="59eae-128">A parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="59eae-129"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="59eae-130">O sistema não pode localizar o caminho especificado pelo parâmetro *convertedDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="59eae-130">The system cannot find the path specified by the *convertedDiskImagePath* parameter.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="59eae-131"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="59eae-132">O parâmetro *convertedDiskImagePath* contém um caractere inválido (um de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="59eae-132">The *convertedDiskImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="59eae-133"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="59eae-134">O parâmetro *convertedDiskImagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="59eae-134">The *convertedDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="59eae-135">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="59eae-135">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="59eae-136"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="59eae-137">O caminho especificado pelo parâmetro *convertedDiskImagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="59eae-137">The path specified by the *convertedDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="59eae-138">O caminho deve ser menor que **o \_ caminho máximo** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="59eae-138">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="59eae-139"><dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="59eae-140">O disco rígido virtual referenciado por este objeto está em uso ou o pai deste disco rígido virtual está em uso.</span><span class="sxs-lookup"><span data-stu-id="59eae-140">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                  |
| <dl> <span data-ttu-id="59eae-141"><dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="59eae-142">O volume do host não tem espaço suficiente para converter este disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="59eae-142">The host volume does not have enough space to convert this virtual hard disk.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="59eae-143"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-143"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="59eae-144">O arquivo referenciado pelo parâmetro *convertedDiskImagePath* já existe.</span><span class="sxs-lookup"><span data-stu-id="59eae-144">The file referenced by the *convertedDiskImagePath* parameter already exists.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="59eae-145"><dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-145"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="59eae-146">O parâmetro *convertedDiskImagePath* deve ser **VmDiskType \_ dinâmico** ou **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="59eae-146">The *convertedDiskImagePath* parameter must be either **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/>                          |
| <dl> <span data-ttu-id="59eae-147"><dt>**VM \_ E \_ \_ \_ arquivo HD inválido**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-147"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="59eae-148">A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) não parece ser uma imagem válida.</span><span class="sxs-lookup"><span data-stu-id="59eae-148">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |
| <dl> <span data-ttu-id="59eae-149"><dt>**VM \_ E \_ \_ caminho pai \_ não \_ encontrado**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-149"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="59eae-150">O pai do disco rígido virtual referenciado por este objeto não existe.</span><span class="sxs-lookup"><span data-stu-id="59eae-150">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="59eae-151"><dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-151"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="59eae-152">A imagem do disco rígido virtual não pode ser convertida porque o aplicativo está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="59eae-152">The virtual hard disk image cannot be converted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="59eae-153"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="59eae-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="59eae-154">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="59eae-154">An unexpected error has occurred.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="59eae-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="59eae-155">Remarks</span></span>

<span data-ttu-id="59eae-156">O arquivo de origem permanece intacto após o processo de conversão.</span><span class="sxs-lookup"><span data-stu-id="59eae-156">The source file is left intact after the conversion process.</span></span>

## <a name="requirements"></a><span data-ttu-id="59eae-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59eae-157">Requirements</span></span>



| <span data-ttu-id="59eae-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="59eae-158">Requirement</span></span> | <span data-ttu-id="59eae-159">Valor</span><span class="sxs-lookup"><span data-stu-id="59eae-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59eae-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59eae-160">Minimum supported client</span></span><br/> | <span data-ttu-id="59eae-161">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="59eae-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59eae-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59eae-162">Minimum supported server</span></span><br/> | <span data-ttu-id="59eae-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="59eae-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="59eae-164">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="59eae-164">End of client support</span></span><br/>    | <span data-ttu-id="59eae-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59eae-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59eae-166">Produto</span><span class="sxs-lookup"><span data-stu-id="59eae-166">Product</span></span><br/>                  | <span data-ttu-id="59eae-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59eae-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="59eae-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59eae-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="59eae-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59eae-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="59eae-170">IID</span><span class="sxs-lookup"><span data-stu-id="59eae-170">IID</span></span><br/>                      | <span data-ttu-id="59eae-171">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="59eae-171">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="59eae-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="59eae-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59eae-173">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="59eae-173">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

