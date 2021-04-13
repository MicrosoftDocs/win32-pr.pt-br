---
title: Propriedade IMsRdpDeviceCollection DeviceByIndex
description: Recupera o dispositivo no índice especificado.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceByIndex
- Propriedade DeviceByIndex Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection, Propriedade DeviceByIndex
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456001"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a><span data-ttu-id="10bae-106">IMsRdpDeviceCollection: Propriedade eviceByIndex de:D</span><span class="sxs-lookup"><span data-stu-id="10bae-106">IMsRdpDeviceCollection::DeviceByIndex property</span></span>

<span data-ttu-id="10bae-107">Recupera o dispositivo no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="10bae-107">Retrieves the device at the specified index.</span></span>

<span data-ttu-id="10bae-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="10bae-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10bae-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10bae-109">Syntax</span></span>


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="10bae-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="10bae-110">Property value</span></span>

<span data-ttu-id="10bae-111">Um ponteiro de interface [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="10bae-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10bae-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="10bae-112">Error codes</span></span>

<span data-ttu-id="10bae-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="10bae-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="10bae-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="10bae-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="10bae-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10bae-115">Requirements</span></span>



| <span data-ttu-id="10bae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="10bae-116">Requirement</span></span> | <span data-ttu-id="10bae-117">Valor</span><span class="sxs-lookup"><span data-stu-id="10bae-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="10bae-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10bae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10bae-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10bae-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="10bae-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10bae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10bae-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10bae-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="10bae-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="10bae-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="10bae-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10bae-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="10bae-124">DLL</span><span class="sxs-lookup"><span data-stu-id="10bae-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10bae-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10bae-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="10bae-126">IID</span><span class="sxs-lookup"><span data-stu-id="10bae-126">IID</span></span><br/>                      | <span data-ttu-id="10bae-127">IID \_ IMsRdpDeviceCollection é definido como 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="10bae-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10bae-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="10bae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bae-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="10bae-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





