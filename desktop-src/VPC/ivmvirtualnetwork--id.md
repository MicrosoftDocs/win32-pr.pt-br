---
title: Método de _ID IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera o identificador interno da rede virtual.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID o método virtual PC
- _ID método virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface virtual PC, método de _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009667"
---
# <a name="ivmvirtualnetwork_id-method"></a><span data-ttu-id="014d4-106">Método IVMVirtualNetwork:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="014d4-106">IVMVirtualNetwork::\_ID method</span></span>

<span data-ttu-id="014d4-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="014d4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="014d4-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="014d4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="014d4-109">Recupera o identificador interno da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="014d4-109">Retrieves the internal identifier of the virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="014d4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="014d4-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a><span data-ttu-id="014d4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="014d4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="014d4-112">*virtualNetworkID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="014d4-112">*virtualNetworkID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="014d4-113">O identificador da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="014d4-113">The virtual network identifier.</span></span> <span data-ttu-id="014d4-114">O identificador para a rede virtual de rede compartilhada (NAT) é 01010101010101010101010101010101.</span><span class="sxs-lookup"><span data-stu-id="014d4-114">The identifier for the Shared Networking (NAT) virtual network is 01010101010101010101010101010101.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="014d4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="014d4-115">Return value</span></span>

<span data-ttu-id="014d4-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="014d4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="014d4-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="014d4-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="014d4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="014d4-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="014d4-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="014d4-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="014d4-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="014d4-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="014d4-121"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="014d4-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="014d4-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="014d4-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="014d4-123"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="014d4-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="014d4-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="014d4-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="014d4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="014d4-125">Remarks</span></span>

<span data-ttu-id="014d4-126">Essa propriedade não pode ser usada por linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="014d4-126">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="014d4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="014d4-127">Requirements</span></span>



| <span data-ttu-id="014d4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="014d4-128">Requirement</span></span> | <span data-ttu-id="014d4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="014d4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="014d4-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="014d4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="014d4-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="014d4-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="014d4-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="014d4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="014d4-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="014d4-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="014d4-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="014d4-134">End of client support</span></span><br/>    | <span data-ttu-id="014d4-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="014d4-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="014d4-136">Produto</span><span class="sxs-lookup"><span data-stu-id="014d4-136">Product</span></span><br/>                  | <span data-ttu-id="014d4-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="014d4-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="014d4-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="014d4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="014d4-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="014d4-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="014d4-140">IID</span><span class="sxs-lookup"><span data-stu-id="014d4-140">IID</span></span><br/>                      | <span data-ttu-id="014d4-141">IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="014d4-141">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="014d4-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="014d4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014d4-143">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="014d4-143">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

