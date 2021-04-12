---
title: Propriedade IVMGuestOS ServicePackMinor (VPCCOMInterfaces. h)
description: A versão secundária do service pack do sistema operacional convidado em execução na máquina virtual.
ms.assetid: f1413b5a-6a74-42a6-9671-b00b7c8912fa
keywords:
- Propriedade ServicePackMinor Virtual PC
- Propriedade ServicePackMinor Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade ServicePackMinor
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMinor
- IVMGuestOS.get_ServicePackMinor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e7a94c5ed8de42cc2455160424246e899014cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455305"
---
# <a name="ivmguestosservicepackminor-property"></a><span data-ttu-id="1c591-106">Propriedade IVMGuestOS:: ServicePackMinor</span><span class="sxs-lookup"><span data-stu-id="1c591-106">IVMGuestOS::ServicePackMinor property</span></span>

<span data-ttu-id="1c591-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1c591-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1c591-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1c591-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1c591-109">A versão secundária do service pack do sistema operacional convidado em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c591-109">The minor version of the service pack of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="1c591-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1c591-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c591-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c591-111">Syntax</span></span>


```C++
HRESULT get_ServicePackMinor(
  [out, retval] BSTR *servicePackMinor
);
```



## <a name="property-value"></a><span data-ttu-id="1c591-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1c591-112">Property value</span></span>

<span data-ttu-id="1c591-113">O número de versão secundária do Service Pack mais recente instalado.</span><span class="sxs-lookup"><span data-stu-id="1c591-113">The minor version number of the latest Service Pack installed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1c591-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1c591-114">Error codes</span></span>



| <span data-ttu-id="1c591-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="1c591-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="1c591-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1c591-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1c591-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1c591-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="1c591-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1c591-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="1c591-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="1c591-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="1c591-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c591-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="1c591-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="1c591-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="1c591-122">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="1c591-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="1c591-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="1c591-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="1c591-124">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="1c591-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="1c591-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="1c591-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="1c591-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1c591-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="1c591-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c591-127">Requirements</span></span>



| <span data-ttu-id="1c591-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c591-128">Requirement</span></span> | <span data-ttu-id="1c591-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1c591-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c591-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c591-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1c591-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1c591-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c591-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c591-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1c591-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1c591-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1c591-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1c591-134">End of client support</span></span><br/>    | <span data-ttu-id="1c591-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c591-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1c591-136">Produto</span><span class="sxs-lookup"><span data-stu-id="1c591-136">Product</span></span><br/>                  | <span data-ttu-id="1c591-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1c591-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1c591-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c591-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c591-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c591-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1c591-140">IID</span><span class="sxs-lookup"><span data-stu-id="1c591-140">IID</span></span><br/>                      | <span data-ttu-id="1c591-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="1c591-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1c591-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c591-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c591-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="1c591-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

