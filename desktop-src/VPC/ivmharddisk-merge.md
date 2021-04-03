---
title: Método de mesclagem IVMHardDisk (VPCCOMInterfaces. h)
description: Mescla um disco rígido virtual diferencial com sua imagem de disco pai.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Método de mesclagem Virtual PC
- Método de mesclagem Virtual PC, interface IVMHardDisk
- Virtual PC de interface IVMHardDisk, método Merge
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918643"
---
# <a name="ivmharddiskmerge-method"></a><span data-ttu-id="656f3-106">Método IVMHardDisk:: Merge</span><span class="sxs-lookup"><span data-stu-id="656f3-106">IVMHardDisk::Merge method</span></span>

<span data-ttu-id="656f3-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="656f3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="656f3-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="656f3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="656f3-109">Mescla um disco rígido virtual diferencial com sua imagem de disco pai.</span><span class="sxs-lookup"><span data-stu-id="656f3-109">Merges a differencing virtual hard disk with its parent disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="656f3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="656f3-110">Syntax</span></span>


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="656f3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="656f3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656f3-112">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="656f3-112">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="656f3-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="656f3-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656f3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="656f3-114">Return value</span></span>

<span data-ttu-id="656f3-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="656f3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="656f3-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="656f3-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="656f3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="656f3-117">Description</span></span>                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="656f3-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="656f3-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="656f3-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="656f3-119">The operation was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="656f3-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="656f3-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="656f3-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="656f3-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="656f3-122"><dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="656f3-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="656f3-123">A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) está em uso ou o pai desta imagem de disco rígido virtual está em uso.</span><span class="sxs-lookup"><span data-stu-id="656f3-123">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use or the parent of this virtual hard disk image is in use.</span></span> <span data-ttu-id="656f3-124">Ou, essas imagens de disco rígido podem fazer parte de um estado salvo.</span><span class="sxs-lookup"><span data-stu-id="656f3-124">Or, these hard disk images could be part of a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="656f3-125"><dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="656f3-125"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="656f3-126">A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) deve ser uma imagem de disco diferencial.</span><span class="sxs-lookup"><span data-stu-id="656f3-126">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a differencing disk image.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="656f3-127"><dt>**VM \_ E \_ File \_ \_ somente leitura**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="656f3-127"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="656f3-128">O pai da imagem do disco rígido virtual referenciado por este objeto [**IVMHardDisk**](ivmharddisk.md) está marcado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="656f3-128">The parent of virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="656f3-129"><dt>**VM \_ E \_ \_ caminho pai \_ não \_ encontrado**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="656f3-129"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="656f3-130">O pai do disco rígido virtual referenciado por este objeto [**IVMHardDisk**](ivmharddisk.md) não existe.</span><span class="sxs-lookup"><span data-stu-id="656f3-130">The parent of the virtual hard disk referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not exist.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="656f3-131"><dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="656f3-131"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="656f3-132">A imagem do disco rígido virtual não pode ser mesclada porque o aplicativo está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="656f3-132">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="656f3-133"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="656f3-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="656f3-134">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="656f3-134">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="656f3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="656f3-135">Requirements</span></span>



| <span data-ttu-id="656f3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="656f3-136">Requirement</span></span> | <span data-ttu-id="656f3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="656f3-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="656f3-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="656f3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="656f3-139">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="656f3-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="656f3-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="656f3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="656f3-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="656f3-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="656f3-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="656f3-142">End of client support</span></span><br/>    | <span data-ttu-id="656f3-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="656f3-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="656f3-144">Produto</span><span class="sxs-lookup"><span data-stu-id="656f3-144">Product</span></span><br/>                  | <span data-ttu-id="656f3-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="656f3-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="656f3-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="656f3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="656f3-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="656f3-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="656f3-148">IID</span><span class="sxs-lookup"><span data-stu-id="656f3-148">IID</span></span><br/>                      | <span data-ttu-id="656f3-149">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="656f3-149">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="656f3-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="656f3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656f3-151">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="656f3-151">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

