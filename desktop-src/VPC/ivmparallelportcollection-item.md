---
title: Propriedade de item IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Recupera o objeto de porta paralela que corresponde ao índice especificado.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMParallelPortCollection
- IVMParallelPortCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa450f1859db8af6ed884b37fc693fc4fb1990f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455805"
---
# <a name="ivmparallelportcollectionitem-property"></a><span data-ttu-id="b433d-106">Propriedade IVMParallelPortCollection:: item</span><span class="sxs-lookup"><span data-stu-id="b433d-106">IVMParallelPortCollection::Item property</span></span>

<span data-ttu-id="b433d-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b433d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b433d-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b433d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b433d-109">Recupera o objeto de porta paralela que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="b433d-109">Retrieves the parallel port object that corresponds to the specified index.</span></span>

<span data-ttu-id="b433d-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b433d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b433d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b433d-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="b433d-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b433d-112">Property value</span></span>

<span data-ttu-id="b433d-113">O objeto [**IVMParallelPort**](ivmparallelport.md) .</span><span class="sxs-lookup"><span data-stu-id="b433d-113">The [**IVMParallelPort**](ivmparallelport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b433d-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b433d-114">Error codes</span></span>



| <span data-ttu-id="b433d-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="b433d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b433d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b433d-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b433d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b433d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b433d-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b433d-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="b433d-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b433d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b433d-120">O parâmetro *vmParallelPort* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b433d-120">The *vmParallelPort* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="b433d-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="b433d-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="b433d-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="b433d-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="b433d-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b433d-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b433d-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="b433d-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="b433d-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b433d-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b433d-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b433d-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="b433d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b433d-127">Requirements</span></span>



| <span data-ttu-id="b433d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b433d-128">Requirement</span></span> | <span data-ttu-id="b433d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b433d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b433d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b433d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b433d-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b433d-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b433d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b433d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b433d-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b433d-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b433d-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b433d-134">End of client support</span></span><br/>    | <span data-ttu-id="b433d-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b433d-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b433d-136">Produto</span><span class="sxs-lookup"><span data-stu-id="b433d-136">Product</span></span><br/>                  | <span data-ttu-id="b433d-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b433d-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b433d-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b433d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b433d-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b433d-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b433d-140">IID</span><span class="sxs-lookup"><span data-stu-id="b433d-140">IID</span></span><br/>                      | <span data-ttu-id="b433d-141">IID \_ IVMParallelPortCollection é definido como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="b433d-141">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b433d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b433d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b433d-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="b433d-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="b433d-144">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="b433d-144">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

