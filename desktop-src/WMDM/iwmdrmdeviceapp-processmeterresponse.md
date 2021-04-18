---
title: Método IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: O método ProcessMeterResponse redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo tiverem sido enviados e processados pelo servidor.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Método ProcessMeterResponse Windows Media Gerenciador de Dispositivos
- Método ProcessMeterResponse Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800184"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a><span data-ttu-id="3d100-106">IWMDRMDeviceApp: método rocessMeterResponse de:P</span><span class="sxs-lookup"><span data-stu-id="3d100-106">IWMDRMDeviceApp::ProcessMeterResponse method</span></span>

<span data-ttu-id="3d100-107">O método **ProcessMeterResponse** redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo tiverem sido enviados e processados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="3d100-107">The **ProcessMeterResponse** method resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d100-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d100-108">Syntax</span></span>


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3d100-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d100-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d100-110">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d100-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d100-111">Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="3d100-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="3d100-112">*pbResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d100-112">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d100-113">Resposta recebida de um servidor de medição depois de enviar dados gerados usando [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span><span class="sxs-lookup"><span data-stu-id="3d100-113">Response received from a metering server, after sending data generated using [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d100-114">*cbResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d100-114">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d100-115">Tamanho de *pbResponse*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3d100-115">Size of *pbResponse*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3d100-116">*pdwFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3d100-116">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d100-117">Um **DWORD** da tabela a seguir que indica se há mais dados de medição no dispositivo que precisam ser processados.</span><span class="sxs-lookup"><span data-stu-id="3d100-117">A **DWORD** from the following table indicating whether there is more metering data on the device that needs to be processed.</span></span>



| <span data-ttu-id="3d100-118">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="3d100-118">Flag</span></span>                            | <span data-ttu-id="3d100-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d100-119">Description</span></span>                                     |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="3d100-120">\_ \_ todas as respostas de medidor de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="3d100-120">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="3d100-121">Todos os dados de medição foram processados.</span><span class="sxs-lookup"><span data-stu-id="3d100-121">All metering data has been processed.</span></span>           |
| <span data-ttu-id="3d100-122">\_parcial de \_ resposta de medidor de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="3d100-122">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="3d100-123">Dados de medição adicionais precisam ser processados.</span><span class="sxs-lookup"><span data-stu-id="3d100-123">Additional metering data needs to be processed.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d100-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d100-124">Return value</span></span>

<span data-ttu-id="3d100-125">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3d100-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3d100-126">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d100-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3d100-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3d100-127">Return code</span></span>                                                                                                      | <span data-ttu-id="3d100-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d100-128">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d100-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3d100-129"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="3d100-130">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3d100-130">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="3d100-131"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3d100-131"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="3d100-132">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="3d100-132">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="3d100-133"><dt>**Erros do dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="3d100-133"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="3d100-134">Qualquer um dos vários erros do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d100-134">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="3d100-135"><dt>**Erros do cliente DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="3d100-135"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="3d100-136">Qualquer um dos vários erros internos do cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="3d100-136">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="3d100-137"><dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d100-137"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="3d100-138">O dispositivo especificado não é um dispositivo compatível com DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3d100-138">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d100-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d100-139">Remarks</span></span>

<span data-ttu-id="3d100-140">Mais informações sobre medição, incluindo exemplos de código, podem ser encontradas no White Paper [monitorando o uso de conteúdo de mídia digital com o Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) no site do MSDN.</span><span class="sxs-lookup"><span data-stu-id="3d100-140">More information on metering, including code examples, can be found in the whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) on the MSDN Web site.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d100-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d100-141">Requirements</span></span>



| <span data-ttu-id="3d100-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d100-142">Requirement</span></span> | <span data-ttu-id="3d100-143">Valor</span><span class="sxs-lookup"><span data-stu-id="3d100-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d100-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d100-144">Header</span></span><br/>  | <dl> <span data-ttu-id="3d100-145"><dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="3d100-145"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="3d100-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d100-146">Library</span></span><br/> | <dl> <span data-ttu-id="3d100-147"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d100-147"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="3d100-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d100-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d100-149">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="3d100-149">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="3d100-150">**Interface IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="3d100-150">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="3d100-151">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="3d100-151">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

