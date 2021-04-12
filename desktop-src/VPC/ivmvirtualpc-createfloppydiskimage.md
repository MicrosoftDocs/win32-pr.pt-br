---
title: Método IVMVirtualPC CreateFloppyDiskImage (VPCCOMInterfaces. h)
description: Cria um arquivo de imagem de disquete.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- CreateFloppyDiskImage do método virtual PC
- Método CreateFloppyDiskImage Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método CreateFloppyDiskImage
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455624"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a><span data-ttu-id="6e3b9-106">Método IVMVirtualPC:: CreateFloppyDiskImage</span><span class="sxs-lookup"><span data-stu-id="6e3b9-106">IVMVirtualPC::CreateFloppyDiskImage method</span></span>

<span data-ttu-id="6e3b9-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6e3b9-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6e3b9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6e3b9-109">Cria um arquivo de imagem de disquete.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-109">Creates a floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3b9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e3b9-110">Syntax</span></span>


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a><span data-ttu-id="6e3b9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e3b9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e3b9-112">*imagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e3b9-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3b9-113">O caminho completo para o novo arquivo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-113">The full path to the new disk image file.</span></span> <span data-ttu-id="6e3b9-114">A pasta que a contém será criada se não existir.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="6e3b9-115">*ImageType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e3b9-115">*imageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3b9-116">O tipo de imagem de disquete a ser criado.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-116">The type of floppy disk image to create.</span></span> <span data-ttu-id="6e3b9-117">Somente **vmFloppyDiskImage \_ LowDensity** (1) e **vmFloppyDiskImage \_ Highdensity** (2) têm suporte.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-117">Only **vmFloppyDiskImage\_LowDensity** (1) and **vmFloppyDiskImage\_HighDensity** (2) are supported.</span></span> <span data-ttu-id="6e3b9-118">Consulte [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="6e3b9-118">See [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e3b9-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e3b9-119">Return value</span></span>

<span data-ttu-id="6e3b9-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-120">This method can return one of these values.</span></span>



| <span data-ttu-id="6e3b9-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6e3b9-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="6e3b9-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e3b9-122">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e3b9-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-123"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="6e3b9-124">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-124">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="6e3b9-125"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6e3b9-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="6e3b9-126">O parâmetro *imagePath* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-126">The *imagePath* parameter is **NULL**.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="6e3b9-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="6e3b9-128">O parâmetro *ImageType* não é [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) ou **vmFloppyDiskImage \_ Highdensity** (2).</span><span class="sxs-lookup"><span data-stu-id="6e3b9-128">The *imageType* parameter is not [**vmFloppyDiskImage\_LowDensity**](vmfloppydiskimagetype.md) (1) or **vmFloppyDiskImage\_HighDensity** (2).</span></span><br/> |
| <dl> <span data-ttu-id="6e3b9-129"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="6e3b9-130">O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="6e3b9-130">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="6e3b9-131"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="6e3b9-132">O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="6e3b9-132">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                           |
| <dl> <span data-ttu-id="6e3b9-133"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="6e3b9-134">O parâmetro *imagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-134">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6e3b9-135">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-135">An absolute path is required.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="6e3b9-136"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="6e3b9-137">O caminho especificado pelo parâmetro *imagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-137">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="6e3b9-138">O comprimento do caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-138">The length of the path must be less than 260 characters.</span></span><br/>                          |
| <dl> <span data-ttu-id="6e3b9-139"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="6e3b9-140">O arquivo referenciado pelo parâmetro *imagePath* já existe.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-140">The file referenced by the parameter *imagePath* already exists.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="6e3b9-141"><dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="6e3b9-142">Não há espaço suficiente no volume do host para criar a imagem de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-142">There is insufficient space on the host volume to create the virtual floppy disk image.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6e3b9-143"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6e3b9-143"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="6e3b9-144">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-144">An unexpected error occurred.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="6e3b9-145"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-145"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="6e3b9-146">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="6e3b9-146">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                           |



 

## <a name="requirements"></a><span data-ttu-id="6e3b9-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e3b9-147">Requirements</span></span>



| <span data-ttu-id="6e3b9-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e3b9-148">Requirement</span></span> | <span data-ttu-id="6e3b9-149">Valor</span><span class="sxs-lookup"><span data-stu-id="6e3b9-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3b9-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e3b9-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3b9-151">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6e3b9-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e3b9-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e3b9-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3b9-153">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6e3b9-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6e3b9-154">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6e3b9-154">End of client support</span></span><br/>    | <span data-ttu-id="6e3b9-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e3b9-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6e3b9-156">Produto</span><span class="sxs-lookup"><span data-stu-id="6e3b9-156">Product</span></span><br/>                  | <span data-ttu-id="6e3b9-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6e3b9-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6e3b9-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e3b9-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e3b9-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e3b9-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6e3b9-160">IID</span><span class="sxs-lookup"><span data-stu-id="6e3b9-160">IID</span></span><br/>                      | <span data-ttu-id="6e3b9-161">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="6e3b9-161">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6e3b9-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e3b9-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3b9-163">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="6e3b9-163">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

