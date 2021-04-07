---
title: Propriedade OSVersion IVMGuestOS (VPCCOMInterfaces. h)
description: A versão do sistema operacional convidado em execução na máquina virtual.
ms.assetid: ef189c14-dc87-4d77-9567-345f49483b13
keywords:
- Propriedade OSVersion Virtual PC
- Propriedade OSVersion Virtual PC, interface IVMGuestOS
- Virtual PC interface IVMGuestOS, Propriedade OSVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSVersion
- IVMGuestOS.get_OSVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338ae98c1830bae208f14aa522f716ac47899731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824380"
---
# <a name="ivmguestososversion-property"></a><span data-ttu-id="4c881-106">Propriedade IVMGuestOS:: OSVersion</span><span class="sxs-lookup"><span data-stu-id="4c881-106">IVMGuestOS::OSVersion property</span></span>

<span data-ttu-id="4c881-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c881-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4c881-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4c881-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4c881-109">Recupera a versão do sistema operacional convidado em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c881-109">Retrieves the version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="4c881-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4c881-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c881-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c881-111">Syntax</span></span>


```C++
HRESULT get_OSVersion(
  [out, retval] BSTR *OSVersion
);
```



## <a name="property-value"></a><span data-ttu-id="4c881-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4c881-112">Property value</span></span>

<span data-ttu-id="4c881-113">A versão.</span><span class="sxs-lookup"><span data-stu-id="4c881-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4c881-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4c881-114">Error codes</span></span>



| <span data-ttu-id="4c881-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="4c881-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="4c881-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4c881-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4c881-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c881-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="4c881-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4c881-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="4c881-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4c881-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="4c881-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4c881-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="4c881-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4c881-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="4c881-122">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="4c881-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="4c881-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="4c881-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="4c881-124">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="4c881-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="4c881-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4c881-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="4c881-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4c881-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="4c881-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c881-127">Requirements</span></span>



| <span data-ttu-id="4c881-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c881-128">Requirement</span></span> | <span data-ttu-id="4c881-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4c881-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c881-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c881-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c881-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4c881-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c881-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c881-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c881-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c881-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4c881-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4c881-134">End of client support</span></span><br/>    | <span data-ttu-id="4c881-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c881-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c881-136">Produto</span><span class="sxs-lookup"><span data-stu-id="4c881-136">Product</span></span><br/>                  | <span data-ttu-id="4c881-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4c881-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4c881-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c881-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c881-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c881-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4c881-140">IID</span><span class="sxs-lookup"><span data-stu-id="4c881-140">IID</span></span><br/>                      | <span data-ttu-id="4c881-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="4c881-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4c881-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c881-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c881-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="4c881-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

