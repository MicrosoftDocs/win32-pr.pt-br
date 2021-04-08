---
title: Propriedade IMsRdpDevice DeviceInstanceId
description: Recupera o identificador da instância de dispositivo do dispositivo.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceInstanceId
- Propriedade DeviceInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpDevice
- Serviços de Área de Trabalho Remota de interface IMsRdpDevice, Propriedade DeviceInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919204"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a><span data-ttu-id="5b9d8-106">IMsRdpDevice: Propriedade eviceInstanceId de:D</span><span class="sxs-lookup"><span data-stu-id="5b9d8-106">IMsRdpDevice::DeviceInstanceId property</span></span>

<span data-ttu-id="5b9d8-107">Recupera o identificador da instância de dispositivo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b9d8-107">Retrieves the device instance identifier of the device.</span></span>

<span data-ttu-id="5b9d8-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5b9d8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b9d8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b9d8-109">Syntax</span></span>


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a><span data-ttu-id="5b9d8-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5b9d8-110">Property value</span></span>

<span data-ttu-id="5b9d8-111">O identificador da instância do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b9d8-111">The device instance identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5b9d8-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5b9d8-112">Error codes</span></span>

<span data-ttu-id="5b9d8-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="5b9d8-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="5b9d8-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="5b9d8-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b9d8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b9d8-115">Requirements</span></span>



| <span data-ttu-id="5b9d8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b9d8-116">Requirement</span></span> | <span data-ttu-id="5b9d8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5b9d8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b9d8-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b9d8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5b9d8-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b9d8-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5b9d8-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b9d8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5b9d8-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b9d8-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5b9d8-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5b9d8-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b9d8-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b9d8-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b9d8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5b9d8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b9d8-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b9d8-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b9d8-126">IID</span><span class="sxs-lookup"><span data-stu-id="5b9d8-126">IID</span></span><br/>                      | <span data-ttu-id="5b9d8-127">IID \_ IMsRdpDevice é definido como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="5b9d8-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="5b9d8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b9d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b9d8-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="5b9d8-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





