---
title: Propriedade SerialPorts IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de portas seriais.
ms.assetid: 502fe4f1-c58c-460c-8431-41fddd753d18
keywords:
- Propriedade SerialPorts Virtual PC
- Propriedade SerialPorts Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade SerialPorts
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SerialPorts
- IVMVirtualMachine.get_SerialPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18119c649014a020dd2a2d4e2fdeb7c2bbaae87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499640"
---
# <a name="ivmvirtualmachineserialports-property"></a><span data-ttu-id="761f1-106">Propriedade IVMVirtualMachine:: SerialPorts</span><span class="sxs-lookup"><span data-stu-id="761f1-106">IVMVirtualMachine::SerialPorts property</span></span>

<span data-ttu-id="761f1-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="761f1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="761f1-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="761f1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="761f1-109">Recupera uma coleção enumerável de portas seriais.</span><span class="sxs-lookup"><span data-stu-id="761f1-109">Retrieves an enumerable collection of serial ports.</span></span>

<span data-ttu-id="761f1-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="761f1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="761f1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="761f1-111">Syntax</span></span>


```C++
HRESULT get_SerialPorts(
  [out, retval] IVMSerialPortCollection **serialPortCollection
);
```



## <a name="property-value"></a><span data-ttu-id="761f1-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="761f1-112">Property value</span></span>

<span data-ttu-id="761f1-113">Um objeto [**IVMSerialPortCollection**](ivmserialportcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="761f1-113">An [**IVMSerialPortCollection**](ivmserialportcollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="761f1-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="761f1-114">Error codes</span></span>



| <span data-ttu-id="761f1-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="761f1-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="761f1-116">Significado</span><span class="sxs-lookup"><span data-stu-id="761f1-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="761f1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="761f1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="761f1-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="761f1-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="761f1-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="761f1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="761f1-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="761f1-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="761f1-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="761f1-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="761f1-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="761f1-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="761f1-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="761f1-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="761f1-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="761f1-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="761f1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="761f1-125">Requirements</span></span>



| <span data-ttu-id="761f1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="761f1-126">Requirement</span></span> | <span data-ttu-id="761f1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="761f1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="761f1-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="761f1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="761f1-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="761f1-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="761f1-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="761f1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="761f1-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="761f1-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="761f1-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="761f1-132">End of client support</span></span><br/>    | <span data-ttu-id="761f1-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="761f1-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="761f1-134">Produto</span><span class="sxs-lookup"><span data-stu-id="761f1-134">Product</span></span><br/>                  | <span data-ttu-id="761f1-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="761f1-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="761f1-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="761f1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="761f1-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="761f1-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="761f1-138">IID</span><span class="sxs-lookup"><span data-stu-id="761f1-138">IID</span></span><br/>                      | <span data-ttu-id="761f1-139">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="761f1-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="761f1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="761f1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761f1-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="761f1-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

