---
title: Propriedade IVMGuestOS ScreenLocked (VPCCOMInterfaces. h)
description: Indica se a tela no sistema operacional convidado está bloqueada.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- Propriedade ScreenLocked Virtual PC
- Propriedade ScreenLocked Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade ScreenLocked
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009468"
---
# <a name="ivmguestosscreenlocked-property"></a><span data-ttu-id="5568c-106">Propriedade IVMGuestOS:: ScreenLocked</span><span class="sxs-lookup"><span data-stu-id="5568c-106">IVMGuestOS::ScreenLocked property</span></span>

<span data-ttu-id="5568c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5568c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5568c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5568c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5568c-109">Indica se a tela no sistema operacional convidado está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="5568c-109">Indicates whether the screen in the guest operating system is locked.</span></span>

<span data-ttu-id="5568c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5568c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5568c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5568c-111">Syntax</span></span>


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a><span data-ttu-id="5568c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5568c-112">Property value</span></span>

<span data-ttu-id="5568c-113">**Variante \_ TRUE** se a tela estiver bloqueada no sistema operacional convidado; caso contrário, **Variant \_ false** .</span><span class="sxs-lookup"><span data-stu-id="5568c-113">**VARIANT\_TRUE** if screen is locked in guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5568c-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5568c-114">Error codes</span></span>



| <span data-ttu-id="5568c-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="5568c-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="5568c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5568c-116">Meaning</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5568c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5568c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="5568c-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5568c-118">The operation was successful.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="5568c-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="5568c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="5568c-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5568c-120">The parameter is **NULL**.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="5568c-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5568c-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="5568c-122">A máquina virtual (VM) deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="5568c-122">The virtual machine (VM) must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="5568c-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="5568c-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="5568c-124">O recurso componentes de integração não está habilitado no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="5568c-124">The integration components feature is not enabled in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="5568c-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="5568c-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="5568c-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="5568c-126">An unexpected error has occurred.</span></span><br/>                                                |



## <a name="requirements"></a><span data-ttu-id="5568c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5568c-127">Requirements</span></span>



| <span data-ttu-id="5568c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5568c-128">Requirement</span></span> | <span data-ttu-id="5568c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5568c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5568c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5568c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5568c-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5568c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5568c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5568c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5568c-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5568c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5568c-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5568c-134">End of client support</span></span><br/>    | <span data-ttu-id="5568c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5568c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5568c-136">Produto</span><span class="sxs-lookup"><span data-stu-id="5568c-136">Product</span></span><br/>                  | <span data-ttu-id="5568c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5568c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5568c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5568c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5568c-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5568c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5568c-140">IID</span><span class="sxs-lookup"><span data-stu-id="5568c-140">IID</span></span><br/>                      | <span data-ttu-id="5568c-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="5568c-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5568c-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="5568c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5568c-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="5568c-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

