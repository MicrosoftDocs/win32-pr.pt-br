---
title: Método IWMDRMDevice IsWMDRMDevice
description: O método IsWMDRMDevice determina se o dispositivo dá suporte ao Windows Media DRM 10 para dispositivos portáteis.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Método IsWMDRMDevice Windows Media Gerenciador de Dispositivos
- Método IsWMDRMDevice Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763392"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a><span data-ttu-id="f63a8-106">Método IWMDRMDevice:: IsWMDRMDevice</span><span class="sxs-lookup"><span data-stu-id="f63a8-106">IWMDRMDevice::IsWMDRMDevice method</span></span>

<span data-ttu-id="f63a8-107">O método **IsWMDRMDevice** determina se o dispositivo dá suporte ao Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="f63a8-107">The **IsWMDRMDevice** method determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f63a8-108">Syntax</span></span>


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a><span data-ttu-id="f63a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f63a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f63a8-110">*pdwVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f63a8-110">*pdwVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f63a8-111">Versão do Windows Media DRM 10 para dispositivos portáteis, que tem o valor de 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="f63a8-111">Version of Windows Media DRM 10 for Portable Devices, which has value of 0x00010000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f63a8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f63a8-112">Return value</span></span>

<span data-ttu-id="f63a8-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f63a8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f63a8-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f63a8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f63a8-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f63a8-115">Return code</span></span>                                                                          | <span data-ttu-id="f63a8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f63a8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f63a8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f63a8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f63a8-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f63a8-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f63a8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f63a8-119">Requirements</span></span>



| <span data-ttu-id="f63a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63a8-120">Requirement</span></span> | <span data-ttu-id="f63a8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f63a8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f63a8-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f63a8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f63a8-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f63a8-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="f63a8-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f63a8-124">Library</span></span><br/> | <dl> <span data-ttu-id="f63a8-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f63a8-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63a8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f63a8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63a8-127">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="f63a8-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





