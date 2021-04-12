---
title: Propriedade ActiveBasicDevice PhysicalNetworkInterface (PlayToDevice. h)
description: Obtém a ID da interface de rede física.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API de streaming de mídia de propriedade PhysicalNetworkInterface
- API de streaming de mídia de propriedade PhysicalNetworkInterface, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade PhysicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455363"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a><span data-ttu-id="66bfa-106">ActiveBasicDevice: Propriedade hysicalNetworkInterface de:P</span><span class="sxs-lookup"><span data-stu-id="66bfa-106">ActiveBasicDevice::PhysicalNetworkInterface property</span></span>

<span data-ttu-id="66bfa-107">Obtém a ID da interface de rede física.</span><span class="sxs-lookup"><span data-stu-id="66bfa-107">Gets the id of the physical network interface.</span></span>

<span data-ttu-id="66bfa-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="66bfa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66bfa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66bfa-109">Syntax</span></span>


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="66bfa-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="66bfa-110">Property value</span></span>

<span data-ttu-id="66bfa-111">Um ponteiro para um **GUID** que especifica a ID da interface de rede física.</span><span class="sxs-lookup"><span data-stu-id="66bfa-111">A pointer to a **GUID** that specifies the id of the physical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="66bfa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66bfa-112">Requirements</span></span>



| <span data-ttu-id="66bfa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="66bfa-113">Requirement</span></span> | <span data-ttu-id="66bfa-114">Valor</span><span class="sxs-lookup"><span data-stu-id="66bfa-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bfa-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66bfa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="66bfa-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66bfa-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66bfa-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66bfa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="66bfa-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="66bfa-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66bfa-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66bfa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="66bfa-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="66bfa-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="66bfa-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="66bfa-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66bfa-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66bfa-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="66bfa-123">DLL</span><span class="sxs-lookup"><span data-stu-id="66bfa-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66bfa-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66bfa-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66bfa-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="66bfa-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="66bfa-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="66bfa-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

