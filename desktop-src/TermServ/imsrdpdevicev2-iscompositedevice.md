---
title: Propriedade IMsRdpDeviceV2 IsCompositeDevice
description: Especifica se o dispositivo é um dispositivo composto.
ms.assetid: cc54f3f0-de0b-4f75-b5a1-4f061ac95ab5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade IsCompositeDevice
- Propriedade IsCompositeDevice Serviços de Área de Trabalho Remota, interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2, Propriedade IsCompositeDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsCompositeDevice
- IMsRdpDeviceV2.get_IsCompositeDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2341544543f436272486a839ffdd3ee68a4a4478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454647"
---
# <a name="imsrdpdevicev2iscompositedevice-property"></a><span data-ttu-id="566e4-106">Propriedade IMsRdpDeviceV2:: IsCompositeDevice</span><span class="sxs-lookup"><span data-stu-id="566e4-106">IMsRdpDeviceV2::IsCompositeDevice property</span></span>

<span data-ttu-id="566e4-107">Especifica se o dispositivo é um dispositivo composto.</span><span class="sxs-lookup"><span data-stu-id="566e4-107">Specifies if the device is a composite device.</span></span>

<span data-ttu-id="566e4-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="566e4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="566e4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="566e4-109">Syntax</span></span>


```C++
HRESULT get_IsCompositeDevice(
  [out, retval] VARIANT_BOOL *pvboolCompositeDevice
);
```



## <a name="property-value"></a><span data-ttu-id="566e4-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="566e4-110">Property value</span></span>

<span data-ttu-id="566e4-111">**true** se o dispositivo for um dispositivo composto; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="566e4-111">**true** if the device is a composite device; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="566e4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="566e4-112">Requirements</span></span>



| <span data-ttu-id="566e4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="566e4-113">Requirement</span></span> | <span data-ttu-id="566e4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="566e4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="566e4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="566e4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="566e4-116">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="566e4-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="566e4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="566e4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="566e4-118">Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="566e4-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="566e4-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="566e4-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="566e4-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="566e4-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="566e4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="566e4-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="566e4-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="566e4-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="566e4-123">IID</span><span class="sxs-lookup"><span data-stu-id="566e4-123">IID</span></span><br/>                      | <span data-ttu-id="566e4-124">IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="566e4-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="566e4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="566e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="566e4-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="566e4-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





