---
title: Propriedade IVMUSBDevice DeviceString (VPCCOMInterfaces. h)
description: Recupera o nome do dispositivo USB.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Propriedade DeviceString do PC virtual
- Propriedade DeviceString, PC virtual, interface IVMUSBDevice
- IVMUSBDevice interface virtual PC, Propriedade DeviceString
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824466"
---
# <a name="ivmusbdevicedevicestring-property"></a><span data-ttu-id="e069b-106">IVMUSBDevice: Propriedade eviceString de:D</span><span class="sxs-lookup"><span data-stu-id="e069b-106">IVMUSBDevice::DeviceString property</span></span>

<span data-ttu-id="e069b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e069b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e069b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e069b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e069b-109">Recupera o nome do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="e069b-109">Retrieves the name of the USB device.</span></span>

<span data-ttu-id="e069b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e069b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e069b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e069b-111">Syntax</span></span>


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a><span data-ttu-id="e069b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e069b-112">Property value</span></span>

<span data-ttu-id="e069b-113">O nome do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="e069b-113">The name of the USB device.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e069b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e069b-114">Error codes</span></span>



| <span data-ttu-id="e069b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e069b-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="e069b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e069b-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e069b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e069b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="e069b-118">O método foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="e069b-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e069b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e069b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="e069b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e069b-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="e069b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e069b-121">Requirements</span></span>



| <span data-ttu-id="e069b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e069b-122">Requirement</span></span> | <span data-ttu-id="e069b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e069b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e069b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e069b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e069b-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e069b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e069b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e069b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e069b-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e069b-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e069b-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e069b-128">End of client support</span></span><br/>    | <span data-ttu-id="e069b-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e069b-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e069b-130">Produto</span><span class="sxs-lookup"><span data-stu-id="e069b-130">Product</span></span><br/>                  | <span data-ttu-id="e069b-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e069b-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e069b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e069b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e069b-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e069b-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e069b-134">IID</span><span class="sxs-lookup"><span data-stu-id="e069b-134">IID</span></span><br/>                      | <span data-ttu-id="e069b-135">IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="e069b-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e069b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e069b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e069b-137">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="e069b-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

