---
title: Propriedade IVMAccountant NetworkBytesSent (VPCCOMInterfaces. h)
description: Número total de bytes enviados por todos os adaptadores de rede virtual para esta máquina virtual.
ms.assetid: 3b5c3fa2-48c6-46c8-bbb6-5d1a9769308a
keywords:
- Propriedade NetworkBytesSent Virtual PC
- Propriedade NetworkBytesSent Virtual PC, interface IVMAccountant
- IVMAccountant interface virtual PC, Propriedade NetworkBytesSent
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesSent
- IVMAccountant.get_NetworkBytesSent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d25a6c0a9ee784af8bfab196fc9aaef0d1474d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918543"
---
# <a name="ivmaccountantnetworkbytessent-property"></a><span data-ttu-id="2008f-106">Propriedade IVMAccountant:: NetworkBytesSent</span><span class="sxs-lookup"><span data-stu-id="2008f-106">IVMAccountant::NetworkBytesSent property</span></span>

<span data-ttu-id="2008f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2008f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2008f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2008f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2008f-109">Recupera o número total de bytes enviados por todos os adaptadores de rede virtual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2008f-109">Retrieves the total number of bytes sent by all virtual network adapters for this virtual machine.</span></span>

<span data-ttu-id="2008f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2008f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2008f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2008f-111">Syntax</span></span>


```C++
HRESULT get_NetworkBytesSent(
  [out, retval] VARIANT *bytesSent
);
```



## <a name="property-value"></a><span data-ttu-id="2008f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2008f-112">Property value</span></span>

<span data-ttu-id="2008f-113">O número total de bytes enviados por todas as placas de interface de rede virtual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2008f-113">The total number of bytes sent by all virtual network interface cards for this virtual machine.</span></span> <span data-ttu-id="2008f-114">Ele é retornado como uma **variante** do tipo **VT \_ decimal**.</span><span class="sxs-lookup"><span data-stu-id="2008f-114">It is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2008f-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2008f-115">Error codes</span></span>



| <span data-ttu-id="2008f-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="2008f-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2008f-117">Significado</span><span class="sxs-lookup"><span data-stu-id="2008f-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="2008f-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2008f-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2008f-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2008f-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="2008f-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2008f-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2008f-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2008f-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="2008f-122"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2008f-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="2008f-123">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="2008f-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="2008f-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="2008f-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2008f-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="2008f-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="2008f-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="2008f-126">Remarks</span></span>

<span data-ttu-id="2008f-127">Observe que as estatísticas de e/s de rede são redefinidas para zero quando uma máquina virtual é ligada, redefinida ou restaurada do estado salvo.</span><span class="sxs-lookup"><span data-stu-id="2008f-127">Note that network I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="2008f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2008f-128">Requirements</span></span>



| <span data-ttu-id="2008f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2008f-129">Requirement</span></span> | <span data-ttu-id="2008f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="2008f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2008f-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2008f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2008f-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2008f-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2008f-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2008f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2008f-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2008f-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2008f-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2008f-135">End of client support</span></span><br/>    | <span data-ttu-id="2008f-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2008f-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2008f-137">Produto</span><span class="sxs-lookup"><span data-stu-id="2008f-137">Product</span></span><br/>                  | <span data-ttu-id="2008f-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2008f-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2008f-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2008f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2008f-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2008f-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2008f-141">IID</span><span class="sxs-lookup"><span data-stu-id="2008f-141">IID</span></span><br/>                      | <span data-ttu-id="2008f-142">IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="2008f-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="2008f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2008f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2008f-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="2008f-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

