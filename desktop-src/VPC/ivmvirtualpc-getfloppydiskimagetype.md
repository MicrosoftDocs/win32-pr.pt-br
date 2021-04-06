---
title: Método IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces. h)
description: Recupera o tipo de um arquivo de imagem de disquete existente.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- GetFloppyDiskImageType do método virtual PC
- Método GetFloppyDiskImageType Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método GetFloppyDiskImageType
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086343"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a><span data-ttu-id="0017a-106">Método IVMVirtualPC:: GetFloppyDiskImageType</span><span class="sxs-lookup"><span data-stu-id="0017a-106">IVMVirtualPC::GetFloppyDiskImageType method</span></span>

<span data-ttu-id="0017a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0017a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0017a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0017a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0017a-109">Recupera o tipo de um arquivo de imagem de disquete existente.</span><span class="sxs-lookup"><span data-stu-id="0017a-109">Retrieves the type of an existing floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0017a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0017a-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a><span data-ttu-id="0017a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0017a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0017a-112">*imagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0017a-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0017a-113">O caminho completo para o arquivo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="0017a-113">The full path to the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="0017a-114">*ImageType* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0017a-114">*imageType* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0017a-115">O tipo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="0017a-115">The disk image type.</span></span> <span data-ttu-id="0017a-116">Para obter uma lista de valores, consulte [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="0017a-116">For a list of values, see [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0017a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0017a-117">Return value</span></span>

<span data-ttu-id="0017a-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0017a-118">This method can return one of these values.</span></span>



| <span data-ttu-id="0017a-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0017a-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="0017a-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0017a-120">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0017a-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0017a-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="0017a-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0017a-122">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="0017a-123"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="0017a-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="0017a-124">O parâmetro *imagePath* ou *ImageType* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0017a-124">The *imagePath* or *imageType* parameter is **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="0017a-125"><dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="0017a-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="0017a-126">O sistema não pode localizar o arquivo especificado pelo parâmetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="0017a-126">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0017a-127"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="0017a-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="0017a-128">O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="0017a-128">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0017a-129"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="0017a-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="0017a-130">O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="0017a-130">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="0017a-131"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="0017a-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="0017a-132">O parâmetro *imagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="0017a-132">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="0017a-133">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="0017a-133">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="0017a-134"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="0017a-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="0017a-135">O caminho especificado pelo parâmetro *imagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="0017a-135">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="0017a-136">O comprimento do caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0017a-136">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="0017a-137"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="0017a-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="0017a-138">O arquivo especificado por *imagePath* não é uma imagem de disquete ou ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="0017a-138">The file specified by *imagePath* is not a floppy image, or an unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="0017a-139"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0017a-139"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="0017a-140">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="0017a-140">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="0017a-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0017a-141">Requirements</span></span>



| <span data-ttu-id="0017a-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0017a-142">Requirement</span></span> | <span data-ttu-id="0017a-143">Valor</span><span class="sxs-lookup"><span data-stu-id="0017a-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0017a-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0017a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0017a-145">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0017a-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0017a-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0017a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0017a-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0017a-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0017a-148">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0017a-148">End of client support</span></span><br/>    | <span data-ttu-id="0017a-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0017a-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0017a-150">Produto</span><span class="sxs-lookup"><span data-stu-id="0017a-150">Product</span></span><br/>                  | <span data-ttu-id="0017a-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0017a-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0017a-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0017a-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="0017a-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0017a-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0017a-154">IID</span><span class="sxs-lookup"><span data-stu-id="0017a-154">IID</span></span><br/>                      | <span data-ttu-id="0017a-155">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="0017a-155">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0017a-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="0017a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0017a-157">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="0017a-157">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

