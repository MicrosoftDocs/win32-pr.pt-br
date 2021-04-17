---
title: Método IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: O método QueryDeviceStatus consulta um dispositivo quanto ao seu status e recursos de DRM atuais.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Método QueryDeviceStatus Windows Media Gerenciador de Dispositivos
- Método QueryDeviceStatus Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759760"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a><span data-ttu-id="45f91-106">Método IWMDRMDeviceApp:: QueryDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="45f91-106">IWMDRMDeviceApp::QueryDeviceStatus method</span></span>

<span data-ttu-id="45f91-107">O método **QueryDeviceStatus** consulta um dispositivo quanto ao seu status e recursos de DRM atuais.</span><span class="sxs-lookup"><span data-stu-id="45f91-107">The **QueryDeviceStatus** method queries a device for its current DRM status and capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f91-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45f91-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="45f91-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45f91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f91-110">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45f91-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f91-111">Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="45f91-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="45f91-112">*pdwStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="45f91-112">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45f91-113">Zero ou mais dos valores **DWORD** a seguir que descrevem os aspectos de DRM do dispositivo, combinados com um **OR bit a** bit.</span><span class="sxs-lookup"><span data-stu-id="45f91-113">Zero or more of the following **DWORD** values describing the DRM aspects of the device, combined with a bitwise **OR**.</span></span> <span data-ttu-id="45f91-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="45f91-114">See Remarks.</span></span>



| <span data-ttu-id="45f91-115">Status</span><span class="sxs-lookup"><span data-stu-id="45f91-115">Status</span></span>                      | <span data-ttu-id="45f91-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="45f91-116">Description</span></span>                                  |
|-----------------------------|----------------------------------------------|
| <span data-ttu-id="45f91-117">\_ISWMDRM de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="45f91-117">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="45f91-118">O dispositivo dá suporte a DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="45f91-118">The device supports Windows Media DRM.</span></span>       |
| <span data-ttu-id="45f91-119">\_NEEDCLOCK de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="45f91-119">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="45f91-120">O dispositivo não tem um Clock seguro.</span><span class="sxs-lookup"><span data-stu-id="45f91-120">The device does not have a secure clock.</span></span>     |
| <span data-ttu-id="45f91-121">\_dispositivo WMDRM \_ revogado</span><span class="sxs-lookup"><span data-stu-id="45f91-121">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="45f91-122">O dispositivo foi revogado.</span><span class="sxs-lookup"><span data-stu-id="45f91-122">The device has been revoked.</span></span>                 |
| <span data-ttu-id="45f91-123">\_NEEDINDIV do cliente WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="45f91-123">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="45f91-124">A segurança do DRM precisa ser individualizada.</span><span class="sxs-lookup"><span data-stu-id="45f91-124">The DRM security needs to be individualized.</span></span> |
| <span data-ttu-id="45f91-125">\_REFRESHCLOCK de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="45f91-125">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="45f91-126">O relógio precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="45f91-126">The clock needs to be refreshed.</span></span>             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f91-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45f91-127">Return value</span></span>

<span data-ttu-id="45f91-128">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="45f91-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="45f91-129">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="45f91-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="45f91-130">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="45f91-130">Return code</span></span>                                                                                                              | <span data-ttu-id="45f91-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="45f91-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45f91-132"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="45f91-132"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="45f91-133">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="45f91-133">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="45f91-134"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="45f91-134"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="45f91-135">O argumento de entrada não é válido.</span><span class="sxs-lookup"><span data-stu-id="45f91-135">The input argument is not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="45f91-136"><dt>**certificado inválido do NS \_ E \_ DRM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45f91-136"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="45f91-137">O certificado de dispositivo recuperado do dispositivo não é válido.</span><span class="sxs-lookup"><span data-stu-id="45f91-137">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="45f91-138"><dt>**o NS \_ E \_ DRM \_ não pode \_ obter o \_ \_ certificado do dispositivo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45f91-138"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="45f91-139">Falha ao recuperar o certificado do dispositivo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45f91-139">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="45f91-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="45f91-140">Remarks</span></span>

<span data-ttu-id="45f91-141">Esse método deve ser chamado antes de executar qualquer ação restrita no conteúdo DRM, como transferir conteúdo DRM para o dispositivo ou adquirir informações de medição.</span><span class="sxs-lookup"><span data-stu-id="45f91-141">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="45f91-142">Se os valores recuperados por *pdwStatus* indicarem que alguma ação precisa ser executada (como individualização para a área de trabalho ou aquisição de um relógio para o dispositivo), o aplicativo deverá chamar [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor de *pdwStatus* recuperado dessa função para o parâmetro *dwFlags* em **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="45f91-142">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="45f91-143">Se zero for retornado, o dispositivo não oferecerá suporte ao Windows Media DRM 10 para dispositivos portáteis e nenhuma ação precisará ser executada.</span><span class="sxs-lookup"><span data-stu-id="45f91-143">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="45f91-144">Consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="45f91-144">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="45f91-145">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45f91-145">Examples</span></span>

<span data-ttu-id="45f91-146">O exemplo de código C++ a seguir cria um objeto **WMDRMDeviceApp** , verifica se o dispositivo é um dispositivo Windows Media DRM 10, se o relógio está correto e solicita os dados de medição.</span><span class="sxs-lookup"><span data-stu-id="45f91-146">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="45f91-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45f91-147">Requirements</span></span>



| <span data-ttu-id="45f91-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f91-148">Requirement</span></span> | <span data-ttu-id="45f91-149">Valor</span><span class="sxs-lookup"><span data-stu-id="45f91-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f91-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45f91-150">Header</span></span><br/>  | <dl> <span data-ttu-id="45f91-151"><dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="45f91-151"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="45f91-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45f91-152">Library</span></span><br/> | <dl> <span data-ttu-id="45f91-153"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45f91-153"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="45f91-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="45f91-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f91-155">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="45f91-155">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="45f91-156">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="45f91-156">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="45f91-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="45f91-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





