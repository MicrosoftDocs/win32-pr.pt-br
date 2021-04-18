---
title: Propriedade IVMGuestOS OSMinorVersion (VPCCOMInterfaces. h)
description: A versão secundária do sistema operacional convidado em execução na máquina virtual.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- Propriedade OSMinorVersion Virtual PC
- Propriedade OSMinorVersion Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade OSMinorVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c068ee6d8112561f57d0644f6bc7bc4844096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770584"
---
# <a name="ivmguestososminorversion-property"></a><span data-ttu-id="3791a-106">Propriedade IVMGuestOS:: OSMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3791a-106">IVMGuestOS::OSMinorVersion property</span></span>

<span data-ttu-id="3791a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3791a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3791a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3791a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3791a-109">Recupera a versão secundária do sistema operacional convidado em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3791a-109">Retrieves the minor version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="3791a-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3791a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3791a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3791a-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="3791a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3791a-112">Property value</span></span>

<span data-ttu-id="3791a-113">A versão secundária.</span><span class="sxs-lookup"><span data-stu-id="3791a-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3791a-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3791a-114">Error codes</span></span>



| <span data-ttu-id="3791a-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3791a-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="3791a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3791a-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3791a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3791a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="3791a-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3791a-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="3791a-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3791a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="3791a-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3791a-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="3791a-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="3791a-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="3791a-122">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="3791a-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="3791a-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="3791a-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="3791a-124">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="3791a-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="3791a-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3791a-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="3791a-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3791a-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="3791a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3791a-127">Requirements</span></span>



| <span data-ttu-id="3791a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3791a-128">Requirement</span></span> | <span data-ttu-id="3791a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3791a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3791a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3791a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3791a-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3791a-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3791a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3791a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3791a-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3791a-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3791a-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3791a-134">End of client support</span></span><br/>    | <span data-ttu-id="3791a-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3791a-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3791a-136">Produto</span><span class="sxs-lookup"><span data-stu-id="3791a-136">Product</span></span><br/>                  | <span data-ttu-id="3791a-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3791a-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3791a-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3791a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3791a-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3791a-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3791a-140">IID</span><span class="sxs-lookup"><span data-stu-id="3791a-140">IID</span></span><br/>                      | <span data-ttu-id="3791a-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="3791a-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3791a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3791a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3791a-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="3791a-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

