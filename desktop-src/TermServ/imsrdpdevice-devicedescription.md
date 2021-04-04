---
title: Propriedade IMsRdpDevice DeviceDescription
description: Recupera a descrição do dispositivo a ser exibida para o usuário se o nome para exibição não estiver disponível.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceDescription
- Propriedade DeviceDescription Serviços de Área de Trabalho Remota, interface IMsRdpDevice
- Serviços de Área de Trabalho Remota de interface IMsRdpDevice, Propriedade DeviceDescription
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085867"
---
# <a name="imsrdpdevicedevicedescription-property"></a><span data-ttu-id="43dc0-106">IMsRdpDevice: Propriedade eviceDescription de:D</span><span class="sxs-lookup"><span data-stu-id="43dc0-106">IMsRdpDevice::DeviceDescription property</span></span>

<span data-ttu-id="43dc0-107">Recupera a descrição do dispositivo a ser exibida para o usuário se o nome para exibição não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="43dc0-107">Retrieves the device description to be displayed to the user if the display name is not available.</span></span>

<span data-ttu-id="43dc0-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="43dc0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43dc0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43dc0-109">Syntax</span></span>


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a><span data-ttu-id="43dc0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="43dc0-110">Property value</span></span>

<span data-ttu-id="43dc0-111">A descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43dc0-111">The device description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43dc0-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="43dc0-112">Error codes</span></span>

<span data-ttu-id="43dc0-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="43dc0-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="43dc0-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="43dc0-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="43dc0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43dc0-115">Requirements</span></span>



| <span data-ttu-id="43dc0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="43dc0-116">Requirement</span></span> | <span data-ttu-id="43dc0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="43dc0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43dc0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43dc0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43dc0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43dc0-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="43dc0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43dc0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43dc0-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43dc0-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="43dc0-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="43dc0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="43dc0-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43dc0-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="43dc0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="43dc0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43dc0-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43dc0-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="43dc0-126">IID</span><span class="sxs-lookup"><span data-stu-id="43dc0-126">IID</span></span><br/>                      | <span data-ttu-id="43dc0-127">IID \_ IMsRdpDevice é definido como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="43dc0-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="43dc0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="43dc0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43dc0-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="43dc0-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





