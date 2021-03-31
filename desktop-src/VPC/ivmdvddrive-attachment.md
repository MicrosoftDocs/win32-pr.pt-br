---
title: Propriedade de anexo IVMDVDDrive (VPCCOMInterfaces. h)
description: Recupera o tipo de mídia anexada à unidade de DVD na máquina virtual.
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- Propriedade do anexo Virtual PC
- Propriedade de anexo Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, Propriedade Attachment
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5c7801e11534249da899797b73b632a7eda307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824598"
---
# <a name="ivmdvddriveattachment-property"></a><span data-ttu-id="6d7c3-106">Propriedade IVMDVDDrive:: Attachment</span><span class="sxs-lookup"><span data-stu-id="6d7c3-106">IVMDVDDrive::Attachment property</span></span>

<span data-ttu-id="6d7c3-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d7c3-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d7c3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d7c3-109">Recupera o tipo de mídia anexada à unidade de DVD na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-109">Retrieves the type of media attached to the DVD drive within the virtual machine.</span></span>

<span data-ttu-id="6d7c3-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7c3-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d7c3-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="6d7c3-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d7c3-112">Property value</span></span>

<span data-ttu-id="6d7c3-113">O tipo de mídia anexado.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-113">The attached media type.</span></span> <span data-ttu-id="6d7c3-114">Para obter uma lista de valores, consulte [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="6d7c3-114">For a list of values, see [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d7c3-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6d7c3-115">Error codes</span></span>



| <span data-ttu-id="6d7c3-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="6d7c3-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="6d7c3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="6d7c3-117">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="6d7c3-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d7c3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="6d7c3-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-119">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="6d7c3-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6d7c3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="6d7c3-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-121">The parameter is **NULL**.</span></span><br/>                  |
| <dl> <span data-ttu-id="6d7c3-122"><dt>E \_ FALHA</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="6d7c3-122"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="6d7c3-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-123">An unexpected error has occurred.</span></span><br/>           |
| <dl> <span data-ttu-id="6d7c3-124"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d7c3-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="6d7c3-125">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-125">The virtual machine could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="6d7c3-126"><dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d7c3-126"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="6d7c3-127">O local do barramento desta unidade é inválido.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-127">The bus location for this drive is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="6d7c3-128"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6d7c3-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="6d7c3-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6d7c3-129">An unexpected error has occurred.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="6d7c3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d7c3-130">Requirements</span></span>



| <span data-ttu-id="6d7c3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d7c3-131">Requirement</span></span> | <span data-ttu-id="6d7c3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="6d7c3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7c3-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d7c3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6d7c3-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6d7c3-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d7c3-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d7c3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6d7c3-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6d7c3-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d7c3-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6d7c3-137">End of client support</span></span><br/>    | <span data-ttu-id="6d7c3-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d7c3-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d7c3-139">Produto</span><span class="sxs-lookup"><span data-stu-id="6d7c3-139">Product</span></span><br/>                  | <span data-ttu-id="6d7c3-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d7c3-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d7c3-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d7c3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d7c3-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d7c3-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d7c3-143">IID</span><span class="sxs-lookup"><span data-stu-id="6d7c3-143">IID</span></span><br/>                      | <span data-ttu-id="6d7c3-144">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="6d7c3-144">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6d7c3-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6d7c3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7c3-146">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="6d7c3-146">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

