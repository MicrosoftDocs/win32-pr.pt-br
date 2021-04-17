---
title: Método IMsRdpDeviceCollection RescanDevices
description: Atualiza a lista de objetos na coleção. | Método IMsRdpDeviceCollection RescanDevices
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RescanDevices
- Método RescanDevices Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection, método RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105768548"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a><span data-ttu-id="30aec-107">Método IMsRdpDeviceCollection:: RescanDevices</span><span class="sxs-lookup"><span data-stu-id="30aec-107">IMsRdpDeviceCollection::RescanDevices method</span></span>

<span data-ttu-id="30aec-108">Atualiza a lista de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="30aec-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="30aec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30aec-109">Syntax</span></span>


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="30aec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30aec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30aec-111">*vboolDynRedir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30aec-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30aec-112">O estado de redirecionamento padrão que será aplicado a quaisquer unidades ou dispositivos descobertos recentemente.</span><span class="sxs-lookup"><span data-stu-id="30aec-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30aec-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30aec-113">Return value</span></span>

<span data-ttu-id="30aec-114">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="30aec-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="30aec-115">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="30aec-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="30aec-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30aec-116">Requirements</span></span>



| <span data-ttu-id="30aec-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="30aec-117">Requirement</span></span> | <span data-ttu-id="30aec-118">Valor</span><span class="sxs-lookup"><span data-stu-id="30aec-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30aec-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30aec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30aec-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30aec-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="30aec-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30aec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30aec-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30aec-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="30aec-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="30aec-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="30aec-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30aec-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="30aec-125">DLL</span><span class="sxs-lookup"><span data-stu-id="30aec-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30aec-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30aec-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="30aec-127">IID</span><span class="sxs-lookup"><span data-stu-id="30aec-127">IID</span></span><br/>                      | <span data-ttu-id="30aec-128">IID \_ IMsRdpDeviceCollection é definido como 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="30aec-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30aec-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="30aec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30aec-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="30aec-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





