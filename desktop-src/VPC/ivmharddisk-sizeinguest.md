---
title: Propriedade IVMHardDisk SizeInGuest (VPCCOMInterfaces. h)
description: Recupera o tamanho do disco rígido virtual no sistema operacional convidado.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Propriedade SizeInGuest Virtual PC
- Propriedade SizeInGuest Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade SizeInGuest
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085968"
---
# <a name="ivmharddisksizeinguest-property"></a><span data-ttu-id="77eee-106">Propriedade IVMHardDisk:: SizeInGuest</span><span class="sxs-lookup"><span data-stu-id="77eee-106">IVMHardDisk::SizeInGuest property</span></span>

<span data-ttu-id="77eee-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77eee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="77eee-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="77eee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="77eee-109">Recupera o tamanho do disco rígido virtual no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="77eee-109">Retrieves the size of the virtual hard disk in the guest operating system.</span></span>

<span data-ttu-id="77eee-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="77eee-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="77eee-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77eee-111">Syntax</span></span>


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="77eee-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="77eee-112">Property value</span></span>

<span data-ttu-id="77eee-113">O tamanho, em bytes, da imagem do disco rígido.</span><span class="sxs-lookup"><span data-stu-id="77eee-113">The size, in bytes, of the hard disk image.</span></span> <span data-ttu-id="77eee-114">Esse valor é uma **variante** do tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="77eee-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77eee-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="77eee-115">Error codes</span></span>



| <span data-ttu-id="77eee-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="77eee-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="77eee-117">Significado</span><span class="sxs-lookup"><span data-stu-id="77eee-117">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77eee-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77eee-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="77eee-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="77eee-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="77eee-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="77eee-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="77eee-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="77eee-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="77eee-122"><dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="77eee-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="77eee-123">Não foi possível encontrar o arquivo de disco rígido virtual atual.</span><span class="sxs-lookup"><span data-stu-id="77eee-123">The current virtual hard disk file could not be found.</span></span><br/>                         |
| <dl> <span data-ttu-id="77eee-124"><dt>VM \_ 0xA004067C \_ de \_ \_ \_ falha de abertura de imagem de HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77eee-124"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="77eee-125">Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="77eee-125">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="77eee-126"><dt>VM \_ E & 0xA0040681 de \_ \_ \_ acesso de imagem de HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77eee-126"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="77eee-127">Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="77eee-127">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="77eee-128"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="77eee-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="77eee-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="77eee-129">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="77eee-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77eee-130">Requirements</span></span>



| <span data-ttu-id="77eee-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="77eee-131">Requirement</span></span> | <span data-ttu-id="77eee-132">Valor</span><span class="sxs-lookup"><span data-stu-id="77eee-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="77eee-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77eee-133">Minimum supported client</span></span><br/> | <span data-ttu-id="77eee-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="77eee-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77eee-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77eee-135">Minimum supported server</span></span><br/> | <span data-ttu-id="77eee-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="77eee-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="77eee-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="77eee-137">End of client support</span></span><br/>    | <span data-ttu-id="77eee-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="77eee-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="77eee-139">Produto</span><span class="sxs-lookup"><span data-stu-id="77eee-139">Product</span></span><br/>                  | <span data-ttu-id="77eee-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="77eee-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="77eee-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77eee-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="77eee-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="77eee-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="77eee-143">IID</span><span class="sxs-lookup"><span data-stu-id="77eee-143">IID</span></span><br/>                      | <span data-ttu-id="77eee-144">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="77eee-144">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="77eee-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="77eee-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77eee-146">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="77eee-146">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

