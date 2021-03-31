---
title: Propriedade Count de IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera o número de portas seriais nesta coleção.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMSerialPortCollection
- Virtual PC de interface IVMSerialPortCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0503f00fd1df7d27a8eeafedd3efe42619b98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824539"
---
# <a name="ivmserialportcollectioncount-property"></a><span data-ttu-id="7ab20-106">Propriedade IVMSerialPortCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="7ab20-106">IVMSerialPortCollection::Count property</span></span>

<span data-ttu-id="7ab20-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7ab20-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7ab20-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7ab20-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7ab20-109">Recupera o número de portas seriais nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="7ab20-109">Retrieves the number of serial ports in this collection.</span></span>

<span data-ttu-id="7ab20-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7ab20-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab20-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ab20-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="7ab20-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7ab20-112">Property value</span></span>

<span data-ttu-id="7ab20-113">O número de portas seriais.</span><span class="sxs-lookup"><span data-stu-id="7ab20-113">The number of serial ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7ab20-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7ab20-114">Error codes</span></span>



| <span data-ttu-id="7ab20-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="7ab20-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="7ab20-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7ab20-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="7ab20-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7ab20-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="7ab20-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7ab20-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="7ab20-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7ab20-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="7ab20-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7ab20-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="7ab20-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ab20-121">Requirements</span></span>



| <span data-ttu-id="7ab20-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab20-122">Requirement</span></span> | <span data-ttu-id="7ab20-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7ab20-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab20-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ab20-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab20-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7ab20-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ab20-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ab20-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab20-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7ab20-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7ab20-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7ab20-128">End of client support</span></span><br/>    | <span data-ttu-id="7ab20-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ab20-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7ab20-130">Produto</span><span class="sxs-lookup"><span data-stu-id="7ab20-130">Product</span></span><br/>                  | <span data-ttu-id="7ab20-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7ab20-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7ab20-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ab20-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ab20-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab20-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7ab20-134">IID</span><span class="sxs-lookup"><span data-stu-id="7ab20-134">IID</span></span><br/>                      | <span data-ttu-id="7ab20-135">IID \_ IVMSerialPortCollection é definido como dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="7ab20-135">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="7ab20-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7ab20-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab20-137">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="7ab20-137">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

