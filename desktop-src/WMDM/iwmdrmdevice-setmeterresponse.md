---
title: Método IWMDRMDevice SetMeterResponse
description: O método SetMeterResponse define a resposta de medição.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Método SetMeterResponse Windows Media Gerenciador de Dispositivos
- Método SetMeterResponse Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810598"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a><span data-ttu-id="01512-106">Método IWMDRMDevice:: SetMeterResponse</span><span class="sxs-lookup"><span data-stu-id="01512-106">IWMDRMDevice::SetMeterResponse method</span></span>

<span data-ttu-id="01512-107">O método **SetMeterResponse** define a resposta de medição.</span><span class="sxs-lookup"><span data-stu-id="01512-107">The **SetMeterResponse** method sets the metering response.</span></span>

## <a name="syntax"></a><span data-ttu-id="01512-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01512-108">Syntax</span></span>


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="01512-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01512-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01512-110">*pbMeterResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01512-110">*pbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01512-111">A resposta de medição a ser definida.</span><span class="sxs-lookup"><span data-stu-id="01512-111">The metering response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="01512-112">*cbMeterResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01512-112">*cbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01512-113">Tamanho da resposta de medição, em bytes.</span><span class="sxs-lookup"><span data-stu-id="01512-113">Size of the metering response, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="01512-114">*pdwFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01512-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01512-115">Sinalizadores de resposta.</span><span class="sxs-lookup"><span data-stu-id="01512-115">Response flags.</span></span> <span data-ttu-id="01512-116">Esse valor deve ser um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="01512-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="01512-117">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="01512-117">Flag</span></span>                            | <span data-ttu-id="01512-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="01512-118">Description</span></span>              |
|---------------------------------|--------------------------|
| <span data-ttu-id="01512-119">\_ \_ todas as respostas de medidor de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="01512-119">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="01512-120">Todas as respostas do medidor.</span><span class="sxs-lookup"><span data-stu-id="01512-120">All meter responses.</span></span>     |
| <span data-ttu-id="01512-121">\_parcial de \_ resposta de medidor de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="01512-121">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="01512-122">Respostas de medidor parciais.</span><span class="sxs-lookup"><span data-stu-id="01512-122">Partial meter responses.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01512-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01512-123">Return value</span></span>

<span data-ttu-id="01512-124">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="01512-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="01512-125">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01512-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="01512-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01512-126">Return code</span></span>                                                                          | <span data-ttu-id="01512-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="01512-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="01512-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01512-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="01512-129">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="01512-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="01512-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01512-130">Requirements</span></span>



| <span data-ttu-id="01512-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="01512-131">Requirement</span></span> | <span data-ttu-id="01512-132">Valor</span><span class="sxs-lookup"><span data-stu-id="01512-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01512-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01512-133">Header</span></span><br/>  | <dl> <span data-ttu-id="01512-134"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01512-134"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="01512-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01512-135">Library</span></span><br/> | <dl> <span data-ttu-id="01512-136"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01512-136"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01512-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="01512-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01512-138">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="01512-138">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





