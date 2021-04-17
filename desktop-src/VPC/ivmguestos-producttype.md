---
title: Propriedade ProductType IVMGuestOS (VPCCOMInterfaces. h)
description: Recupera o tipo de produto do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Propriedade ProductType Virtual PC
- Propriedade ProductType Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, propriedade ProductType
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759587"
---
# <a name="ivmguestosproducttype-property"></a><span data-ttu-id="b877f-106">IVMGuestOS: Propriedade roductType de:P</span><span class="sxs-lookup"><span data-stu-id="b877f-106">IVMGuestOS::ProductType property</span></span>

<span data-ttu-id="b877f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b877f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b877f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b877f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b877f-109">Recupera o tipo de produto do sistema operacional convidado em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b877f-109">Retrieves the product type of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="b877f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b877f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b877f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b877f-111">Syntax</span></span>


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a><span data-ttu-id="b877f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b877f-112">Property value</span></span>

<span data-ttu-id="b877f-113">O tipo de produto.</span><span class="sxs-lookup"><span data-stu-id="b877f-113">The product type.</span></span> <span data-ttu-id="b877f-114">Há suporte para os valores de cadeia de caracteres a seguir.</span><span class="sxs-lookup"><span data-stu-id="b877f-114">The following string values are supported.</span></span>



| <span data-ttu-id="b877f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b877f-115">Value</span></span>                                                                                  | <span data-ttu-id="b877f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b877f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b877f-117"><dt>"0x0000002"</dt></span><span class="sxs-lookup"><span data-stu-id="b877f-117"><dt>"0x0000002"</dt></span></span> </dl> | <span data-ttu-id="b877f-118">O sistema é um controlador de domínio e o sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b877f-118">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="b877f-119"><dt>"0x0000003"</dt></span><span class="sxs-lookup"><span data-stu-id="b877f-119"><dt>"0x0000003"</dt></span></span> </dl> | <span data-ttu-id="b877f-120">O sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b877f-120">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="b877f-121">Observe que um servidor que também é um controlador de domínio é relatado **como \_ \_ \_ controlador de domínio do NT**, não ver o **\_ \_ servidor NT**.</span><span class="sxs-lookup"><span data-stu-id="b877f-121">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <dl> <span data-ttu-id="b877f-122"><dt>"0x0000001"</dt></span><span class="sxs-lookup"><span data-stu-id="b877f-122"><dt>"0x0000001"</dt></span></span> </dl> | <span data-ttu-id="b877f-123">O sistema operacional é o Windows 7, o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b877f-123">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="b877f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b877f-124">Requirements</span></span>



| <span data-ttu-id="b877f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b877f-125">Requirement</span></span> | <span data-ttu-id="b877f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b877f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b877f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b877f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b877f-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b877f-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b877f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b877f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b877f-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b877f-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b877f-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b877f-131">End of client support</span></span><br/>    | <span data-ttu-id="b877f-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b877f-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b877f-133">Produto</span><span class="sxs-lookup"><span data-stu-id="b877f-133">Product</span></span><br/>                  | <span data-ttu-id="b877f-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b877f-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b877f-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b877f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b877f-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b877f-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b877f-137">IID</span><span class="sxs-lookup"><span data-stu-id="b877f-137">IID</span></span><br/>                      | <span data-ttu-id="b877f-138">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="b877f-138">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b877f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b877f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b877f-140">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="b877f-140">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

