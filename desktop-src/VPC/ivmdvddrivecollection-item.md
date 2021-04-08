---
title: Propriedade de item IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera o objeto da unidade de CD ou DVD que corresponde ao índice especificado.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009328"
---
# <a name="ivmdvddrivecollectionitem-property"></a><span data-ttu-id="cbfb9-106">Propriedade IVMDVDDriveCollection:: item</span><span class="sxs-lookup"><span data-stu-id="cbfb9-106">IVMDVDDriveCollection::Item property</span></span>

<span data-ttu-id="cbfb9-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cbfb9-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cbfb9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cbfb9-109">Recupera o objeto da unidade de CD ou DVD que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-109">Retrieves the CD or DVD drive object that corresponds to the specified index.</span></span>

<span data-ttu-id="cbfb9-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfb9-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbfb9-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a><span data-ttu-id="cbfb9-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cbfb9-112">Property value</span></span>

<span data-ttu-id="cbfb9-113">O objeto [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb9-113">The [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbfb9-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="cbfb9-114">Error codes</span></span>



| <span data-ttu-id="cbfb9-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="cbfb9-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cbfb9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="cbfb9-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbfb9-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cbfb9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cbfb9-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="cbfb9-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="cbfb9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cbfb9-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-120">The parameter is **NULL**.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="cbfb9-121"><dt>E \_ FALHA</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="cbfb9-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="cbfb9-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-122">An unexpected error has occurred.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="cbfb9-123"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="cbfb9-123"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="cbfb9-124">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-124">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="cbfb9-125"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cbfb9-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="cbfb9-126">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-126">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="cbfb9-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="cbfb9-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cbfb9-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-128">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="cbfb9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbfb9-129">Requirements</span></span>



| <span data-ttu-id="cbfb9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbfb9-130">Requirement</span></span> | <span data-ttu-id="cbfb9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="cbfb9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfb9-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbfb9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cbfb9-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cbfb9-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbfb9-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbfb9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cbfb9-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cbfb9-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cbfb9-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cbfb9-136">End of client support</span></span><br/>    | <span data-ttu-id="cbfb9-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbfb9-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cbfb9-138">Produto</span><span class="sxs-lookup"><span data-stu-id="cbfb9-138">Product</span></span><br/>                  | <span data-ttu-id="cbfb9-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cbfb9-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cbfb9-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbfb9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbfb9-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbfb9-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cbfb9-142">IID</span><span class="sxs-lookup"><span data-stu-id="cbfb9-142">IID</span></span><br/>                      | <span data-ttu-id="cbfb9-143">IID \_ IVMDVDDriveCollection é definido como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="cbfb9-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="cbfb9-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbfb9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfb9-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="cbfb9-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="cbfb9-146">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="cbfb9-146">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

