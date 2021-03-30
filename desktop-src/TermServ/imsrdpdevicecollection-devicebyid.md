---
title: Propriedade IMsRdpDeviceCollection DeviceById
description: Recupera o dispositivo com o identificador especificado.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceById
- Propriedade DeviceById Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection, Propriedade DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455057"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a><span data-ttu-id="f6d34-106">IMsRdpDeviceCollection: Propriedade eviceById de:D</span><span class="sxs-lookup"><span data-stu-id="f6d34-106">IMsRdpDeviceCollection::DeviceById property</span></span>

<span data-ttu-id="f6d34-107">Recupera o dispositivo com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="f6d34-107">Retrieves the device with the specified identifier.</span></span>

<span data-ttu-id="f6d34-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f6d34-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d34-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6d34-109">Syntax</span></span>


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="f6d34-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f6d34-110">Property value</span></span>

<span data-ttu-id="f6d34-111">Um ponteiro de interface [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d34-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f6d34-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f6d34-112">Error codes</span></span>

<span data-ttu-id="f6d34-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="f6d34-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="f6d34-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="f6d34-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d34-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6d34-115">Requirements</span></span>



| <span data-ttu-id="f6d34-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6d34-116">Requirement</span></span> | <span data-ttu-id="f6d34-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f6d34-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d34-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6d34-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d34-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6d34-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="f6d34-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6d34-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d34-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6d34-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f6d34-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f6d34-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6d34-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6d34-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f6d34-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f6d34-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6d34-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6d34-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f6d34-126">IID</span><span class="sxs-lookup"><span data-stu-id="f6d34-126">IID</span></span><br/>                      | <span data-ttu-id="f6d34-127">IID \_ IMsRdpDeviceCollection é definido como 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="f6d34-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6d34-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f6d34-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d34-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="f6d34-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





