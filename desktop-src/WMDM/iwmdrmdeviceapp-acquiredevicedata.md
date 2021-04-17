---
title: Método IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: O método AcquireDeviceData inicializa ou redefine um relógio seguro do dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Método AcquireDeviceData Windows Media Gerenciador de Dispositivos
- Método AcquireDeviceData Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método AcquireDeviceData
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770534"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a><span data-ttu-id="e0870-106">Método IWMDRMDeviceApp:: AcquireDeviceData</span><span class="sxs-lookup"><span data-stu-id="e0870-106">IWMDRMDeviceApp::AcquireDeviceData method</span></span>

<span data-ttu-id="e0870-107">O método **AcquireDeviceData** inicializa ou redefine um relógio seguro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0870-107">The **AcquireDeviceData** method initializes or resets a device secure clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0870-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0870-108">Syntax</span></span>


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="e0870-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0870-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0870-110">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0870-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0870-111">Ponteiro para uma interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) para o dispositivo que irá relatar dados de medição.</span><span class="sxs-lookup"><span data-stu-id="e0870-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface for the device that will report metering data.</span></span>

</dd> <dt>

<span data-ttu-id="e0870-112">*pProgressCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0870-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0870-113">O retorno de chamada de progresso por meio do qual o aplicativo pode acompanhar o progresso do evento ou cancelar o evento.</span><span class="sxs-lookup"><span data-stu-id="e0870-113">Progress callback through which the application can track the progress of the event, or cancel the event.</span></span> <span data-ttu-id="e0870-114">O progresso é identificado pelo parâmetro *EventID* dos métodos [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .</span><span class="sxs-lookup"><span data-stu-id="e0870-114">The progress is identified by the *EventId* parameter of [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) methods.</span></span>

</dd> <dt>

<span data-ttu-id="e0870-115">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0870-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0870-116">Um **or** lógico de um ou ambos os sinalizadores a seguir, especificando a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="e0870-116">A logical **OR** of one or both of the following flags, specifying what action to perform.</span></span> <span data-ttu-id="e0870-117">Esse valor é recuperado do parâmetro *pdwStatus* de [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="e0870-117">This value is retrieved from the *pdwStatus* parameter of [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span> <span data-ttu-id="e0870-118">Você pode usar o sinalizador *pdwStatus* diretamente.</span><span class="sxs-lookup"><span data-stu-id="e0870-118">You can use the *pdwStatus* flag directly.</span></span>



| <span data-ttu-id="e0870-119">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="e0870-119">Flag</span></span>                        | <span data-ttu-id="e0870-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0870-120">Description</span></span>                                   |
|-----------------------------|-----------------------------------------------|
| <span data-ttu-id="e0870-121">\_NEEDCLOCK de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="e0870-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="e0870-122">Adquira um relógio de um servidor de clock seguro.</span><span class="sxs-lookup"><span data-stu-id="e0870-122">Acquire a clock from a secure clock server.</span></span>   |
| <span data-ttu-id="e0870-123">\_REFRESHCLOCK de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="e0870-123">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="e0870-124">Atualize o relógio de um servidor de relógio seguro.</span><span class="sxs-lookup"><span data-stu-id="e0870-124">Refresh the clock from a secure clock server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e0870-125">*pdwStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0870-125">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0870-126">Um dos valores **DWORD** a seguir que especificam o status retornado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0870-126">One of the following **DWORD** values specifying the status returned by the device.</span></span>



| <span data-ttu-id="e0870-127">Status</span><span class="sxs-lookup"><span data-stu-id="e0870-127">Status</span></span> | <span data-ttu-id="e0870-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0870-128">Description</span></span>                                                     |
|--------|-----------------------------------------------------------------|
| <span data-ttu-id="e0870-129">0</span><span class="sxs-lookup"><span data-stu-id="e0870-129">0</span></span>      | <span data-ttu-id="e0870-130">Não há suporte para a ação.</span><span class="sxs-lookup"><span data-stu-id="e0870-130">The action is not supported.</span></span>                                    |
| <span data-ttu-id="e0870-131">1</span><span class="sxs-lookup"><span data-stu-id="e0870-131">1</span></span>      | <span data-ttu-id="e0870-132">O relógio de segurança do dispositivo não pôde ser adquirido do serviço.</span><span class="sxs-lookup"><span data-stu-id="e0870-132">The device secure clock could not be acquired from the service.</span></span> |
| <span data-ttu-id="e0870-133">2</span><span class="sxs-lookup"><span data-stu-id="e0870-133">2</span></span>      | <span data-ttu-id="e0870-134">Não foi possível definir o Clock seguro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0870-134">The device's secure clock could not be set.</span></span>                     |
| <span data-ttu-id="e0870-135">3</span><span class="sxs-lookup"><span data-stu-id="e0870-135">3</span></span>      | <span data-ttu-id="e0870-136">O clock de segurança do dispositivo foi definido.</span><span class="sxs-lookup"><span data-stu-id="e0870-136">The device's secure clock was set.</span></span>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0870-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0870-137">Return value</span></span>

<span data-ttu-id="e0870-138">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e0870-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e0870-139">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0870-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e0870-140">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0870-140">Return code</span></span>                                                                                                                             | <span data-ttu-id="e0870-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0870-141">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0870-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-142"><dt>**S\_OK**</dt></span></span> </dl>                                                    | <span data-ttu-id="e0870-143">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e0870-143">The method succeeded.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="e0870-144"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-144"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                                       | <span data-ttu-id="e0870-145">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="e0870-145">One or more arguments are not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="e0870-146"><dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-146"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>                        | <span data-ttu-id="e0870-147">O dispositivo especificado não é um dispositivo compatível com DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e0870-147">The specified device is not a Windows Media DRM compatible device.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="e0870-148"><dt>**o NS \_ E \_ DRM \_ não consegue \_ obter o \_ \_ \_ Clock seguro**</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-148"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="e0870-149">Falha ao recuperar o desafio de relógio seguro do dispositivo ou não foi possível recuperar a URL do clock seguro do desafio.</span><span class="sxs-lookup"><span data-stu-id="e0870-149">Failed to retrieve secure clock challenge from the device or unable to retrieve the secure clock URL from the challenge.</span></span><br/> |
| <dl> <span data-ttu-id="e0870-150"><dt>**o NS \_ E \_ DRM \_ não pode \_ obter o \_ \_ relógio seguro \_ \_ do \_ servidor**</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-150"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK\_FROM\_SERVER**</dt></span></span> </dl> | <span data-ttu-id="e0870-151">Falha ao recuperar a resposta do relógio seguro do servidor do clock seguro.</span><span class="sxs-lookup"><span data-stu-id="e0870-151">Failed to retrieve the secure clock response from the secure clock server.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e0870-152"><dt>**o NS \_ E \_ DRM \_ não pode \_ definir o \_ \_ \_ relógio seguro**</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-152"><dt>**NS\_E\_DRM\_UNABLE\_TO\_SET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="e0870-153">Falha ao enviar o desafio de relógio seguro para o dispositivo ou o dispositivo não pôde definir o relógio.</span><span class="sxs-lookup"><span data-stu-id="e0870-153">Failed to send the secure clock challenge to the device, or the device failed to set the clock.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="e0870-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0870-154">Remarks</span></span>

<span data-ttu-id="e0870-155">Este é um método assíncrono; o dispositivo deve aguardar o retorno de chamada [**IWMDMProgress:: End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) para esta operação antes de tentar reproduzir qualquer conteúdo licenciado.</span><span class="sxs-lookup"><span data-stu-id="e0870-155">This is an asynchronous method; the device must await the [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) callback for this operation before attempting to play any licensed content.</span></span>

<span data-ttu-id="e0870-156">Um aplicativo pode saber se o dispositivo deve ter seu relógio redefinido ou atualizado chamando [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="e0870-156">An application can learn if the device must have its clock reset or updated by calling [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span>

<span data-ttu-id="e0870-157">Seu aplicativo deve ter uma conexão com a Internet para habilitá-lo a adquirir ou redefinir um relógio seguro.</span><span class="sxs-lookup"><span data-stu-id="e0870-157">Your application must have an Internet connection to enable it to acquire or reset a secure clock.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0870-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0870-158">Requirements</span></span>



| <span data-ttu-id="e0870-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0870-159">Requirement</span></span> | <span data-ttu-id="e0870-160">Valor</span><span class="sxs-lookup"><span data-stu-id="e0870-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0870-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0870-161">Header</span></span><br/>  | <dl> <span data-ttu-id="e0870-162"><dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-162"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="e0870-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0870-163">Library</span></span><br/> | <dl> <span data-ttu-id="e0870-164"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0870-164"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="e0870-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0870-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0870-166">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="e0870-166">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="e0870-167">**Interface IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="e0870-167">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="e0870-168">**Interface IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="e0870-168">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="e0870-169">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="e0870-169">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





