---
title: Propriedade IVMGuestOS ServicePackMajor (VPCCOMInterfaces. h)
description: A versão principal do service pack do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 87dbc4cc-8a8d-468f-9a29-e5047029b032
keywords:
- Propriedade ServicePackMajor Virtual PC
- Propriedade ServicePackMajor Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade ServicePackMajor
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMajor
- IVMGuestOS.get_ServicePackMajor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1fa89b51e26354ce2983ad42025b1b9a3922d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085699"
---
# <a name="ivmguestosservicepackmajor-property"></a><span data-ttu-id="96f3c-106">Propriedade IVMGuestOS:: ServicePackMajor</span><span class="sxs-lookup"><span data-stu-id="96f3c-106">IVMGuestOS::ServicePackMajor property</span></span>

<span data-ttu-id="96f3c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96f3c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96f3c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96f3c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96f3c-109">A versão principal do service pack do sistema operacional convidado em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="96f3c-109">The major version of the service pack of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="96f3c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="96f3c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="96f3c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96f3c-111">Syntax</span></span>


```C++
HRESULT get_ServicePackMajor(
  [out, retval] BSTR *servicePackMajor
);
```



## <a name="property-value"></a><span data-ttu-id="96f3c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="96f3c-112">Property value</span></span>

<span data-ttu-id="96f3c-113">O número de versão principal do Service Pack mais recente instalado.</span><span class="sxs-lookup"><span data-stu-id="96f3c-113">The major version number of the latest Service Pack installed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="96f3c-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="96f3c-114">Error codes</span></span>



| <span data-ttu-id="96f3c-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="96f3c-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="96f3c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="96f3c-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="96f3c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96f3c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="96f3c-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="96f3c-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="96f3c-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="96f3c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="96f3c-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="96f3c-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="96f3c-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="96f3c-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="96f3c-122">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="96f3c-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="96f3c-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="96f3c-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="96f3c-124">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="96f3c-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="96f3c-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="96f3c-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="96f3c-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="96f3c-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="96f3c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96f3c-127">Requirements</span></span>



| <span data-ttu-id="96f3c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f3c-128">Requirement</span></span> | <span data-ttu-id="96f3c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="96f3c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96f3c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96f3c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="96f3c-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="96f3c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96f3c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96f3c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="96f3c-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="96f3c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96f3c-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="96f3c-134">End of client support</span></span><br/>    | <span data-ttu-id="96f3c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96f3c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96f3c-136">Produto</span><span class="sxs-lookup"><span data-stu-id="96f3c-136">Product</span></span><br/>                  | <span data-ttu-id="96f3c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96f3c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96f3c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96f3c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f3c-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f3c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96f3c-140">IID</span><span class="sxs-lookup"><span data-stu-id="96f3c-140">IID</span></span><br/>                      | <span data-ttu-id="96f3c-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="96f3c-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="96f3c-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="96f3c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f3c-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="96f3c-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

