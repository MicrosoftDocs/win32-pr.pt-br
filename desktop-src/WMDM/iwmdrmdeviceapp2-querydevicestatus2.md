---
title: Método IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: O método QueryDeviceStatus2 consulta um dispositivo em busca de um status ou recurso DRM específico.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Método QueryDeviceStatus2 Windows Media Gerenciador de Dispositivos
- Método QueryDeviceStatus2 Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp2
- Interface IWMDRMDeviceApp2 Windows Media Gerenciador de Dispositivos, método QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781471"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a><span data-ttu-id="fc5dd-106">Método IWMDRMDeviceApp2:: QueryDeviceStatus2</span><span class="sxs-lookup"><span data-stu-id="fc5dd-106">IWMDRMDeviceApp2::QueryDeviceStatus2 method</span></span>

<span data-ttu-id="fc5dd-107">O método **QueryDeviceStatus2** consulta um dispositivo em busca de um status ou recurso DRM específico.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-107">The **QueryDeviceStatus2** method queries a device for a specific DRM status or capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc5dd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc5dd-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="fc5dd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc5dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc5dd-110">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc5dd-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5dd-111">Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="fc5dd-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="fc5dd-112">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc5dd-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5dd-113">Um ou mais dos valores **DWORD** a seguir que especificam quais recursos a serem solicitados, combinados com um **OR bit a** bit.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-113">One or more of the following **DWORD** values specifying which capabilities to request, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="fc5dd-114">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="fc5dd-114">Flag</span></span>                              | <span data-ttu-id="fc5dd-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc5dd-115">Description</span></span>                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fc5dd-116">\_INDIVSTATUS do \_ cliente de consulta WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fc5dd-116">WMDRM\_QUERY\_CLIENT\_INDIVSTATUS</span></span> | <span data-ttu-id="fc5dd-117">Consulte se os componentes DRM do computador precisam ser individualizados.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-117">Query whether the computer's DRM components need to be individualized.</span></span>       |
| <span data-ttu-id="fc5dd-118">\_CLOCKSTATUS de \_ dispositivo de consulta WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fc5dd-118">WMDRM\_QUERY\_DEVICE\_CLOCKSTATUS</span></span> | <span data-ttu-id="fc5dd-119">Consulte se o relógio seguro do dispositivo precisa ser adicionado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-119">Query whether the device's secure clock needs to be added or updated.</span></span>        |
| <span data-ttu-id="fc5dd-120">\_dispositivo de consulta WMDRM \_ \_ isrevoged</span><span class="sxs-lookup"><span data-stu-id="fc5dd-120">WMDRM\_QUERY\_DEVICE\_ISREVOKED</span></span>   | <span data-ttu-id="fc5dd-121">Consulte se o dispositivo foi revogado.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-121">Query whether the device is revoked.</span></span>                                         |
| <span data-ttu-id="fc5dd-122">\_ISWMDRM de \_ dispositivo de consulta WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fc5dd-122">WMDRM\_QUERY\_DEVICE\_ISWMDRM</span></span>     | <span data-ttu-id="fc5dd-123">Consulte se o dispositivo dá suporte a Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-123">Query whether the device supports Windows Media DRM 10 for Portable Devices.</span></span> |



 

</dd> <dt>

<span data-ttu-id="fc5dd-124">*pdwStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fc5dd-124">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5dd-125">Zero ou mais dos valores **DWORD** a seguir que especificam o status do dispositivo solicitado, combinado com um **OR bit a** bit.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-125">Zero or more of the following **DWORD** values specifying the requested device status, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="fc5dd-126">Status</span><span class="sxs-lookup"><span data-stu-id="fc5dd-126">Status</span></span>                      | <span data-ttu-id="fc5dd-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc5dd-127">Description</span></span>                                              |
|-----------------------------|----------------------------------------------------------|
| <span data-ttu-id="fc5dd-128">\_ISWMDRM de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fc5dd-128">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="fc5dd-129">O dispositivo dá suporte a DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-129">The device supports Windows Media DRM.</span></span>                   |
| <span data-ttu-id="fc5dd-130">\_NEEDCLOCK de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fc5dd-130">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="fc5dd-131">O dispositivo não tem um Clock seguro.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-131">The device does not have a secure clock.</span></span>                 |
| <span data-ttu-id="fc5dd-132">\_dispositivo WMDRM \_ revogado</span><span class="sxs-lookup"><span data-stu-id="fc5dd-132">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="fc5dd-133">O dispositivo foi revogado.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-133">The device has been revoked.</span></span>                             |
| <span data-ttu-id="fc5dd-134">\_NEEDINDIV do cliente WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fc5dd-134">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="fc5dd-135">Os componentes DRM do computador precisam ser individualizados.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-135">The computer's DRM components need to be individualized.</span></span> |
| <span data-ttu-id="fc5dd-136">\_REFRESHCLOCK de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fc5dd-136">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="fc5dd-137">O relógio precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-137">The clock needs to be refreshed.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc5dd-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc5dd-138">Return value</span></span>

<span data-ttu-id="fc5dd-139">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fc5dd-140">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fc5dd-141">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fc5dd-141">Return code</span></span>                                                                                                              | <span data-ttu-id="fc5dd-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc5dd-142">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc5dd-143"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5dd-143"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="fc5dd-144">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-144">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="fc5dd-145"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5dd-145"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="fc5dd-146">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-146">One or more arguments are not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="fc5dd-147"><dt>**certificado inválido do NS \_ E \_ DRM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5dd-147"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="fc5dd-148">O certificado de dispositivo recuperado do dispositivo não é válido.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-148">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="fc5dd-149"><dt>**o NS \_ E \_ DRM \_ não pode \_ obter o \_ \_ certificado do dispositivo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc5dd-149"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="fc5dd-150">Falha ao recuperar o certificado do dispositivo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-150">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="fc5dd-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc5dd-151">Remarks</span></span>

<span data-ttu-id="fc5dd-152">Esse método deve ser chamado antes de executar qualquer ação restrita no conteúdo DRM, como transferir conteúdo DRM para o dispositivo ou adquirir informações de medição.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-152">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="fc5dd-153">Se os valores recuperados por *pdwStatus* indicarem que alguma ação precisa ser executada (como individualização para a área de trabalho ou aquisição de um relógio para o dispositivo), o aplicativo deverá chamar [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor *pdwStatus* recuperado dessa função para o parâmetro *dwFlags* em **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-153">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="fc5dd-154">Se zero for retornado, o dispositivo não oferecerá suporte ao Windows Media DRM 10 para dispositivos portáteis e nenhuma ação precisará ser executada.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-154">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="fc5dd-155">Consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="fc5dd-155">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5dd-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc5dd-156">Requirements</span></span>



| <span data-ttu-id="fc5dd-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc5dd-157">Requirement</span></span> | <span data-ttu-id="fc5dd-158">Valor</span><span class="sxs-lookup"><span data-stu-id="fc5dd-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5dd-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc5dd-159">Header</span></span><br/>  | <dl> <span data-ttu-id="fc5dd-160"><dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="fc5dd-160"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="fc5dd-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc5dd-161">Library</span></span><br/> | <dl> <span data-ttu-id="fc5dd-162"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc5dd-162"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="fc5dd-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc5dd-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5dd-164">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="fc5dd-164">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="fc5dd-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="fc5dd-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[<span data-ttu-id="fc5dd-166">**Interface IWMDRMDeviceApp2**</span><span class="sxs-lookup"><span data-stu-id="fc5dd-166">**IWMDRMDeviceApp2 Interface**</span></span>](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





