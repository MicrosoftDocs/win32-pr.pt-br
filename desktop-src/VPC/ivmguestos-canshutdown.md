---
title: Propriedade Cancel Shutdown do IVMGuestOS (VPCCOMInterfaces. h)
description: Indica se o sistema operacional convidado pode ser desligado corretamente.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- Desligamento da propriedade Virtual PC
- Propriedade CanShutdown Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, desshutdown Property
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f76e652b7a172da6f5a438f72b09443a13dcce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295897"
---
# <a name="ivmguestoscanshutdown-property"></a><span data-ttu-id="6d7cb-106">Propriedade IVMGuestOS:: CanShutdown</span><span class="sxs-lookup"><span data-stu-id="6d7cb-106">IVMGuestOS::CanShutdown property</span></span>

<span data-ttu-id="6d7cb-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d7cb-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d7cb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d7cb-109">Indica se o sistema operacional convidado pode ser desligado corretamente (requer componentes de integração).</span><span class="sxs-lookup"><span data-stu-id="6d7cb-109">Indicates whether the guest operating system can be cleanly shut down (requires Integration Components).</span></span>

<span data-ttu-id="6d7cb-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7cb-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d7cb-111">Syntax</span></span>


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a><span data-ttu-id="6d7cb-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d7cb-112">Property value</span></span>

<span data-ttu-id="6d7cb-113">**Variante \_ TRUE** se o sistema operacional der suporte à operação de desligamento e a **variante \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-113">**VARIANT\_TRUE** if the operating system supports the shutdown operation and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d7cb-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6d7cb-114">Error codes</span></span>



| <span data-ttu-id="6d7cb-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="6d7cb-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6d7cb-116">Significado</span><span class="sxs-lookup"><span data-stu-id="6d7cb-116">Meaning</span></span>                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="6d7cb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d7cb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6d7cb-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-118">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="6d7cb-119"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6d7cb-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="6d7cb-120">A máquina virtual não está ativada.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-120">The virtual machine is not turned on.</span></span><br/>   |
| <dl> <span data-ttu-id="6d7cb-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6d7cb-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6d7cb-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-122">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="6d7cb-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d7cb-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6d7cb-124">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-124">The virtual machine could not be found.</span></span><br/> |
| <dl> <span data-ttu-id="6d7cb-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6d7cb-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6d7cb-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-126">An unexpected error has occurred.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="6d7cb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d7cb-127">Requirements</span></span>



| <span data-ttu-id="6d7cb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d7cb-128">Requirement</span></span> | <span data-ttu-id="6d7cb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6d7cb-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7cb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d7cb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6d7cb-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6d7cb-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d7cb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d7cb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6d7cb-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6d7cb-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d7cb-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6d7cb-134">End of client support</span></span><br/>    | <span data-ttu-id="6d7cb-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d7cb-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d7cb-136">Produto</span><span class="sxs-lookup"><span data-stu-id="6d7cb-136">Product</span></span><br/>                  | <span data-ttu-id="6d7cb-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d7cb-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d7cb-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d7cb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d7cb-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d7cb-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d7cb-140">IID</span><span class="sxs-lookup"><span data-stu-id="6d7cb-140">IID</span></span><br/>                      | <span data-ttu-id="6d7cb-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="6d7cb-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6d7cb-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d7cb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7cb-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="6d7cb-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

