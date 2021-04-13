---
title: Propriedade ActiveBasicDevice IsSearchSupported (PlayToDevice. h)
description: Obtém um valor que indica se o dispositivo dá suporte à pesquisa.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- API de streaming de mídia de propriedade IsSearchSupported
- API de streaming de mídia de propriedade IsSearchSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsSearchSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369890"
---
# <a name="activebasicdeviceissearchsupported-property"></a><span data-ttu-id="359de-106">Propriedade ActiveBasicDevice:: IsSearchSupported</span><span class="sxs-lookup"><span data-stu-id="359de-106">ActiveBasicDevice::IsSearchSupported property</span></span>

<span data-ttu-id="359de-107">Obtém um valor que indica se o dispositivo dá suporte à pesquisa.</span><span class="sxs-lookup"><span data-stu-id="359de-107">Gets a value that indicates if the device supports search.</span></span>

<span data-ttu-id="359de-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="359de-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="359de-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="359de-109">Syntax</span></span>


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="359de-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="359de-110">Property value</span></span>

<span data-ttu-id="359de-111">Um ponteiro para um **booliano** que indica se o dispositivo dá suporte à pesquisa.</span><span class="sxs-lookup"><span data-stu-id="359de-111">A pointer to a **boolean** that indicates if the device supports search.</span></span>

<span data-ttu-id="359de-112">**true** se o dispositivo der suporte à pesquisa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="359de-112">**true** if the device supports search; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="359de-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="359de-113">Requirements</span></span>



| <span data-ttu-id="359de-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="359de-114">Requirement</span></span> | <span data-ttu-id="359de-115">Valor</span><span class="sxs-lookup"><span data-stu-id="359de-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="359de-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="359de-116">Minimum supported client</span></span><br/> | <span data-ttu-id="359de-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="359de-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="359de-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="359de-118">Minimum supported server</span></span><br/> | <span data-ttu-id="359de-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="359de-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="359de-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="359de-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="359de-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="359de-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="359de-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="359de-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="359de-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="359de-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="359de-124">DLL</span><span class="sxs-lookup"><span data-stu-id="359de-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="359de-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="359de-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="359de-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="359de-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="359de-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="359de-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

