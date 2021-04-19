---
title: Método IWMDRMDevice GetDeviceCertificate
description: O método GetDeviceCertificate recupera o certificado do dispositivo.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Método GetDeviceCertificate Windows Media Gerenciador de Dispositivos
- Método GetDeviceCertificate Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método GetDeviceCertificate
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810600"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a><span data-ttu-id="598c5-106">Método IWMDRMDevice:: GetDeviceCertificate</span><span class="sxs-lookup"><span data-stu-id="598c5-106">IWMDRMDevice::GetDeviceCertificate method</span></span>

<span data-ttu-id="598c5-107">O método **GetDeviceCertificate** recupera o certificado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="598c5-107">The **GetDeviceCertificate** method retrieves the device certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="598c5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="598c5-108">Syntax</span></span>


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a><span data-ttu-id="598c5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="598c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598c5-110">*pbstrDevCert* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="598c5-110">*pbstrDevCert* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="598c5-111">Ponteiro para um **BSTR** que contém o certificado de dispositivo recuperado.</span><span class="sxs-lookup"><span data-stu-id="598c5-111">Pointer to a **BSTR** containing the retrieved device certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598c5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="598c5-112">Return value</span></span>

<span data-ttu-id="598c5-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="598c5-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="598c5-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="598c5-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="598c5-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="598c5-115">Return code</span></span>                                                                          | <span data-ttu-id="598c5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="598c5-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="598c5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="598c5-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="598c5-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="598c5-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="598c5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="598c5-119">Requirements</span></span>



| <span data-ttu-id="598c5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="598c5-120">Requirement</span></span> | <span data-ttu-id="598c5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="598c5-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="598c5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="598c5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="598c5-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="598c5-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="598c5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="598c5-124">Library</span></span><br/> | <dl> <span data-ttu-id="598c5-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="598c5-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598c5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="598c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598c5-127">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="598c5-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





