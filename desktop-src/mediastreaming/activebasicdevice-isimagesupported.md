---
title: Propriedade ActiveBasicDevice IsImageSupported (PlayToDevice. h)
description: Obtém um valor que indica se o dispositivo dá suporte a imagens.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- API de streaming de mídia de propriedade IsImageSupported
- API de streaming de mídia de propriedade IsImageSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsImageSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e90f51d2dd59ffec8221787b9ee7c247536abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105797524"
---
# <a name="activebasicdeviceisimagesupported-property"></a><span data-ttu-id="f2db5-106">Propriedade ActiveBasicDevice:: IsImageSupported</span><span class="sxs-lookup"><span data-stu-id="f2db5-106">ActiveBasicDevice::IsImageSupported property</span></span>

<span data-ttu-id="f2db5-107">Obtém um valor que indica se o dispositivo dá suporte a imagens.</span><span class="sxs-lookup"><span data-stu-id="f2db5-107">Gets a value that indicates if the device supports images.</span></span>

<span data-ttu-id="f2db5-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f2db5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2db5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2db5-109">Syntax</span></span>


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="f2db5-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f2db5-110">Property value</span></span>

<span data-ttu-id="f2db5-111">Um ponteiro para um **booliano** que indica se o dispositivo dá suporte a imagens.</span><span class="sxs-lookup"><span data-stu-id="f2db5-111">A pointer to a **boolean** that indicates if the device supports images.</span></span>

<span data-ttu-id="f2db5-112">**true** se o dispositivo der suporte a imagens; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f2db5-112">**true** if the device supports images; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2db5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2db5-113">Requirements</span></span>



| <span data-ttu-id="f2db5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2db5-114">Requirement</span></span> | <span data-ttu-id="f2db5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f2db5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2db5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2db5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2db5-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2db5-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f2db5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2db5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2db5-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="f2db5-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f2db5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2db5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2db5-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2db5-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2db5-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="f2db5-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2db5-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2db5-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="f2db5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f2db5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2db5-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2db5-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2db5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2db5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2db5-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2db5-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

