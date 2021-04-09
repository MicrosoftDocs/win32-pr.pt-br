---
title: Propriedade Count de IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Número de unidades de disquete nesta coleção.
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMFloppyDriveCollection
- Virtual PC de interface IVMFloppyDriveCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b00c13795a633c664cea2c4476d58b346f9108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009729"
---
# <a name="ivmfloppydrivecollectioncount-property"></a><span data-ttu-id="e3851-106">Propriedade IVMFloppyDriveCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="e3851-106">IVMFloppyDriveCollection::Count property</span></span>

<span data-ttu-id="e3851-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e3851-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e3851-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e3851-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e3851-109">Recupera o número de unidades de disquete nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="e3851-109">Retrieves the number of floppy drives in this collection.</span></span>

<span data-ttu-id="e3851-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e3851-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3851-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3851-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="e3851-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e3851-112">Property value</span></span>

<span data-ttu-id="e3851-113">O número de unidades de mídia de disquete.</span><span class="sxs-lookup"><span data-stu-id="e3851-113">The number of floppy media drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e3851-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e3851-114">Error codes</span></span>



| <span data-ttu-id="e3851-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e3851-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e3851-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e3851-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e3851-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3851-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e3851-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e3851-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e3851-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e3851-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e3851-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e3851-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e3851-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e3851-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="e3851-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="e3851-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="e3851-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e3851-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e3851-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e3851-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e3851-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3851-125">Requirements</span></span>



| <span data-ttu-id="e3851-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3851-126">Requirement</span></span> | <span data-ttu-id="e3851-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e3851-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3851-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3851-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e3851-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e3851-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3851-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3851-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e3851-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e3851-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e3851-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e3851-132">End of client support</span></span><br/>    | <span data-ttu-id="e3851-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3851-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e3851-134">Produto</span><span class="sxs-lookup"><span data-stu-id="e3851-134">Product</span></span><br/>                  | <span data-ttu-id="e3851-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e3851-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e3851-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3851-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3851-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3851-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e3851-138">IID</span><span class="sxs-lookup"><span data-stu-id="e3851-138">IID</span></span><br/>                      | <span data-ttu-id="e3851-139">IID \_ IVMFloppyDriveCollection é definido como 8ba70a25-f698-4ee5-85CE-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="e3851-139">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="e3851-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3851-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3851-141">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="e3851-141">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

