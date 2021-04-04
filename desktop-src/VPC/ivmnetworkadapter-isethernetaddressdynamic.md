---
title: Propriedade IVMNetworkAdapter IsEthernetAddressDynamic (VPCCOMInterfaces. h)
description: Determina se o endereço Ethernet é gerado dinamicamente.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- Propriedade IsEthernetAddressDynamic Virtual PC
- Propriedade IsEthernetAddressDynamic Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, Propriedade IsEthernetAddressDynamic
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008808"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a><span data-ttu-id="882fd-106">Propriedade IVMNetworkAdapter:: IsEthernetAddressDynamic</span><span class="sxs-lookup"><span data-stu-id="882fd-106">IVMNetworkAdapter::IsEthernetAddressDynamic property</span></span>

<span data-ttu-id="882fd-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="882fd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="882fd-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="882fd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="882fd-109">Determina se o endereço Ethernet é gerado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="882fd-109">Determines whether the Ethernet address is dynamically generated.</span></span>

<span data-ttu-id="882fd-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="882fd-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="882fd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="882fd-111">Syntax</span></span>


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a><span data-ttu-id="882fd-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="882fd-112">Property value</span></span>

<span data-ttu-id="882fd-113">Defina como VARIANT \_ true se o endereço Ethernet deve ser gerado dinamicamente e Variant \_ false se o endereço Ethernet for estático.</span><span class="sxs-lookup"><span data-stu-id="882fd-113">Set to VARIANT\_TRUE if the Ethernet address should be dynamically generated and VARIANT\_FALSE if the Ethernet address is static.</span></span>

## <a name="error-codes"></a><span data-ttu-id="882fd-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="882fd-114">Error codes</span></span>



| <span data-ttu-id="882fd-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="882fd-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="882fd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="882fd-116">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="882fd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="882fd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="882fd-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="882fd-118">The operation was successful.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="882fd-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="882fd-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="882fd-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="882fd-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="882fd-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="882fd-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="882fd-122">A máquina virtual não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="882fd-122">The virtual machine was not found.</span></span> <span data-ttu-id="882fd-123">Isso poderá ocorrer se o computador tiver sido removido após a criação do objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="882fd-123">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/> |
| <dl> <span data-ttu-id="882fd-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="882fd-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="882fd-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="882fd-125">An unexpected error has occurred.</span></span><br/>                                                                                                                         |



## <a name="remarks"></a><span data-ttu-id="882fd-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="882fd-126">Remarks</span></span>

<span data-ttu-id="882fd-127">Essa propriedade deve ser definida como **true** (padrão) para a maioria das interfaces de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="882fd-127">This property should be set to **TRUE** (default) for most virtual network interfaces.</span></span> <span data-ttu-id="882fd-128">Se o software no convidado exigir um endereço Ethernet estático, essa propriedade deverá ser definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="882fd-128">If software in the guest requires a static Ethernet address, this property should be set to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="882fd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="882fd-129">Requirements</span></span>



| <span data-ttu-id="882fd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="882fd-130">Requirement</span></span> | <span data-ttu-id="882fd-131">Valor</span><span class="sxs-lookup"><span data-stu-id="882fd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="882fd-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="882fd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="882fd-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="882fd-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="882fd-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="882fd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="882fd-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="882fd-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="882fd-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="882fd-136">End of client support</span></span><br/>    | <span data-ttu-id="882fd-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="882fd-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="882fd-138">Produto</span><span class="sxs-lookup"><span data-stu-id="882fd-138">Product</span></span><br/>                  | <span data-ttu-id="882fd-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="882fd-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="882fd-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="882fd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="882fd-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="882fd-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="882fd-142">IID</span><span class="sxs-lookup"><span data-stu-id="882fd-142">IID</span></span><br/>                      | <span data-ttu-id="882fd-143">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="882fd-143">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="882fd-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="882fd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882fd-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="882fd-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

