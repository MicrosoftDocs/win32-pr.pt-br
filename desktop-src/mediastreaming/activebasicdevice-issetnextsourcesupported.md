---
title: Propriedade ActiveBasicDevice IsSetNextSourceSupported (PlayToDevice. h)
description: Obtém um valor que indica se há suporte para a configuração da próxima fonte.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- API de streaming de mídia de propriedade IsSetNextSourceSupported
- API de streaming de mídia de propriedade IsSetNextSourceSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812334"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a><span data-ttu-id="56e5e-106">Propriedade ActiveBasicDevice:: IsSetNextSourceSupported</span><span class="sxs-lookup"><span data-stu-id="56e5e-106">ActiveBasicDevice::IsSetNextSourceSupported property</span></span>

<span data-ttu-id="56e5e-107">Obtém um valor que indica se há suporte para a configuração da próxima fonte.</span><span class="sxs-lookup"><span data-stu-id="56e5e-107">Gets a value that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="56e5e-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="56e5e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e5e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56e5e-109">Syntax</span></span>


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="56e5e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="56e5e-110">Property value</span></span>

<span data-ttu-id="56e5e-111">Um ponteiro para um **booliano** que indica se há suporte para a configuração da próxima fonte.</span><span class="sxs-lookup"><span data-stu-id="56e5e-111">A pointer to a **boolean** that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="56e5e-112">**true** se a configuração da próxima fonte for suportada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="56e5e-112">**true** if setting the next source is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e5e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56e5e-113">Requirements</span></span>



| <span data-ttu-id="56e5e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56e5e-114">Requirement</span></span> | <span data-ttu-id="56e5e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="56e5e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e5e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56e5e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56e5e-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56e5e-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56e5e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56e5e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56e5e-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="56e5e-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="56e5e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56e5e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56e5e-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="56e5e-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="56e5e-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="56e5e-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56e5e-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56e5e-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="56e5e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="56e5e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56e5e-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e5e-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e5e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="56e5e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="56e5e-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56e5e-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

