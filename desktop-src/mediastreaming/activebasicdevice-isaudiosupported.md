---
title: Propriedade ActiveBasicDevice IsAudioSupported (PlayToDevice. h)
description: Obtém um valor que indica se o dispositivo dá suporte a áudio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- API de streaming de mídia de propriedade IsAudioSupported
- API de streaming de mídia de propriedade IsAudioSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009743"
---
# <a name="activebasicdeviceisaudiosupported-property"></a><span data-ttu-id="89e2e-106">Propriedade ActiveBasicDevice:: IsAudioSupported</span><span class="sxs-lookup"><span data-stu-id="89e2e-106">ActiveBasicDevice::IsAudioSupported property</span></span>

<span data-ttu-id="89e2e-107">Obtém um valor que indica se o dispositivo dá suporte a áudio.</span><span class="sxs-lookup"><span data-stu-id="89e2e-107">Gets a value that indicates if the device supports audio.</span></span>

<span data-ttu-id="89e2e-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="89e2e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e2e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89e2e-109">Syntax</span></span>


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="89e2e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="89e2e-110">Property value</span></span>

<span data-ttu-id="89e2e-111">Um ponteiro para um **booliano** que indica se o dispositivo dá suporte a áudio.</span><span class="sxs-lookup"><span data-stu-id="89e2e-111">A pointer to a **boolean** that indicates if the device supports audio.</span></span>

<span data-ttu-id="89e2e-112">**true** se o dispositivo der suporte a áudio; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="89e2e-112">**true** if the device supports audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="89e2e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89e2e-113">Requirements</span></span>



| <span data-ttu-id="89e2e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e2e-114">Requirement</span></span> | <span data-ttu-id="89e2e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="89e2e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="89e2e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e2e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="89e2e-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89e2e-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89e2e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e2e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="89e2e-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="89e2e-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="89e2e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89e2e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="89e2e-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="89e2e-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="89e2e-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="89e2e-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89e2e-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="89e2e-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="89e2e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="89e2e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89e2e-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89e2e-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89e2e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="89e2e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="89e2e-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="89e2e-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

