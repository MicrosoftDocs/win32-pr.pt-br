---
title: Propriedade IVMHostInfo OSMajorVersion (VPCCOMInterfaces. h)
description: Recupera a versão principal do sistema operacional em execução no computador host.
ms.assetid: d0b62d2d-532f-45c7-8622-67176b9b4a8f
keywords:
- Propriedade OSMajorVersion Virtual PC
- Propriedade OSMajorVersion Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade OSMajorVersion
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMajorVersion
- IVMHostInfo.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf064744d90ede010a7e48e0e23e6a62a19eb4af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369194"
---
# <a name="ivmhostinfoosmajorversion-property"></a><span data-ttu-id="eee6b-106">Propriedade IVMHostInfo:: OSMajorVersion</span><span class="sxs-lookup"><span data-stu-id="eee6b-106">IVMHostInfo::OSMajorVersion property</span></span>

<span data-ttu-id="eee6b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eee6b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eee6b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eee6b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eee6b-109">Recupera a versão principal do sistema operacional em execução no computador host.</span><span class="sxs-lookup"><span data-stu-id="eee6b-109">Retrieves the major version of the operating system running on the host machine.</span></span>

<span data-ttu-id="eee6b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="eee6b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee6b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eee6b-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] long *osMajorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="eee6b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="eee6b-112">Property value</span></span>

<span data-ttu-id="eee6b-113">A versão principal.</span><span class="sxs-lookup"><span data-stu-id="eee6b-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eee6b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="eee6b-114">Error codes</span></span>



| <span data-ttu-id="eee6b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="eee6b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="eee6b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="eee6b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="eee6b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eee6b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="eee6b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="eee6b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="eee6b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="eee6b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="eee6b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="eee6b-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="eee6b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="eee6b-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="eee6b-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eee6b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eee6b-123">Requirements</span></span>



| <span data-ttu-id="eee6b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eee6b-124">Requirement</span></span> | <span data-ttu-id="eee6b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="eee6b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee6b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eee6b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eee6b-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eee6b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eee6b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eee6b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eee6b-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eee6b-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eee6b-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="eee6b-130">End of client support</span></span><br/>    | <span data-ttu-id="eee6b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eee6b-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eee6b-132">Produto</span><span class="sxs-lookup"><span data-stu-id="eee6b-132">Product</span></span><br/>                  | <span data-ttu-id="eee6b-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eee6b-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eee6b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eee6b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee6b-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee6b-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eee6b-136">IID</span><span class="sxs-lookup"><span data-stu-id="eee6b-136">IID</span></span><br/>                      | <span data-ttu-id="eee6b-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="eee6b-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="eee6b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="eee6b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee6b-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="eee6b-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

