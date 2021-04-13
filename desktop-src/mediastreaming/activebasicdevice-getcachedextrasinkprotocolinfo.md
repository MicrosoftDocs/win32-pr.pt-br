---
title: Método ActiveBasicDevice GetCachedExtraSinkProtocolInfo (PlayToDevice. h)
description: Obtém informações adicionais do protocolo de coletor armazenado em cache para o dispositivo.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- API de streaming de mídia do método GetCachedExtraSinkProtocolInfo
- API de streaming de mídia do método GetCachedExtraSinkProtocolInfo, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetCachedExtraSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369712"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a><span data-ttu-id="db803-106">Método ActiveBasicDevice:: GetCachedExtraSinkProtocolInfo</span><span class="sxs-lookup"><span data-stu-id="db803-106">ActiveBasicDevice::GetCachedExtraSinkProtocolInfo method</span></span>

<span data-ttu-id="db803-107">Obtém informações adicionais do protocolo de coletor armazenado em cache para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db803-107">Gets additional cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="db803-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db803-108">Syntax</span></span>


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="db803-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db803-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db803-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="db803-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="db803-111">As informações adicionais do protocolo de coletor armazenado em cache para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db803-111">The extra cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db803-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db803-112">Return value</span></span>

<span data-ttu-id="db803-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db803-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db803-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db803-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db803-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db803-115">Requirements</span></span>



| <span data-ttu-id="db803-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="db803-116">Requirement</span></span> | <span data-ttu-id="db803-117">Valor</span><span class="sxs-lookup"><span data-stu-id="db803-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="db803-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db803-118">Minimum supported client</span></span><br/> | <span data-ttu-id="db803-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db803-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="db803-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db803-120">Minimum supported server</span></span><br/> | <span data-ttu-id="db803-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="db803-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db803-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db803-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="db803-123"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="db803-123"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="db803-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="db803-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db803-125"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db803-125"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="db803-126">DLL</span><span class="sxs-lookup"><span data-stu-id="db803-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db803-127"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db803-127"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db803-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="db803-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="db803-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db803-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

