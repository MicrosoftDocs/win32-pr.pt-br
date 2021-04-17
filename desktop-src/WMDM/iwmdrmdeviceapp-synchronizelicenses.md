---
title: Método IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: O método SynchronizeLicenses atualiza licenças em um dispositivo quando elas estão próximas de expirar.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Método SynchronizeLicenses Windows Media Gerenciador de Dispositivos
- Método SynchronizeLicenses Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783648"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a><span data-ttu-id="6af61-106">Método IWMDRMDeviceApp:: SynchronizeLicenses</span><span class="sxs-lookup"><span data-stu-id="6af61-106">IWMDRMDeviceApp::SynchronizeLicenses method</span></span>

<span data-ttu-id="6af61-107">O método **SynchronizeLicenses** atualiza licenças em um dispositivo quando elas estão próximas de expirar.</span><span class="sxs-lookup"><span data-stu-id="6af61-107">The **SynchronizeLicenses** method updates licenses on a device when they are close to expiring.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af61-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6af61-108">Syntax</span></span>


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a><span data-ttu-id="6af61-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6af61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af61-110">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6af61-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af61-111">Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="6af61-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="6af61-112">*pProgressCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6af61-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af61-113">O retorno de chamada de progresso que receberá o progresso de todas as etapas que talvez precisem ser executadas. A etapa é identificada pelo parâmetro *EventID* do método [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) chamado.</span><span class="sxs-lookup"><span data-stu-id="6af61-113">Progress callback that will receive progress of any steps that it might need to carry out. The step is identified by the *EventId* parameter of the [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) method called.</span></span>

</dd> <dt>

<span data-ttu-id="6af61-114">*cMinCountThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6af61-114">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af61-115">Contagem mínima opcional de execuções pendentes em uma licença de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6af61-115">Optional minimum remaining play count on a device license.</span></span>

</dd> <dt>

<span data-ttu-id="6af61-116">*cMinHoursThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6af61-116">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af61-117">Mínimo opcional de horas restantes em uma licença de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6af61-117">Optional minimum remaining hours on a device license.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af61-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6af61-118">Return value</span></span>

<span data-ttu-id="6af61-119">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6af61-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6af61-120">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6af61-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6af61-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6af61-121">Return code</span></span>                                                                                                         | <span data-ttu-id="6af61-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6af61-122">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6af61-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-123"><dt>**S\_OK**</dt></span></span> </dl>                                | <span data-ttu-id="6af61-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6af61-124">The method succeeded.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="6af61-125"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-125"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="6af61-126">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="6af61-126">One or more arguments are not valid.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="6af61-127"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-127"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>                | <span data-ttu-id="6af61-128">O XML está formado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="6af61-128">XML is improperly formed.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="6af61-129"><dt>**DRM \_ E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-129"><dt>**DRM\_E\_NOTIMPL**</dt></span></span> </dl>                      | <span data-ttu-id="6af61-130">Essa funcionalidade não está implementada no momento.</span><span class="sxs-lookup"><span data-stu-id="6af61-130">This functionality is not currently implemented.</span></span> <span data-ttu-id="6af61-131">(SyncLicenses w/ *pDevice* = NULL)</span><span class="sxs-lookup"><span data-stu-id="6af61-131">(SyncLicenses w/ *pDevice* =NULL)</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6af61-132"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-132"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>                | <span data-ttu-id="6af61-133">O XML de licença foi formado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="6af61-133">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="6af61-134"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-134"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>                 | <span data-ttu-id="6af61-135">O XML de licença foi formado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="6af61-135">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="6af61-136"><dt>**o DRM \_ E a \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-136"><dt>**DRM\_E\_OUTOFMEMORY**</dt></span></span> </dl>                  | <span data-ttu-id="6af61-137">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="6af61-137">Out of memory.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="6af61-138"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-138"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>                  | <span data-ttu-id="6af61-139">Falha ao localizar uma marca XML necessária na licença.</span><span class="sxs-lookup"><span data-stu-id="6af61-139">Failed to find a required XML tag in the license.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6af61-140"><dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-140"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>    | <span data-ttu-id="6af61-141">O dispositivo especificado não é um dispositivo compatível com o Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="6af61-141">The specified device is not a Windows Media DRM-compatible device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="6af61-142"><dt>**o NS \_ E \_ DRM precisa de \_ \_ individualização**</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-142"><dt>**NS\_E\_DRM\_NEEDS\_INDIVIDUALIZATION**</dt></span></span> </dl> | <span data-ttu-id="6af61-143">O DRM requer uma caixa preta individual para executar essa função.</span><span class="sxs-lookup"><span data-stu-id="6af61-143">The DRM requires an individualized black box to perform this function.</span></span> <span data-ttu-id="6af61-144">Em outras palavras, o SDK do Windows Media format requer uma atualização de segurança.</span><span class="sxs-lookup"><span data-stu-id="6af61-144">In other words, the Windows Media Format SDK requires a security upgrade.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6af61-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="6af61-145">Remarks</span></span>

<span data-ttu-id="6af61-146">Essa chamada só pode ser feita em um dispositivo que ofereça suporte ao Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="6af61-146">This call can only be made on a device that supports Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="6af61-147">Você deve especificar pelo menos um parâmetro de limite.</span><span class="sxs-lookup"><span data-stu-id="6af61-147">You must specify at least one threshold parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af61-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6af61-148">Requirements</span></span>



| <span data-ttu-id="6af61-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af61-149">Requirement</span></span> | <span data-ttu-id="6af61-150">Valor</span><span class="sxs-lookup"><span data-stu-id="6af61-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af61-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6af61-151">Header</span></span><br/>  | <dl> <span data-ttu-id="6af61-152"><dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-152"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="6af61-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6af61-153">Library</span></span><br/> | <dl> <span data-ttu-id="6af61-154"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6af61-154"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="6af61-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="6af61-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af61-156">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="6af61-156">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="6af61-157">**Interface IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="6af61-157">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="6af61-158">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="6af61-158">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





