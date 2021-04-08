---
title: Propriedade IVMHardDisk HostFreeDiskSpace (VPCCOMInterfaces. h)
description: Recupera a quantidade de espaço em disco restante disponível no host para o disco rígido virtual.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Propriedade HostFreeDiskSpace Virtual PC
- Propriedade HostFreeDiskSpace Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086266"
---
# <a name="ivmharddiskhostfreediskspace-property"></a><span data-ttu-id="3dc0a-106">Propriedade IVMHardDisk:: HostFreeDiskSpace</span><span class="sxs-lookup"><span data-stu-id="3dc0a-106">IVMHardDisk::HostFreeDiskSpace property</span></span>

<span data-ttu-id="3dc0a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3dc0a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3dc0a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3dc0a-109">Recupera a quantidade de espaço em disco restante disponível no host para o disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-109">Retrieves the amount of remaining disk space available on the host for the virtual hard disk.</span></span>

<span data-ttu-id="3dc0a-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc0a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dc0a-111">Syntax</span></span>


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a><span data-ttu-id="3dc0a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3dc0a-112">Property value</span></span>

<span data-ttu-id="3dc0a-113">A quantidade de espaço em disco restante disponível no computador host para o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-113">The amount of remaining disk space available on the host computer for the current hard disk image file.</span></span> <span data-ttu-id="3dc0a-114">Esse valor é uma **variante** do tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3dc0a-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3dc0a-115">Error codes</span></span>



| <span data-ttu-id="3dc0a-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3dc0a-116">Name/value</span></span>                                                                                                                                                                            | <span data-ttu-id="3dc0a-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3dc0a-117">Meaning</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3dc0a-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3dc0a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                               | <span data-ttu-id="3dc0a-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-119">The operation was successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="3dc0a-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3dc0a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                 | <span data-ttu-id="3dc0a-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-121">The parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3dc0a-122"><dt>HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3dc0a-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl> | <span data-ttu-id="3dc0a-123">O caminho para o arquivo de disco rígido virtual atual não é válido.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-123">The path to the current virtual hard disk file is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="3dc0a-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3dc0a-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                         | <span data-ttu-id="3dc0a-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-125">An unexpected error has occurred.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="3dc0a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dc0a-126">Requirements</span></span>



| <span data-ttu-id="3dc0a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dc0a-127">Requirement</span></span> | <span data-ttu-id="3dc0a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3dc0a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc0a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dc0a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc0a-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3dc0a-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3dc0a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dc0a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc0a-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3dc0a-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3dc0a-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3dc0a-133">End of client support</span></span><br/>    | <span data-ttu-id="3dc0a-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3dc0a-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3dc0a-135">Produto</span><span class="sxs-lookup"><span data-stu-id="3dc0a-135">Product</span></span><br/>                  | <span data-ttu-id="3dc0a-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3dc0a-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3dc0a-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dc0a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dc0a-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dc0a-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3dc0a-139">IID</span><span class="sxs-lookup"><span data-stu-id="3dc0a-139">IID</span></span><br/>                      | <span data-ttu-id="3dc0a-140">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="3dc0a-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3dc0a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dc0a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc0a-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="3dc0a-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

