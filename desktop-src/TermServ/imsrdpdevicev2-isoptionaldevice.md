---
title: Propriedade IMsRdpDeviceV2 IsOptionalDevice
description: Especifica se o dispositivo é opcional para o redirecionamento de USB.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade IsOptionalDevice
- Propriedade IsOptionalDevice Serviços de Área de Trabalho Remota, interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2, Propriedade IsOptionalDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455488"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a><span data-ttu-id="7c659-106">Propriedade IMsRdpDeviceV2:: IsOptionalDevice</span><span class="sxs-lookup"><span data-stu-id="7c659-106">IMsRdpDeviceV2::IsOptionalDevice property</span></span>

<span data-ttu-id="7c659-107">Especifica se o dispositivo é opcional para o redirecionamento de USB.</span><span class="sxs-lookup"><span data-stu-id="7c659-107">Specifies if the device is optional for USB redirection.</span></span>

<span data-ttu-id="7c659-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7c659-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c659-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c659-109">Syntax</span></span>


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a><span data-ttu-id="7c659-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7c659-110">Property value</span></span>

<span data-ttu-id="7c659-111">**true** se o dispositivo for opcional; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7c659-111">**true** if the device is a optional; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c659-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c659-112">Requirements</span></span>



| <span data-ttu-id="7c659-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c659-113">Requirement</span></span> | <span data-ttu-id="7c659-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7c659-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c659-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c659-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7c659-116">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="7c659-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="7c659-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c659-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7c659-118">Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="7c659-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="7c659-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7c659-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c659-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c659-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c659-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7c659-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c659-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c659-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c659-123">IID</span><span class="sxs-lookup"><span data-stu-id="7c659-123">IID</span></span><br/>                      | <span data-ttu-id="7c659-124">IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="7c659-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="7c659-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c659-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c659-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="7c659-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





