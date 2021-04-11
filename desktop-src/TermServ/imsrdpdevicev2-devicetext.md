---
title: Propriedade IMsRdpDeviceV2 DeviceText
description: Contém o texto do dispositivo.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceText
- Propriedade DeviceText Serviços de Área de Trabalho Remota, interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2, Propriedade DeviceText
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163583"
---
# <a name="imsrdpdevicev2devicetext-property"></a><span data-ttu-id="f437f-106">IMsRdpDeviceV2: Propriedade eviceText de:D</span><span class="sxs-lookup"><span data-stu-id="f437f-106">IMsRdpDeviceV2::DeviceText property</span></span>

<span data-ttu-id="f437f-107">Contém o texto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f437f-107">Contains the device text.</span></span> <span data-ttu-id="f437f-108">Esse é o nome que o Windows exibe para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f437f-108">This is the name that Windows displays to the user.</span></span>

<span data-ttu-id="f437f-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f437f-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f437f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f437f-110">Syntax</span></span>


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a><span data-ttu-id="f437f-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f437f-111">Property value</span></span>

<span data-ttu-id="f437f-112">O nome para exibição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f437f-112">The display name for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f437f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f437f-113">Requirements</span></span>



| <span data-ttu-id="f437f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f437f-114">Requirement</span></span> | <span data-ttu-id="f437f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f437f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f437f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f437f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f437f-117">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="f437f-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="f437f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f437f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f437f-119">Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="f437f-119">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="f437f-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f437f-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f437f-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f437f-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f437f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f437f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f437f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f437f-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f437f-124">IID</span><span class="sxs-lookup"><span data-stu-id="f437f-124">IID</span></span><br/>                      | <span data-ttu-id="f437f-125">IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="f437f-125">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="f437f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f437f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f437f-127">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="f437f-127">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





