---
title: Propriedade de item IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Objeto de disquete que corresponde ao índice especificado.
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMFloppyDriveCollection
- IVMFloppyDriveCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086350"
---
# <a name="ivmfloppydrivecollectionitem-property"></a><span data-ttu-id="7f1c1-106">Propriedade IVMFloppyDriveCollection:: item</span><span class="sxs-lookup"><span data-stu-id="7f1c1-106">IVMFloppyDriveCollection::Item property</span></span>

<span data-ttu-id="7f1c1-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f1c1-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f1c1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f1c1-109">Recupera o objeto de disquete que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-109">Retrieves the floppy object that corresponds to the specified index.</span></span>

<span data-ttu-id="7f1c1-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f1c1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f1c1-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a><span data-ttu-id="7f1c1-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7f1c1-112">Property value</span></span>

<span data-ttu-id="7f1c1-113">O objeto [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="7f1c1-113">The [**IVMFloppyDrive**](ivmfloppydrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f1c1-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7f1c1-114">Error codes</span></span>



| <span data-ttu-id="7f1c1-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="7f1c1-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7f1c1-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7f1c1-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f1c1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f1c1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7f1c1-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="7f1c1-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7f1c1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7f1c1-120">O parâmetro *floppyDrive* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-120">The *floppyDrive* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="7f1c1-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="7f1c1-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="7f1c1-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="7f1c1-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7f1c1-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7f1c1-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-124">The configuration is unknown.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="7f1c1-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="7f1c1-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7f1c1-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="7f1c1-126">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="7f1c1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f1c1-127">Requirements</span></span>



| <span data-ttu-id="7f1c1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f1c1-128">Requirement</span></span> | <span data-ttu-id="7f1c1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7f1c1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1c1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f1c1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7f1c1-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f1c1-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f1c1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f1c1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7f1c1-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7f1c1-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f1c1-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7f1c1-134">End of client support</span></span><br/>    | <span data-ttu-id="7f1c1-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f1c1-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f1c1-136">Produto</span><span class="sxs-lookup"><span data-stu-id="7f1c1-136">Product</span></span><br/>                  | <span data-ttu-id="7f1c1-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f1c1-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f1c1-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f1c1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f1c1-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f1c1-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f1c1-140">IID</span><span class="sxs-lookup"><span data-stu-id="7f1c1-140">IID</span></span><br/>                      | <span data-ttu-id="7f1c1-141">IID \_ IVMFloppyDriveCollection é definido como 8ba70a25-f698-4ee5-85CE-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="7f1c1-141">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7f1c1-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f1c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f1c1-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="7f1c1-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="7f1c1-144">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="7f1c1-144">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

