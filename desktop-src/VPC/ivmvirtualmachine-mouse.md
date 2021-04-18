---
title: Propriedade de mouse IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o dispositivo de mouse para a máquina virtual.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Propriedade do mouse Virtual PC
- Propriedade do mouse Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade do mouse
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813249"
---
# <a name="ivmvirtualmachinemouse-property"></a><span data-ttu-id="01c9b-106">Propriedade IVMVirtualMachine:: mouse</span><span class="sxs-lookup"><span data-stu-id="01c9b-106">IVMVirtualMachine::Mouse property</span></span>

<span data-ttu-id="01c9b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01c9b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="01c9b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="01c9b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="01c9b-109">Recupera o dispositivo de mouse para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="01c9b-109">Retrieves the mouse device for the virtual machine.</span></span>

<span data-ttu-id="01c9b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="01c9b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c9b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01c9b-111">Syntax</span></span>


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a><span data-ttu-id="01c9b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="01c9b-112">Property value</span></span>

<span data-ttu-id="01c9b-113">Um objeto [**IVMMouse**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="01c9b-113">An [**IVMMouse**](ivmmouse.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01c9b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="01c9b-114">Error codes</span></span>



| <span data-ttu-id="01c9b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="01c9b-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="01c9b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="01c9b-116">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="01c9b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01c9b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="01c9b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="01c9b-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="01c9b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="01c9b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="01c9b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="01c9b-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="01c9b-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="01c9b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="01c9b-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="01c9b-122">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="01c9b-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="01c9b-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="01c9b-124">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="01c9b-124">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="01c9b-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="01c9b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="01c9b-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="01c9b-126">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="01c9b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01c9b-127">Requirements</span></span>



| <span data-ttu-id="01c9b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c9b-128">Requirement</span></span> | <span data-ttu-id="01c9b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="01c9b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c9b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01c9b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="01c9b-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01c9b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01c9b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01c9b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="01c9b-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="01c9b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="01c9b-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="01c9b-134">End of client support</span></span><br/>    | <span data-ttu-id="01c9b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="01c9b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="01c9b-136">Produto</span><span class="sxs-lookup"><span data-stu-id="01c9b-136">Product</span></span><br/>                  | <span data-ttu-id="01c9b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="01c9b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="01c9b-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01c9b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c9b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c9b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="01c9b-140">IID</span><span class="sxs-lookup"><span data-stu-id="01c9b-140">IID</span></span><br/>                      | <span data-ttu-id="01c9b-141">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="01c9b-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="01c9b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="01c9b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c9b-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="01c9b-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

