---
title: Propriedade IVMGuestOS ComputerName (VPCCOMInterfaces. h)
description: O nome do computador do sistema operacional convidado em execução na máquina virtual.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- Propriedade ComputerName PC virtual
- Propriedade ComputerName Virtual PC, interface IVMGuestOS
- Virtual PC interface IVMGuestOS, Propriedade ComputerName
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b266c238809284b340095dd25390d6e5f3d2b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455909"
---
# <a name="ivmguestoscomputername-property"></a><span data-ttu-id="05c66-106">Propriedade IVMGuestOS:: ComputerName</span><span class="sxs-lookup"><span data-stu-id="05c66-106">IVMGuestOS::ComputerName property</span></span>

<span data-ttu-id="05c66-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05c66-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05c66-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05c66-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05c66-109">Recupera o nome do computador do sistema operacional convidado em execução na VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="05c66-109">Retrieves the computer name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="05c66-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="05c66-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c66-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05c66-111">Syntax</span></span>


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a><span data-ttu-id="05c66-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="05c66-112">Property value</span></span>

<span data-ttu-id="05c66-113">O nome do computador do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="05c66-113">The computer name of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05c66-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="05c66-114">Error codes</span></span>



| <span data-ttu-id="05c66-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="05c66-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="05c66-116">Significado</span><span class="sxs-lookup"><span data-stu-id="05c66-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="05c66-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05c66-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="05c66-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="05c66-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="05c66-119"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="05c66-119"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="05c66-120">O parâmetro não é válido ou não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="05c66-120">The parameter is not valid or not specified.</span></span><br/>         |
| <dl> <span data-ttu-id="05c66-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="05c66-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="05c66-122">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="05c66-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="05c66-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="05c66-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="05c66-124">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="05c66-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="05c66-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="05c66-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="05c66-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="05c66-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="05c66-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c66-127">Requirements</span></span>



| <span data-ttu-id="05c66-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c66-128">Requirement</span></span> | <span data-ttu-id="05c66-129">Valor</span><span class="sxs-lookup"><span data-stu-id="05c66-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c66-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c66-130">Minimum supported client</span></span><br/> | <span data-ttu-id="05c66-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="05c66-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05c66-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c66-132">Minimum supported server</span></span><br/> | <span data-ttu-id="05c66-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="05c66-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="05c66-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="05c66-134">End of client support</span></span><br/>    | <span data-ttu-id="05c66-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05c66-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="05c66-136">Produto</span><span class="sxs-lookup"><span data-stu-id="05c66-136">Product</span></span><br/>                  | <span data-ttu-id="05c66-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05c66-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="05c66-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05c66-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c66-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c66-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="05c66-140">IID</span><span class="sxs-lookup"><span data-stu-id="05c66-140">IID</span></span><br/>                      | <span data-ttu-id="05c66-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="05c66-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="05c66-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="05c66-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c66-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="05c66-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

