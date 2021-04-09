---
title: Propriedade do tipo IVMHardDisk (VPCCOMInterfaces. h)
description: Tipo de disco rígido virtual.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Propriedade de tipo Virtual PC
- Propriedade de tipo Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade Type
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009326"
---
# <a name="ivmharddisktype-property"></a><span data-ttu-id="1573f-106">Propriedade IVMHardDisk:: Type</span><span class="sxs-lookup"><span data-stu-id="1573f-106">IVMHardDisk::Type property</span></span>

<span data-ttu-id="1573f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1573f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1573f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1573f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1573f-109">Recupera o tipo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="1573f-109">Retrieves the type of the virtual hard disk.</span></span>

<span data-ttu-id="1573f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1573f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1573f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1573f-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a><span data-ttu-id="1573f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1573f-112">Property value</span></span>

<span data-ttu-id="1573f-113">O tipo da imagem do disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="1573f-113">The type of the current hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1573f-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1573f-114">Error codes</span></span>



| <span data-ttu-id="1573f-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="1573f-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="1573f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1573f-116">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1573f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1573f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="1573f-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1573f-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="1573f-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="1573f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="1573f-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1573f-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="1573f-121"><dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="1573f-121"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="1573f-122">Não foi possível encontrar o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="1573f-122">The current hard disk image file could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="1573f-123"><dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1573f-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="1573f-124">O tipo da imagem do disco rígido atual é inválido.</span><span class="sxs-lookup"><span data-stu-id="1573f-124">The type of the current hard disk image is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="1573f-125"><dt>VM \_ 0xA004067C \_ de \_ \_ \_ falha de abertura de imagem de HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1573f-125"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="1573f-126">Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="1573f-126">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="1573f-127"><dt>VM \_ E & 0xA0040681 de \_ \_ \_ acesso de imagem de HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1573f-127"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="1573f-128">Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="1573f-128">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="1573f-129"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="1573f-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="1573f-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1573f-130">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="1573f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1573f-131">Requirements</span></span>



| <span data-ttu-id="1573f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1573f-132">Requirement</span></span> | <span data-ttu-id="1573f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1573f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1573f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1573f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1573f-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1573f-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1573f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1573f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1573f-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1573f-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1573f-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1573f-138">End of client support</span></span><br/>    | <span data-ttu-id="1573f-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1573f-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1573f-140">Produto</span><span class="sxs-lookup"><span data-stu-id="1573f-140">Product</span></span><br/>                  | <span data-ttu-id="1573f-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1573f-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1573f-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1573f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1573f-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1573f-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1573f-144">IID</span><span class="sxs-lookup"><span data-stu-id="1573f-144">IID</span></span><br/>                      | <span data-ttu-id="1573f-145">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="1573f-145">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1573f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1573f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1573f-147">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="1573f-147">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

