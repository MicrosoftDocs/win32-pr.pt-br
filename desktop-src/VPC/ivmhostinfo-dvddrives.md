---
title: Propriedade IVMHostInfo DVDDrives (VPCCOMInterfaces. h)
description: Recupera as letras da unidade associadas aos dispositivos de CD e DVD do host.
ms.assetid: 17f01d00-2c02-48f0-bfe9-0326a40fdf55
keywords:
- Propriedade DVDDrives Virtual PC
- Propriedade DVDDrives Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade DVDDrives
topic_type:
- apiref
api_name:
- IVMHostInfo.DVDDrives
- IVMHostInfo.get_DVDDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb9380773934b63ae637d32ec5acfef5112f2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369603"
---
# <a name="ivmhostinfodvddrives-property"></a><span data-ttu-id="04132-106">IVMHostInfo: Propriedade VDDrives de:D</span><span class="sxs-lookup"><span data-stu-id="04132-106">IVMHostInfo::DVDDrives property</span></span>

<span data-ttu-id="04132-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="04132-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="04132-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04132-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="04132-109">Recupera as letras da unidade associadas aos dispositivos de CD e DVD do host.</span><span class="sxs-lookup"><span data-stu-id="04132-109">Retrieves the drive letters associated with host CD and DVD devices.</span></span>

<span data-ttu-id="04132-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="04132-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04132-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04132-111">Syntax</span></span>


```C++
HRESULT get_DVDDrives(
  [out, retval] VARIANT *DVDDrives
);
```



## <a name="property-value"></a><span data-ttu-id="04132-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="04132-112">Property value</span></span>

<span data-ttu-id="04132-113">Uma matriz de letras de unidade.</span><span class="sxs-lookup"><span data-stu-id="04132-113">An array of drive letters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="04132-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="04132-114">Error codes</span></span>



| <span data-ttu-id="04132-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="04132-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="04132-116">Significado</span><span class="sxs-lookup"><span data-stu-id="04132-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="04132-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04132-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="04132-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="04132-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="04132-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="04132-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="04132-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04132-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="04132-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="04132-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="04132-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="04132-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="04132-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04132-123">Requirements</span></span>



| <span data-ttu-id="04132-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="04132-124">Requirement</span></span> | <span data-ttu-id="04132-125">Valor</span><span class="sxs-lookup"><span data-stu-id="04132-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="04132-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04132-126">Minimum supported client</span></span><br/> | <span data-ttu-id="04132-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="04132-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04132-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04132-128">Minimum supported server</span></span><br/> | <span data-ttu-id="04132-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="04132-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="04132-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="04132-130">End of client support</span></span><br/>    | <span data-ttu-id="04132-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04132-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="04132-132">Produto</span><span class="sxs-lookup"><span data-stu-id="04132-132">Product</span></span><br/>                  | <span data-ttu-id="04132-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="04132-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="04132-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04132-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="04132-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="04132-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="04132-136">IID</span><span class="sxs-lookup"><span data-stu-id="04132-136">IID</span></span><br/>                      | <span data-ttu-id="04132-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="04132-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="04132-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="04132-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04132-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="04132-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

