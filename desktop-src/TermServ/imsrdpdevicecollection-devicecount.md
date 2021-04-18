---
title: Propriedade IMsRdpDeviceCollection DeviceCount
description: Recupera a contagem de objetos na coleção. | Propriedade IMsRdpDeviceCollection DeviceCount
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceCount
- Propriedade DeviceCount Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection, Propriedade DeviceCount
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a389cd89699eb383b9f235858f0cf4a052606a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105761801"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a><span data-ttu-id="c74b6-107">IMsRdpDeviceCollection: Propriedade eviceCount de:D</span><span class="sxs-lookup"><span data-stu-id="c74b6-107">IMsRdpDeviceCollection::DeviceCount property</span></span>

<span data-ttu-id="c74b6-108">Recupera a contagem de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="c74b6-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="c74b6-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c74b6-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c74b6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c74b6-110">Syntax</span></span>


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a><span data-ttu-id="c74b6-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c74b6-111">Property value</span></span>

<span data-ttu-id="c74b6-112">A contagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="c74b6-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c74b6-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c74b6-113">Error codes</span></span>

<span data-ttu-id="c74b6-114">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="c74b6-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="c74b6-115">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="c74b6-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c74b6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c74b6-116">Requirements</span></span>



| <span data-ttu-id="c74b6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c74b6-117">Requirement</span></span> | <span data-ttu-id="c74b6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c74b6-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c74b6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c74b6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c74b6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c74b6-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c74b6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c74b6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c74b6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c74b6-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c74b6-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c74b6-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c74b6-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c74b6-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c74b6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c74b6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c74b6-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c74b6-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c74b6-127">IID</span><span class="sxs-lookup"><span data-stu-id="c74b6-127">IID</span></span><br/>                      | <span data-ttu-id="c74b6-128">IID \_ IMsRdpDeviceCollection é definido como 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="c74b6-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c74b6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c74b6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c74b6-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="c74b6-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





