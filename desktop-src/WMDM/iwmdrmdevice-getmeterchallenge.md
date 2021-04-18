---
title: Método IWMDRMDevice GetMeterChallenge
description: O método GetMeterChallenge recupera o desafio de medição.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Método GetMeterChallenge Windows Media Gerenciador de Dispositivos
- Método GetMeterChallenge Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781294"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a><span data-ttu-id="e6416-106">Método IWMDRMDevice:: GetMeterChallenge</span><span class="sxs-lookup"><span data-stu-id="e6416-106">IWMDRMDevice::GetMeterChallenge method</span></span>

<span data-ttu-id="e6416-107">O método **GetMeterChallenge** recupera o desafio de medição.</span><span class="sxs-lookup"><span data-stu-id="e6416-107">The **GetMeterChallenge** method retrieves the metering challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6416-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6416-108">Syntax</span></span>


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="e6416-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6416-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6416-110">*bstrMeterCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6416-110">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6416-111">Certificado de medição que o proprietário do conteúdo envia ao computador host para coletar os dados de medição associados no dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6416-111">Metering certificate that the content owner sends to the host computer for collecting the associated metering data on the device</span></span>

</dd> <dt>

<span data-ttu-id="e6416-112">*ppbMeterChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e6416-112">*ppbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6416-113">Resultado do desafio de medição recuperado.</span><span class="sxs-lookup"><span data-stu-id="e6416-113">Retrieved metering challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="e6416-114">*pcbMeterChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e6416-114">*pcbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6416-115">O tamanho do desafio de medição, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e6416-115">The size of the metering challenge, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6416-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6416-116">Return value</span></span>

<span data-ttu-id="e6416-117">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e6416-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e6416-118">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6416-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e6416-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e6416-119">Return code</span></span>                                                                          | <span data-ttu-id="e6416-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6416-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e6416-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6416-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e6416-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e6416-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6416-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6416-123">Remarks</span></span>

<span data-ttu-id="e6416-124">A medição de dados é coletada e armazenada no armazenamento de dados DRM no dispositivo para conteúdo com medição habilitada.</span><span class="sxs-lookup"><span data-stu-id="e6416-124">Metering data is collected and stored in the DRM data store on the device for content with metering enabled.</span></span> <span data-ttu-id="e6416-125">Ações como reproduzir serão registradas.</span><span class="sxs-lookup"><span data-stu-id="e6416-125">Actions such as play will be recorded.</span></span> <span data-ttu-id="e6416-126">Quando essa função é chamada, o dispositivo coleta os dados de medição no armazenamento de dados DRM na forma de um documento XML e os envia para o hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="e6416-126">When this function is called, the device collects the metering data in the DRM data store in the form of an XML document and sends it to the hostcomputer.</span></span> <span data-ttu-id="e6416-127">Se houver muitos dados, eles serão enviados em fases.</span><span class="sxs-lookup"><span data-stu-id="e6416-127">If there is too much data, it is sent in phases.</span></span>

<span data-ttu-id="e6416-128">Quando o computador host recebe os dados de medição, ele envia os dados pela Internet para a URL especificada no certificado de medição.</span><span class="sxs-lookup"><span data-stu-id="e6416-128">When the host computer receives the metering data, it sends the data over the Internet to the URL specified in the metering certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6416-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6416-129">Requirements</span></span>



| <span data-ttu-id="e6416-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6416-130">Requirement</span></span> | <span data-ttu-id="e6416-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e6416-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6416-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6416-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e6416-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6416-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="e6416-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6416-134">Library</span></span><br/> | <dl> <span data-ttu-id="e6416-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6416-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6416-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6416-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6416-137">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="e6416-137">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





