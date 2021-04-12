---
title: Propriedade IVMGuestOS OSName (VPCCOMInterfaces. h)
description: O nome do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- Propriedade OSName Virtual PC
- Propriedade OSName Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade OSName
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672c7b2c852bcbb1ec39b61889b03738e3a2df23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455092"
---
# <a name="ivmguestososname-property"></a><span data-ttu-id="8059c-106">Propriedade IVMGuestOS:: OSName</span><span class="sxs-lookup"><span data-stu-id="8059c-106">IVMGuestOS::OSName property</span></span>

<span data-ttu-id="8059c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8059c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8059c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8059c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8059c-109">Recupera o nome do sistema operacional convidado em execução na VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="8059c-109">Retrieves the name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="8059c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8059c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8059c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8059c-111">Syntax</span></span>


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a><span data-ttu-id="8059c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8059c-112">Property value</span></span>

<span data-ttu-id="8059c-113">O nome completo (incluindo o nome do conjunto) do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="8059c-113">The full name (including suite name) of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8059c-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8059c-114">Error codes</span></span>



| <span data-ttu-id="8059c-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="8059c-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="8059c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8059c-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8059c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8059c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="8059c-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8059c-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="8059c-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="8059c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="8059c-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8059c-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="8059c-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8059c-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="8059c-122">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="8059c-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="8059c-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="8059c-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="8059c-124">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="8059c-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="8059c-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="8059c-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="8059c-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8059c-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="8059c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="8059c-127">Remarks</span></span>

<span data-ttu-id="8059c-128">A VM deve estar em execução (ou seja, totalmente inicializada e não desligada) e os componentes de integração devem ser instalados quando esse método é invocado.</span><span class="sxs-lookup"><span data-stu-id="8059c-128">The VM must be running (that is, fully booted and not shutting down) and integration components must be installed when this method is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="8059c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8059c-129">Requirements</span></span>



| <span data-ttu-id="8059c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8059c-130">Requirement</span></span> | <span data-ttu-id="8059c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8059c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8059c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8059c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8059c-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8059c-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8059c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8059c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8059c-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8059c-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8059c-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8059c-136">End of client support</span></span><br/>    | <span data-ttu-id="8059c-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8059c-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8059c-138">Produto</span><span class="sxs-lookup"><span data-stu-id="8059c-138">Product</span></span><br/>                  | <span data-ttu-id="8059c-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8059c-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8059c-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8059c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8059c-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8059c-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8059c-142">IID</span><span class="sxs-lookup"><span data-stu-id="8059c-142">IID</span></span><br/>                      | <span data-ttu-id="8059c-143">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8059c-143">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8059c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8059c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8059c-145">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="8059c-145">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

