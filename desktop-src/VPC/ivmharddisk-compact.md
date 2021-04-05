---
title: Método IVMHardDisk Compact (VPCCOMInterfaces. h)
description: Compacta uma imagem de disco rígido virtual de expansão dinâmica.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- PC virtual do método compacto
- Método compacto Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, método compacto
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645086"
---
# <a name="ivmharddiskcompact-method"></a><span data-ttu-id="0d628-106">Método IVMHardDisk:: Compact</span><span class="sxs-lookup"><span data-stu-id="0d628-106">IVMHardDisk::Compact method</span></span>

<span data-ttu-id="0d628-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d628-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0d628-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0d628-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0d628-109">Compacta uma imagem de disco rígido virtual de expansão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0d628-109">Compacts a dynamically expanding virtual hard disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d628-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d628-110">Syntax</span></span>


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a><span data-ttu-id="0d628-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d628-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d628-112">*compactTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0d628-112">*compactTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0d628-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de compactação.</span><span class="sxs-lookup"><span data-stu-id="0d628-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion the compaction process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d628-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d628-114">Return value</span></span>

<span data-ttu-id="0d628-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0d628-115">This method can return one of these values.</span></span>



| <span data-ttu-id="0d628-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0d628-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="0d628-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d628-117">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d628-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="0d628-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0d628-119">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="0d628-120"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="0d628-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="0d628-121">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="0d628-121">An unexpected error has occurred.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="0d628-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="0d628-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="0d628-123">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0d628-123">The parameter is **NULL**.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="0d628-124"><dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="0d628-125">A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) está em uso.</span><span class="sxs-lookup"><span data-stu-id="0d628-125">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use.</span></span><br/>                                  |
| <dl> <span data-ttu-id="0d628-126"><dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="0d628-127">O volume do host não tem espaço suficiente para criar um arquivo temporário necessário para a compactação desta imagem de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="0d628-127">The host volume does not have enough space to create a temporary file needed for the compaction of this virtual hard disk image.</span></span><br/>     |
| <dl> <span data-ttu-id="0d628-128"><dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-128"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="0d628-129">A imagem do disco rígido virtual não pode ser compactada porque o aplicativo está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="0d628-129">The virtual hard disk image cannot be compacted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0d628-130"><dt>**VM \_ E \_ File \_ \_ somente leitura**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-130"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="0d628-131">A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) está marcada como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0d628-131">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                     |
| <dl> <span data-ttu-id="0d628-132"><dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-132"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="0d628-133">A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) deve ser um tipo de imagem **vmDiskTypeDynamic** .</span><span class="sxs-lookup"><span data-stu-id="0d628-133">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a **vmDiskTypeDynamic** image type.</span></span><br/> |
| <dl> <span data-ttu-id="0d628-134"><dt>**VM \_ E \_ \_ \_ arquivo HD inválido**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-134"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="0d628-135">A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) não parece ser uma imagem válida.</span><span class="sxs-lookup"><span data-stu-id="0d628-135">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="0d628-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d628-136">Remarks</span></span>

<span data-ttu-id="0d628-137">Para compactar uma imagem de disco rígido de expansão dinâmica, o espaço livre na imagem de disco deve ser zerado primeiro.</span><span class="sxs-lookup"><span data-stu-id="0d628-137">To compact a dynamically expanding hard disk image, free space on the disk image should first be zeroed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d628-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d628-138">Requirements</span></span>



| <span data-ttu-id="0d628-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d628-139">Requirement</span></span> | <span data-ttu-id="0d628-140">Valor</span><span class="sxs-lookup"><span data-stu-id="0d628-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d628-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d628-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0d628-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d628-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d628-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d628-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0d628-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0d628-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0d628-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0d628-145">End of client support</span></span><br/>    | <span data-ttu-id="0d628-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d628-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0d628-147">Produto</span><span class="sxs-lookup"><span data-stu-id="0d628-147">Product</span></span><br/>                  | <span data-ttu-id="0d628-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0d628-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0d628-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d628-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d628-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d628-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0d628-151">IID</span><span class="sxs-lookup"><span data-stu-id="0d628-151">IID</span></span><br/>                      | <span data-ttu-id="0d628-152">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="0d628-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0d628-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d628-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d628-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="0d628-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

