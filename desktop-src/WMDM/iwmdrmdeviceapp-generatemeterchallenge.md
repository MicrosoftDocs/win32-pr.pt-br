---
title: Método IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp. h)
description: O método GenerateMeterChallenge adquire dados de medição de um dispositivo.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Método GenerateMeterChallenge Windows Media Gerenciador de Dispositivos
- Método GenerateMeterChallenge Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método GenerateMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810596"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a><span data-ttu-id="1a8f5-106">Método IWMDRMDeviceApp:: GenerateMeterChallenge</span><span class="sxs-lookup"><span data-stu-id="1a8f5-106">IWMDRMDeviceApp::GenerateMeterChallenge method</span></span>

<span data-ttu-id="1a8f5-107">O método **GenerateMeterChallenge** adquire dados de medição de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-107">The **GenerateMeterChallenge** method acquires metering data from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8f5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a8f5-108">Syntax</span></span>


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a><span data-ttu-id="1a8f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a8f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a8f5-110">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a8f5-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8f5-111">Ponteiro para uma interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="1a8f5-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="1a8f5-112">Se o aplicativo passar em **NULL**, as informações de medição armazenadas no computador serão usadas em vez de monitorar as informações de um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-112">If the application passes in **NULL**, metering information stored on the computer is used instead of metering information from a connected device.</span></span>

</dd> <dt>

<span data-ttu-id="1a8f5-113">*bstrMeterCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a8f5-113">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8f5-114">O certificado de medição do aplicativo, como um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-114">The application's metering certificate, as a **BSTR**.</span></span> <span data-ttu-id="1a8f5-115">Este é um certificado assinado recebido da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-115">This is a signed certificate received from Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="1a8f5-116">*pbstrMeterURL* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a8f5-116">*pbstrMeterURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8f5-117">A URL na qual os dados de medição devem ser enviados.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-117">The URL where metering data should be sent.</span></span> <span data-ttu-id="1a8f5-118">Isso é alocado pelo Windows Media Gerenciador de Dispositivos e deve ser gratuito pelo chamador usando **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-118">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> <dt>

<span data-ttu-id="1a8f5-119">*pbstrMeterData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a8f5-119">*pbstrMeterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8f5-120">Medição de dados a serem enviados para o serviço de medição.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-120">Metering data to send to the metering service.</span></span> <span data-ttu-id="1a8f5-121">Isso é alocado pelo Windows Media Gerenciador de Dispositivos e deve ser gratuito pelo chamador usando **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-121">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a8f5-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a8f5-122">Return value</span></span>

<span data-ttu-id="1a8f5-123">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1a8f5-124">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1a8f5-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1a8f5-125">Return code</span></span>                                                                                                      | <span data-ttu-id="1a8f5-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a8f5-126">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a8f5-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-127"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="1a8f5-128">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-128">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="1a8f5-129"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-129"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="1a8f5-130">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-130">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="1a8f5-131"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-131"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>             | <span data-ttu-id="1a8f5-132">O XML está formado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-132">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="1a8f5-133"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-133"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>             | <span data-ttu-id="1a8f5-134">O XML está formado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-134">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="1a8f5-135"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-135"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>              | <span data-ttu-id="1a8f5-136">O XML está formado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-136">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="1a8f5-137"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-137"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>               | <span data-ttu-id="1a8f5-138">Falha ao localizar uma marca XML necessária.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-138">Failed to find a required XML tag.</span></span><br/>                                 |
| <dl> <span data-ttu-id="1a8f5-139"><dt>**Erros do dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-139"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="1a8f5-140">Qualquer um dos vários erros do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-140">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="1a8f5-141"><dt>**Erros do cliente DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-141"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="1a8f5-142">Qualquer um dos vários erros internos do cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-142">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="1a8f5-143"><dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-143"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="1a8f5-144">O dispositivo especificado não é um dispositivo compatível com DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-144">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1a8f5-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a8f5-145">Remarks</span></span>

<span data-ttu-id="1a8f5-146">Antes de chamar esse método, o aplicativo deve chamar [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) para verificar se todos os componentes DRM do dispositivo estão atualizados.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-146">Before calling this method, the application should call [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) to verify that all the device's DRM components are up to date.</span></span> <span data-ttu-id="1a8f5-147">Esse método só pode ser chamado em um dispositivo que ofereça suporte ao Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-147">This method can only be called on a device that supports Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="1a8f5-148">Os dados recuperados *pbstrMeterData* devem ser enviados para a URL especificada por *pbstrMeterURL*.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-148">The retrieved data *pbstrMeterData* should be sent to the URL specified by *pbstrMeterURL*.</span></span> <span data-ttu-id="1a8f5-149">Certifique-se de codificar por URL os dados recuperados para que eles não sejam modificados durante a transferência.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-149">Be sure to URL-encode the retrieved data so that it does not get modified during transfer.</span></span>

<span data-ttu-id="1a8f5-150">Consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-150">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="1a8f5-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a8f5-151">Examples</span></span>

<span data-ttu-id="1a8f5-152">O exemplo de código C++ a seguir cria um objeto **WMDRMDeviceApp** , verifica se o dispositivo é um dispositivo Windows Media DRM 10, se o relógio está correto e solicita os dados de medição.</span><span class="sxs-lookup"><span data-stu-id="1a8f5-152">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a><span data-ttu-id="1a8f5-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a8f5-153">Requirements</span></span>



| <span data-ttu-id="1a8f5-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a8f5-154">Requirement</span></span> | <span data-ttu-id="1a8f5-155">Valor</span><span class="sxs-lookup"><span data-stu-id="1a8f5-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8f5-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a8f5-156">Header</span></span><br/>  | <dl> <span data-ttu-id="1a8f5-157"><dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-157"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="1a8f5-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a8f5-158">Library</span></span><br/> | <dl> <span data-ttu-id="1a8f5-159"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a8f5-159"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="1a8f5-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a8f5-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8f5-161">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="1a8f5-161">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="1a8f5-162">**Interface IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="1a8f5-162">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="1a8f5-163">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="1a8f5-163">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





