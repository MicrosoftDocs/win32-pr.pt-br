---
title: Propriedade nome do IVMParallelPort (VPCCOMInterfaces. h)
description: Nome da porta paralela.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Propriedade do nome Virtual PC
- Propriedade de nome Virtual PC, interface IVMParallelPort
- IVMParallelPort interface virtual PC, Propriedade Name
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085125"
---
# <a name="ivmparallelportname-property"></a><span data-ttu-id="53e00-106">Propriedade IVMParallelPort:: Name</span><span class="sxs-lookup"><span data-stu-id="53e00-106">IVMParallelPort::Name property</span></span>

<span data-ttu-id="53e00-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="53e00-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="53e00-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="53e00-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="53e00-109">Recupera e define o nome da porta paralela.</span><span class="sxs-lookup"><span data-stu-id="53e00-109">Retrieves and sets the name of the parallel port.</span></span>

<span data-ttu-id="53e00-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="53e00-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e00-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="53e00-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="53e00-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="53e00-112">Property value</span></span>

<span data-ttu-id="53e00-113">Define o nome da porta paralela (por exemplo, "LPT1").</span><span class="sxs-lookup"><span data-stu-id="53e00-113">Sets the name of the parallel port (for example, "LPT1").</span></span>

## <a name="error-codes"></a><span data-ttu-id="53e00-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="53e00-114">Error codes</span></span>



| <span data-ttu-id="53e00-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="53e00-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="53e00-116">Significado</span><span class="sxs-lookup"><span data-stu-id="53e00-116">Meaning</span></span>                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="53e00-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53e00-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="53e00-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="53e00-118">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="53e00-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="53e00-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="53e00-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="53e00-120">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="53e00-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="53e00-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="53e00-122">O parâmetro refere-se a uma porta paralela que não é válida.</span><span class="sxs-lookup"><span data-stu-id="53e00-122">The parameter refers to a parallel port that is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="53e00-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="53e00-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="53e00-124">A configuração desta máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="53e00-124">The configuration for this virtual machine is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="53e00-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="53e00-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="53e00-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="53e00-126">An unexpected error has occurred.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="53e00-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53e00-127">Requirements</span></span>



| <span data-ttu-id="53e00-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e00-128">Requirement</span></span> | <span data-ttu-id="53e00-129">Valor</span><span class="sxs-lookup"><span data-stu-id="53e00-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53e00-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53e00-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53e00-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="53e00-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53e00-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53e00-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53e00-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="53e00-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="53e00-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="53e00-134">End of client support</span></span><br/>    | <span data-ttu-id="53e00-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="53e00-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="53e00-136">Produto</span><span class="sxs-lookup"><span data-stu-id="53e00-136">Product</span></span><br/>                  | <span data-ttu-id="53e00-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="53e00-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="53e00-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53e00-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="53e00-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="53e00-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="53e00-140">IID</span><span class="sxs-lookup"><span data-stu-id="53e00-140">IID</span></span><br/>                      | <span data-ttu-id="53e00-141">IID \_ IVMParallelPort é definido como 097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="53e00-141">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="53e00-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="53e00-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e00-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="53e00-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

