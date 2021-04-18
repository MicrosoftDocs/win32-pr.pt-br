---
title: Método ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtém as informações do protocolo de coletor em cache para o dispositivo. | Método ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- API de streaming de mídia do método SetCachedSinkProtocolInfo
- API de streaming de mídia do método SetCachedSinkProtocolInfo, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método SetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105762971"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a><span data-ttu-id="51d22-107">Método ActiveBasicDevice:: SetCachedSinkProtocolInfo</span><span class="sxs-lookup"><span data-stu-id="51d22-107">ActiveBasicDevice::SetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="51d22-108">Obtém as informações do protocolo de coletor em cache para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51d22-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d22-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51d22-109">Syntax</span></span>


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="51d22-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51d22-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51d22-111">*physicalNetworkInterface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51d22-111">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51d22-112">Especifica a interface de rede física.</span><span class="sxs-lookup"><span data-stu-id="51d22-112">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="51d22-113">*taxa de bits* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51d22-113">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51d22-114">O valor de taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="51d22-114">The bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51d22-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51d22-115">Return value</span></span>

<span data-ttu-id="51d22-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="51d22-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51d22-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51d22-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51d22-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51d22-118">Requirements</span></span>



| <span data-ttu-id="51d22-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51d22-119">Requirement</span></span> | <span data-ttu-id="51d22-120">Valor</span><span class="sxs-lookup"><span data-stu-id="51d22-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d22-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51d22-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51d22-122">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51d22-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="51d22-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51d22-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51d22-124">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="51d22-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="51d22-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51d22-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="51d22-126"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="51d22-126"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="51d22-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="51d22-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51d22-128"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="51d22-128"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="51d22-129">DLL</span><span class="sxs-lookup"><span data-stu-id="51d22-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51d22-130"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51d22-130"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d22-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="51d22-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="51d22-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51d22-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

