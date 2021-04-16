---
title: Propriedade ActiveBasicDevice IsMuteSupported (PlayToDevice. h)
description: Obtém um valor que indica se o dispositivo dá suporte a mudo do áudio.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- API de streaming de mídia de propriedade IsMuteSupported
- API de streaming de mídia de propriedade IsMuteSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsMuteSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455364"
---
# <a name="activebasicdeviceismutesupported-property"></a><span data-ttu-id="1eb23-106">Propriedade ActiveBasicDevice:: IsMuteSupported</span><span class="sxs-lookup"><span data-stu-id="1eb23-106">ActiveBasicDevice::IsMuteSupported property</span></span>

<span data-ttu-id="1eb23-107">Obtém um valor que indica se o dispositivo dá suporte a mudo do áudio.</span><span class="sxs-lookup"><span data-stu-id="1eb23-107">Gets a value that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="1eb23-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1eb23-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb23-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1eb23-109">Syntax</span></span>


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="1eb23-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1eb23-110">Property value</span></span>

<span data-ttu-id="1eb23-111">Um ponteiro para um **booliano** que indica se o dispositivo dá suporte a mudo do áudio.</span><span class="sxs-lookup"><span data-stu-id="1eb23-111">A pointer to a **boolean** that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="1eb23-112">**true** se o dispositivo der suporte a mudo do áudio; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1eb23-112">**true** if the device supports muting the audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb23-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1eb23-113">Requirements</span></span>



| <span data-ttu-id="1eb23-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eb23-114">Requirement</span></span> | <span data-ttu-id="1eb23-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1eb23-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb23-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1eb23-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb23-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1eb23-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1eb23-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1eb23-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb23-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="1eb23-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1eb23-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1eb23-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eb23-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eb23-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="1eb23-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="1eb23-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1eb23-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1eb23-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="1eb23-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1eb23-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eb23-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eb23-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb23-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1eb23-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1eb23-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1eb23-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

