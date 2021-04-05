---
title: Propriedade IVMKeyboard HasExclusiveAccess (VPCCOMInterfaces. h)
description: Indica se este objeto tem controle exclusivo sobre o dispositivo de teclado da VM.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Propriedade HasExclusiveAccess Virtual PC
- Propriedade HasExclusiveAccess Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, Propriedade HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086222"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a><span data-ttu-id="a53c6-106">Propriedade IVMKeyboard:: HasExclusiveAccess</span><span class="sxs-lookup"><span data-stu-id="a53c6-106">IVMKeyboard::HasExclusiveAccess property</span></span>

<span data-ttu-id="a53c6-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a53c6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a53c6-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a53c6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a53c6-109">Indica se este objeto tem controle exclusivo sobre o dispositivo de teclado da máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="a53c6-109">Indicates whether this object has exclusive control over the virtual machine's (VM) keyboard device.</span></span>

<span data-ttu-id="a53c6-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a53c6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53c6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a53c6-111">Syntax</span></span>


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a><span data-ttu-id="a53c6-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a53c6-112">Property value</span></span>

<span data-ttu-id="a53c6-113">**True** se o acesso exclusivo ao dispositivo de teclado da VM tiver sido adquirido; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="a53c6-113">**TRUE** if exclusive access to the VM's keyboard device has been acquired, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a53c6-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a53c6-114">Error codes</span></span>



| <span data-ttu-id="a53c6-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a53c6-115">Name/value</span></span>                                                                                                                                                                   | <span data-ttu-id="a53c6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a53c6-116">Meaning</span></span>                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a53c6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a53c6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="a53c6-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a53c6-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="a53c6-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a53c6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                        | <span data-ttu-id="a53c6-120">O parâmetro *isexclusive* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a53c6-120">The *isExclusive* parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="a53c6-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a53c6-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                   | <span data-ttu-id="a53c6-122">O modo exclusivo solicitado já está definido para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a53c6-122">The requested exclusive mode is already set for this device.</span></span> <span data-ttu-id="a53c6-123">Isso pode ocorrer ao tentar definir o modo exclusivo quando ele já foi adquirido ou ao tentar liberar o modo exclusivo quando ele não foi adquirido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a53c6-123">This can happen when trying to set exclusive mode when it has already been acquired, or when trying to release exclusive mode when it had not been previously acquired.</span></span><br/> |
| <dl> <span data-ttu-id="a53c6-124"><dt>VM \_ E & \_ set \_ Exclusive \_ mode \_ falham</dt> <dt>0xA0040825</dt></span><span class="sxs-lookup"><span data-stu-id="a53c6-124"><dt>VM\_E\_SET\_EXCLUSIVE\_MODE\_FAIL</dt> <dt>0xA0040825</dt></span></span> </dl> | <span data-ttu-id="a53c6-125">Falha ao definir ou liberar o modo exclusivo conforme solicitado.</span><span class="sxs-lookup"><span data-stu-id="a53c6-125">Failed to set or release exclusive mode as requested.</span></span> <span data-ttu-id="a53c6-126">Isso pode ocorrer porque a VM não está mais em execução ou porque outro processo já adquiriu o modo exclusivo no dispositivo de teclado da VM.</span><span class="sxs-lookup"><span data-stu-id="a53c6-126">This could be because the VM is no longer running, or because another process has already acquired exclusive mode on the VM's keyboard device.</span></span><br/>                                 |
| <dl> <span data-ttu-id="a53c6-127"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="a53c6-127"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                     | <span data-ttu-id="a53c6-128">A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.</span><span class="sxs-lookup"><span data-stu-id="a53c6-128">The specified string is empty, or contains an invalid key code.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="a53c6-129"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a53c6-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                | <span data-ttu-id="a53c6-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a53c6-130">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="a53c6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a53c6-131">Requirements</span></span>



| <span data-ttu-id="a53c6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53c6-132">Requirement</span></span> | <span data-ttu-id="a53c6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a53c6-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53c6-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a53c6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a53c6-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a53c6-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a53c6-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a53c6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a53c6-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a53c6-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a53c6-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a53c6-138">End of client support</span></span><br/>    | <span data-ttu-id="a53c6-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a53c6-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a53c6-140">Produto</span><span class="sxs-lookup"><span data-stu-id="a53c6-140">Product</span></span><br/>                  | <span data-ttu-id="a53c6-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a53c6-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a53c6-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a53c6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a53c6-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a53c6-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a53c6-144">IID</span><span class="sxs-lookup"><span data-stu-id="a53c6-144">IID</span></span><br/>                      | <span data-ttu-id="a53c6-145">IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="a53c6-145">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a53c6-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a53c6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53c6-147">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="a53c6-147">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

