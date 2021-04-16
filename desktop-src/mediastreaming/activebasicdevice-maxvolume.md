---
title: Propriedade ActiveBasicDevice MaxVolume (PlayToDevice. h)
description: Obtém o volume máximo com suporte pelo dispositivo.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- API de streaming de mídia de propriedade MaxVolume
- API de streaming de mídia de propriedade MaxVolume, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48c25ef6c0e25c35ba07914c00fb063b4e8dc79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455937"
---
# <a name="activebasicdevicemaxvolume-property"></a><span data-ttu-id="15e05-106">Propriedade ActiveBasicDevice:: MaxVolume</span><span class="sxs-lookup"><span data-stu-id="15e05-106">ActiveBasicDevice::MaxVolume property</span></span>

<span data-ttu-id="15e05-107">Obtém o volume máximo com suporte pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15e05-107">Gets the maximum volume supported by the device.</span></span>

<span data-ttu-id="15e05-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="15e05-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e05-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15e05-109">Syntax</span></span>


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a><span data-ttu-id="15e05-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="15e05-110">Property value</span></span>

<span data-ttu-id="15e05-111">Um ponteiro para um **UINT32** que especifica o volume máximo suportado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15e05-111">A pointer to a **UINT32** that specifies the maximum volume supported by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e05-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15e05-112">Requirements</span></span>



| <span data-ttu-id="15e05-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="15e05-113">Requirement</span></span> | <span data-ttu-id="15e05-114">Valor</span><span class="sxs-lookup"><span data-stu-id="15e05-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e05-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15e05-115">Minimum supported client</span></span><br/> | <span data-ttu-id="15e05-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15e05-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15e05-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15e05-117">Minimum supported server</span></span><br/> | <span data-ttu-id="15e05-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="15e05-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15e05-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15e05-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e05-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="15e05-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="15e05-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="15e05-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15e05-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15e05-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="15e05-123">DLL</span><span class="sxs-lookup"><span data-stu-id="15e05-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15e05-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e05-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e05-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="15e05-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="15e05-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15e05-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

