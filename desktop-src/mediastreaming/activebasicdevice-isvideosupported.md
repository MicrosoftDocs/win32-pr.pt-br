---
title: Propriedade ActiveBasicDevice IsVideoSupported (PlayToDevice. h)
description: Obtém um valor que indica se o dispositivo dá suporte a vídeo.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- API de streaming de mídia de propriedade IsVideoSupported
- API de streaming de mídia de propriedade IsVideoSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsVideoSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766467"
---
# <a name="activebasicdeviceisvideosupported-property"></a><span data-ttu-id="50ca2-106">Propriedade ActiveBasicDevice:: IsVideoSupported</span><span class="sxs-lookup"><span data-stu-id="50ca2-106">ActiveBasicDevice::IsVideoSupported property</span></span>

<span data-ttu-id="50ca2-107">Obtém um valor que indica se o dispositivo dá suporte a vídeo.</span><span class="sxs-lookup"><span data-stu-id="50ca2-107">Gets a value that indicates if the device supports video.</span></span>

<span data-ttu-id="50ca2-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="50ca2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ca2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50ca2-109">Syntax</span></span>


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="50ca2-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="50ca2-110">Property value</span></span>

<span data-ttu-id="50ca2-111">Um ponteiro para um **booliano** que indica se o dispositivo dá suporte a vídeo.</span><span class="sxs-lookup"><span data-stu-id="50ca2-111">A pointer to a **boolean** that indicates if the device supports video.</span></span>

<span data-ttu-id="50ca2-112">**true** se o dispositivo der suporte a vídeo; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="50ca2-112">**true** if the device supports video; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ca2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50ca2-113">Requirements</span></span>



| <span data-ttu-id="50ca2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50ca2-114">Requirement</span></span> | <span data-ttu-id="50ca2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="50ca2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ca2-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50ca2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50ca2-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50ca2-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="50ca2-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50ca2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50ca2-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="50ca2-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="50ca2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50ca2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="50ca2-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="50ca2-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="50ca2-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="50ca2-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50ca2-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50ca2-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="50ca2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="50ca2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50ca2-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50ca2-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50ca2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="50ca2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="50ca2-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50ca2-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

