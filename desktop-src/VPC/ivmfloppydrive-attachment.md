---
title: Propriedade de anexo IVMFloppyDrive (VPCCOMInterfaces. h)
description: Recupera o tipo de mídia anexada à unidade de disquete na máquina virtual.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Propriedade do anexo Virtual PC
- Propriedade de anexo Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, Propriedade Attachment
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790456"
---
# <a name="ivmfloppydriveattachment-property"></a><span data-ttu-id="3663c-106">Propriedade IVMFloppyDrive:: Attachment</span><span class="sxs-lookup"><span data-stu-id="3663c-106">IVMFloppyDrive::Attachment property</span></span>

<span data-ttu-id="3663c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3663c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3663c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3663c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3663c-109">Recupera o tipo de mídia anexada à unidade de disquete na VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="3663c-109">Retrieves the type of media attached to the floppy drive in the virtual machine (VM).</span></span>

<span data-ttu-id="3663c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3663c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3663c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3663c-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="3663c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3663c-112">Property value</span></span>

<span data-ttu-id="3663c-113">O tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3663c-113">The type of media.</span></span> <span data-ttu-id="3663c-114">Para obter uma lista de valores, consulte [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="3663c-114">For a list of values, see [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="3663c-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3663c-115">Error codes</span></span>



| <span data-ttu-id="3663c-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3663c-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3663c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3663c-117">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3663c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3663c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3663c-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3663c-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="3663c-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3663c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3663c-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3663c-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="3663c-122"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3663c-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3663c-123">A configuração desta VM não é válida ou não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3663c-123">The configuration for this VM is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="3663c-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3663c-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3663c-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3663c-125">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="3663c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3663c-126">Requirements</span></span>



| <span data-ttu-id="3663c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3663c-127">Requirement</span></span> | <span data-ttu-id="3663c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3663c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3663c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3663c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3663c-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3663c-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3663c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3663c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3663c-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3663c-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3663c-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3663c-133">End of client support</span></span><br/>    | <span data-ttu-id="3663c-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3663c-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3663c-135">Produto</span><span class="sxs-lookup"><span data-stu-id="3663c-135">Product</span></span><br/>                  | <span data-ttu-id="3663c-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3663c-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3663c-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3663c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3663c-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3663c-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3663c-139">IID</span><span class="sxs-lookup"><span data-stu-id="3663c-139">IID</span></span><br/>                      | <span data-ttu-id="3663c-140">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="3663c-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3663c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3663c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3663c-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="3663c-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

