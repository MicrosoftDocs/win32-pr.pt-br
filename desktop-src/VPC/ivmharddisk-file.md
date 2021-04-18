---
title: Propriedade de arquivo IVMHardDisk (VPCCOMInterfaces. h)
description: Recupera o nome do caminho completo do arquivo de disco rígido virtual.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Propriedade de arquivo Virtual PC
- Propriedade de arquivo Virtual PC, interface IVMHardDisk
- Virtual PC interface IVMHardDisk, Propriedade File
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764013"
---
# <a name="ivmharddiskfile-property"></a><span data-ttu-id="61666-106">Propriedade IVMHardDisk:: File</span><span class="sxs-lookup"><span data-stu-id="61666-106">IVMHardDisk::File property</span></span>

<span data-ttu-id="61666-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="61666-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="61666-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="61666-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="61666-109">Recupera o nome do caminho completo do arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="61666-109">Retrieves the full path name of the virtual hard disk file.</span></span>

<span data-ttu-id="61666-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="61666-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61666-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61666-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a><span data-ttu-id="61666-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="61666-112">Property value</span></span>

<span data-ttu-id="61666-113">O nome do caminho completo do arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="61666-113">The full path name of the current hard disk image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="61666-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="61666-114">Error codes</span></span>



| <span data-ttu-id="61666-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="61666-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="61666-116">Significado</span><span class="sxs-lookup"><span data-stu-id="61666-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="61666-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61666-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="61666-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="61666-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="61666-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="61666-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="61666-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="61666-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="61666-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="61666-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="61666-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="61666-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="61666-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61666-123">Requirements</span></span>



| <span data-ttu-id="61666-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="61666-124">Requirement</span></span> | <span data-ttu-id="61666-125">Valor</span><span class="sxs-lookup"><span data-stu-id="61666-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61666-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61666-126">Minimum supported client</span></span><br/> | <span data-ttu-id="61666-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="61666-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61666-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61666-128">Minimum supported server</span></span><br/> | <span data-ttu-id="61666-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61666-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="61666-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="61666-130">End of client support</span></span><br/>    | <span data-ttu-id="61666-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61666-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="61666-132">Produto</span><span class="sxs-lookup"><span data-stu-id="61666-132">Product</span></span><br/>                  | <span data-ttu-id="61666-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="61666-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="61666-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61666-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="61666-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="61666-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="61666-136">IID</span><span class="sxs-lookup"><span data-stu-id="61666-136">IID</span></span><br/>                      | <span data-ttu-id="61666-137">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="61666-137">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="61666-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="61666-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61666-139">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="61666-139">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

