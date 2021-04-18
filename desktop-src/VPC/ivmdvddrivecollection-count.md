---
title: Propriedade Count de IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera o número de unidades de CD e DVD nesta coleção.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMDVDDriveCollection
- Virtual PC de interface IVMDVDDriveCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759815"
---
# <a name="ivmdvddrivecollectioncount-property"></a><span data-ttu-id="c3284-106">Propriedade IVMDVDDriveCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="c3284-106">IVMDVDDriveCollection::Count property</span></span>

<span data-ttu-id="c3284-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3284-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c3284-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c3284-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c3284-109">Recupera o número de unidades de CD e DVD nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="c3284-109">Retrieves the number of CD and DVD drives in this collection.</span></span>

<span data-ttu-id="c3284-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c3284-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3284-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3284-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="c3284-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c3284-112">Property value</span></span>

<span data-ttu-id="c3284-113">O número de unidades de CD e DVD.</span><span class="sxs-lookup"><span data-stu-id="c3284-113">The number of CD and DVD drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c3284-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c3284-114">Error codes</span></span>



| <span data-ttu-id="c3284-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="c3284-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c3284-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c3284-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c3284-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c3284-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c3284-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c3284-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c3284-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="c3284-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c3284-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3284-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c3284-121"><dt>E \_ FALHA</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="c3284-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="c3284-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="c3284-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="c3284-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c3284-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c3284-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="c3284-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c3284-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="c3284-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c3284-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="c3284-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c3284-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3284-127">Requirements</span></span>



| <span data-ttu-id="c3284-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3284-128">Requirement</span></span> | <span data-ttu-id="c3284-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c3284-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3284-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3284-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c3284-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c3284-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3284-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3284-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c3284-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c3284-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c3284-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c3284-134">End of client support</span></span><br/>    | <span data-ttu-id="c3284-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3284-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c3284-136">Produto</span><span class="sxs-lookup"><span data-stu-id="c3284-136">Product</span></span><br/>                  | <span data-ttu-id="c3284-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c3284-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c3284-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3284-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3284-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3284-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c3284-140">IID</span><span class="sxs-lookup"><span data-stu-id="c3284-140">IID</span></span><br/>                      | <span data-ttu-id="c3284-141">IID \_ IVMDVDDriveCollection é definido como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="c3284-141">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="c3284-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3284-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3284-143">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="c3284-143">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

