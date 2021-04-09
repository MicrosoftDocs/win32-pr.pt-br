---
title: Propriedade IVMHardDisk SizeOnHost (VPCCOMInterfaces. h)
description: Tamanho do arquivo de disco rígido virtual no computador host.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Propriedade SizeOnHost Virtual PC
- Propriedade SizeOnHost Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009579"
---
# <a name="ivmharddisksizeonhost-property"></a><span data-ttu-id="42505-106">Propriedade IVMHardDisk:: SizeOnHost</span><span class="sxs-lookup"><span data-stu-id="42505-106">IVMHardDisk::SizeOnHost property</span></span>

<span data-ttu-id="42505-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="42505-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="42505-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="42505-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="42505-109">Recupera o tamanho do arquivo de disco rígido virtual no computador host.</span><span class="sxs-lookup"><span data-stu-id="42505-109">Retrieves the size of the virtual hard disk file on the host computer.</span></span>

<span data-ttu-id="42505-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="42505-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="42505-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42505-111">Syntax</span></span>


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="42505-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="42505-112">Property value</span></span>

<span data-ttu-id="42505-113">O tamanho, em bytes, do arquivo de imagem de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="42505-113">The size, in bytes, of the hard disk image file.</span></span> <span data-ttu-id="42505-114">Esse valor é uma **variante** do tipo **VT \_ decimal**.</span><span class="sxs-lookup"><span data-stu-id="42505-114">This value is a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42505-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="42505-115">Error codes</span></span>



| <span data-ttu-id="42505-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="42505-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="42505-117">Significado</span><span class="sxs-lookup"><span data-stu-id="42505-117">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="42505-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42505-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="42505-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="42505-119">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="42505-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="42505-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="42505-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="42505-121">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="42505-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="42505-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="42505-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="42505-123">An unexpected error has occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="42505-124"><dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="42505-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="42505-125">O arquivo de imagem do disco rígido não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="42505-125">The hard disk image file was not found.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="42505-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42505-126">Requirements</span></span>



| <span data-ttu-id="42505-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="42505-127">Requirement</span></span> | <span data-ttu-id="42505-128">Valor</span><span class="sxs-lookup"><span data-stu-id="42505-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42505-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42505-129">Minimum supported client</span></span><br/> | <span data-ttu-id="42505-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="42505-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42505-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42505-131">Minimum supported server</span></span><br/> | <span data-ttu-id="42505-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="42505-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="42505-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="42505-133">End of client support</span></span><br/>    | <span data-ttu-id="42505-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42505-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="42505-135">Produto</span><span class="sxs-lookup"><span data-stu-id="42505-135">Product</span></span><br/>                  | <span data-ttu-id="42505-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="42505-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="42505-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42505-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="42505-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="42505-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="42505-139">IID</span><span class="sxs-lookup"><span data-stu-id="42505-139">IID</span></span><br/>                      | <span data-ttu-id="42505-140">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="42505-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="42505-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="42505-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42505-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="42505-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

