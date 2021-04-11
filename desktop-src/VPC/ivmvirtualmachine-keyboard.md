---
title: Propriedade de teclado IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o dispositivo de teclado para a máquina virtual.
ms.assetid: bf516d07-eea9-40e3-b0d3-0fd4d3a04eb1
keywords:
- Propriedade de teclado virtual PC
- Propriedade de teclado virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade Keyboard
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Keyboard
- IVMVirtualMachine.get_Keyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31080b376a9e0fa999d568e5f3c7524d597aa0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295862"
---
# <a name="ivmvirtualmachinekeyboard-property"></a><span data-ttu-id="84162-106">Propriedade IVMVirtualMachine:: Keyboard</span><span class="sxs-lookup"><span data-stu-id="84162-106">IVMVirtualMachine::Keyboard property</span></span>

<span data-ttu-id="84162-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84162-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84162-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84162-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84162-109">Recupera o dispositivo de teclado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="84162-109">Retrieves the keyboard device for the virtual machine.</span></span>

<span data-ttu-id="84162-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="84162-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84162-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84162-111">Syntax</span></span>


```C++
HRESULT get_Keyboard(
  [out, retval] IVMKeyboard **keyboard
);
```



## <a name="property-value"></a><span data-ttu-id="84162-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="84162-112">Property value</span></span>

<span data-ttu-id="84162-113">O objeto [**IVMKeyboard**](ivmkeyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="84162-113">The [**IVMKeyboard**](ivmkeyboard.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="84162-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="84162-114">Error codes</span></span>



| <span data-ttu-id="84162-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="84162-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="84162-116">Significado</span><span class="sxs-lookup"><span data-stu-id="84162-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="84162-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="84162-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="84162-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="84162-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="84162-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="84162-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="84162-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="84162-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="84162-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="84162-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="84162-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="84162-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="84162-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="84162-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="84162-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="84162-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="84162-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84162-125">Requirements</span></span>



| <span data-ttu-id="84162-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="84162-126">Requirement</span></span> | <span data-ttu-id="84162-127">Valor</span><span class="sxs-lookup"><span data-stu-id="84162-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84162-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84162-128">Minimum supported client</span></span><br/> | <span data-ttu-id="84162-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="84162-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84162-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84162-130">Minimum supported server</span></span><br/> | <span data-ttu-id="84162-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="84162-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84162-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="84162-132">End of client support</span></span><br/>    | <span data-ttu-id="84162-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84162-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84162-134">Produto</span><span class="sxs-lookup"><span data-stu-id="84162-134">Product</span></span><br/>                  | <span data-ttu-id="84162-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84162-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84162-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84162-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="84162-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="84162-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="84162-138">IID</span><span class="sxs-lookup"><span data-stu-id="84162-138">IID</span></span><br/>                      | <span data-ttu-id="84162-139">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="84162-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="84162-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="84162-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84162-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="84162-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

