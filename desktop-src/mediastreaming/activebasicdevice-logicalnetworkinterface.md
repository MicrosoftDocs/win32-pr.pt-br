---
title: Propriedade ActiveBasicDevice LogicalNetworkInterface (PlayToDevice. h)
description: Obtém a ID da interface de rede lógica.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- API de streaming de mídia de propriedade LogicalNetworkInterface
- API de streaming de mídia de propriedade LogicalNetworkInterface, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade LogicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369541"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a><span data-ttu-id="3bfe6-106">Propriedade ActiveBasicDevice:: LogicalNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3bfe6-106">ActiveBasicDevice::LogicalNetworkInterface property</span></span>

<span data-ttu-id="3bfe6-107">Obtém a ID da interface de rede lógica.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-107">Gets the id of the logical network interface.</span></span>

<span data-ttu-id="3bfe6-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bfe6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bfe6-109">Syntax</span></span>


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="3bfe6-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3bfe6-110">Property value</span></span>

<span data-ttu-id="3bfe6-111">Um ponteiro para um **GUID** que especifica a ID da interface de rede lógica.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-111">A pointer to a **GUID** that specifies the id of the logical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bfe6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bfe6-112">Requirements</span></span>



| <span data-ttu-id="3bfe6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bfe6-113">Requirement</span></span> | <span data-ttu-id="3bfe6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3bfe6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bfe6-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bfe6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3bfe6-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3bfe6-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3bfe6-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bfe6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3bfe6-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="3bfe6-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3bfe6-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bfe6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bfe6-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bfe6-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="3bfe6-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="3bfe6-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3bfe6-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3bfe6-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="3bfe6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3bfe6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bfe6-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bfe6-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bfe6-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3bfe6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3bfe6-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3bfe6-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

