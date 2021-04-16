---
title: Propriedade IMsRdpDeviceV2 CmDeviceInstance
description: Contém a instância de dispositivo do Configuration Manager do dispositivo.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CmDeviceInstance
- Propriedade CmDeviceInstance Serviços de Área de Trabalho Remota, interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2, Propriedade CmDeviceInstance
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758095"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a><span data-ttu-id="19d11-106">Propriedade IMsRdpDeviceV2:: CmDeviceInstance</span><span class="sxs-lookup"><span data-stu-id="19d11-106">IMsRdpDeviceV2::CmDeviceInstance property</span></span>

<span data-ttu-id="19d11-107">Contém a instância de dispositivo do Configuration Manager do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19d11-107">Contains the configuration manager device instance of the device.</span></span>

<span data-ttu-id="19d11-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="19d11-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d11-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19d11-109">Syntax</span></span>


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a><span data-ttu-id="19d11-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="19d11-110">Property value</span></span>

<span data-ttu-id="19d11-111">A instância de dispositivo do Configuration Manager do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19d11-111">The configuration manager device instance of the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="19d11-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19d11-112">Requirements</span></span>



| <span data-ttu-id="19d11-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="19d11-113">Requirement</span></span> | <span data-ttu-id="19d11-114">Valor</span><span class="sxs-lookup"><span data-stu-id="19d11-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19d11-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19d11-115">Minimum supported client</span></span><br/> | <span data-ttu-id="19d11-116">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="19d11-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="19d11-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19d11-117">Minimum supported server</span></span><br/> | <span data-ttu-id="19d11-118">Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="19d11-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="19d11-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="19d11-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="19d11-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d11-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="19d11-121">DLL</span><span class="sxs-lookup"><span data-stu-id="19d11-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19d11-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d11-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="19d11-123">IID</span><span class="sxs-lookup"><span data-stu-id="19d11-123">IID</span></span><br/>                      | <span data-ttu-id="19d11-124">IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="19d11-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="19d11-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="19d11-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d11-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="19d11-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





