---
title: Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtém as informações do protocolo de coletor em cache para o dispositivo. | Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- API de streaming de mídia do método GetCachedSinkProtocolInfo
- API de streaming de mídia do método GetCachedSinkProtocolInfo, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781343"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a><span data-ttu-id="d2aa4-107">Método ActiveBasicDevice:: GetCachedSinkProtocolInfo</span><span class="sxs-lookup"><span data-stu-id="d2aa4-107">ActiveBasicDevice::GetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="d2aa4-108">Obtém as informações do protocolo de coletor em cache para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2aa4-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2aa4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2aa4-109">Syntax</span></span>


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="d2aa4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2aa4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2aa4-111">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d2aa4-111">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d2aa4-112">As informações do protocolo de coletor em cache para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2aa4-112">The cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2aa4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2aa4-113">Return value</span></span>

<span data-ttu-id="d2aa4-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d2aa4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2aa4-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2aa4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2aa4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2aa4-116">Requirements</span></span>



| <span data-ttu-id="d2aa4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2aa4-117">Requirement</span></span> | <span data-ttu-id="d2aa4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d2aa4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2aa4-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2aa4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2aa4-120">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2aa4-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d2aa4-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2aa4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2aa4-122">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="d2aa4-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d2aa4-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2aa4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2aa4-124"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2aa4-124"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2aa4-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="d2aa4-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2aa4-126"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2aa4-126"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="d2aa4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d2aa4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2aa4-128"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2aa4-128"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2aa4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2aa4-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2aa4-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2aa4-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

