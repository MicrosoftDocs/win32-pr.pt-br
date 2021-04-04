---
title: Propriedade Count de IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera o número de conexões de disco rígido nesta coleção.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMHardDiskConnectionCollection
- Virtual PC de interface IVMHardDiskConnectionCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34bbf4d07d7c5967ccfc38e16a743105de8e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644713"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a><span data-ttu-id="8370f-106">Propriedade IVMHardDiskConnectionCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="8370f-106">IVMHardDiskConnectionCollection::Count property</span></span>

<span data-ttu-id="8370f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8370f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8370f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8370f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8370f-109">Recupera o número de conexões de disco rígido nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="8370f-109">Retrieves the number of hard disk connections in this collection.</span></span>

<span data-ttu-id="8370f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8370f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8370f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8370f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="8370f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8370f-112">Property value</span></span>

<span data-ttu-id="8370f-113">O número de conexões de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="8370f-113">The number of hard disk connections.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8370f-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8370f-114">Error codes</span></span>



| <span data-ttu-id="8370f-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="8370f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8370f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8370f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8370f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8370f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8370f-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8370f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="8370f-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="8370f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8370f-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8370f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="8370f-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8370f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="8370f-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="8370f-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="8370f-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="8370f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8370f-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8370f-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8370f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8370f-125">Requirements</span></span>



| <span data-ttu-id="8370f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8370f-126">Requirement</span></span> | <span data-ttu-id="8370f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8370f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8370f-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8370f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8370f-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8370f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="8370f-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8370f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8370f-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8370f-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="8370f-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8370f-132">End of client support</span></span><br/>    | <span data-ttu-id="8370f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8370f-133">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="8370f-134">Produto</span><span class="sxs-lookup"><span data-stu-id="8370f-134">Product</span></span><br/>                  | <span data-ttu-id="8370f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8370f-135">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="8370f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8370f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8370f-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8370f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="8370f-138">IID</span><span class="sxs-lookup"><span data-stu-id="8370f-138">IID</span></span><br/>                      | <span data-ttu-id="8370f-139">IID \_ IVMHardDiskconnectionCollection é definido como b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="8370f-139">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8370f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8370f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8370f-141">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="8370f-141">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

