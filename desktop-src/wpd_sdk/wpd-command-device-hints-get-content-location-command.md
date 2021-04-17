---
description: O comando \_ \_ obter dicas de dispositivo de comando para \_ \_ obter \_ local do conteúdo \_ recupera as IDs de objeto das pastas que podem conter um objeto de um tipo especificado.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782718"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a><span data-ttu-id="91170-103">Comando de \_ dicas de dispositivo de comando WPD \_ \_ \_ obter \_ local do conteúdo \_</span><span class="sxs-lookup"><span data-stu-id="91170-103">WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION Command</span></span>

<span data-ttu-id="91170-104">O **comando \_ obter dicas de dispositivo de comando para \_ \_ \_ obter \_ \_ local do conteúdo** recupera as IDs de objeto das pastas que podem conter um objeto de um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="91170-104">The **WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION** command retrieves the object IDs of folders that can hold an object of a specified type.</span></span> <span data-ttu-id="91170-105">Esse comando é fornecido como uma maneira mais rápida para um cliente descobrir onde um dispositivo armazena objetos específicos do que pela enumeração de objeto bruta.</span><span class="sxs-lookup"><span data-stu-id="91170-105">This command is provided as a faster way for a client to discover where a device stores specific objects than by brute object enumeration.</span></span>

## <a name="command-category"></a><span data-ttu-id="91170-106">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="91170-106">Command category</span></span>

<span data-ttu-id="91170-107">**\_dicas de \_ dispositivo de categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="91170-107">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>

## <a name="parameters"></a><span data-ttu-id="91170-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91170-108">Parameters</span></span>

<span data-ttu-id="91170-109">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="91170-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="91170-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="91170-110">Parameter</span></span>                                   | <span data-ttu-id="91170-111">VarType</span><span class="sxs-lookup"><span data-stu-id="91170-111">VarType</span></span>   | <span data-ttu-id="91170-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="91170-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91170-113">\_tipo de \_ conteúdo de dicas de dispositivo de propriedade WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="91170-113">WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_TYPE</span></span> | <span data-ttu-id="91170-114">CLSID do VT \_</span><span class="sxs-lookup"><span data-stu-id="91170-114">VT\_CLSID</span></span> | <span data-ttu-id="91170-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="91170-115">Required.</span></span> <span data-ttu-id="91170-116">O tipo de objeto para o qual o chamador deseja localizar o contêiner.</span><span class="sxs-lookup"><span data-stu-id="91170-116">The object type that the caller wishes to find the container for.</span></span> <span data-ttu-id="91170-117">Por exemplo, para localizar as pastas de nível superior usadas para manter imagens em uma câmera digital, o chamador enviará uma \_ imagem de tipo de conteúdo WPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="91170-117">For example, to find the top-level folders used to hold images on a digital camera, the caller would submit WPD\_CONTENT\_TYPE\_IMAGE.</span></span> <span data-ttu-id="91170-118">Consulte [requisitos para objetos](requirements-for-objects.md) para obter uma lista de tipos de objetos definidos por dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="91170-118">See [Requirements for Objects](requirements-for-objects.md) for a list of object types defined by Windows Portable Devices.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="91170-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="91170-119">Return Value</span></span>

<span data-ttu-id="91170-120">O driver deve retornar os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="91170-120">The driver should return the following results.</span></span>



| <span data-ttu-id="91170-121">Resultado</span><span class="sxs-lookup"><span data-stu-id="91170-121">Result</span></span>                                               | <span data-ttu-id="91170-122">VarType</span><span class="sxs-lookup"><span data-stu-id="91170-122">VarType</span></span>     | <span data-ttu-id="91170-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="91170-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91170-124">**\_locais de \_ conteúdo de dicas de dispositivo de propriedade WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91170-124">**WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_LOCATIONS**</span></span> | <span data-ttu-id="91170-125">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="91170-125">VT\_UNKNOWN</span></span> | <span data-ttu-id="91170-126">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="91170-126">Required.</span></span> <span data-ttu-id="91170-127">Um [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) dos valores de LPWStr do tipo VT \_ que especificam as IDs de objeto das pastas que contêm objetos do tipo indicado pelo parâmetro de chamada.</span><span class="sxs-lookup"><span data-stu-id="91170-127">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) of type VT\_LPWSTR values that specify the object IDs of folders containing objects of the type indicated by the calling parameter.</span></span> <span data-ttu-id="91170-128">Se nenhuma pasta for encontrada, ela deverá ser uma lista vazia. As pastas indicadas pelo resultado podem ou não conter objetos de outros tipos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="91170-128">If no folders are found, this should be an empty list.The folders indicated by the result may or may not contain objects of other content types.</span></span> <span data-ttu-id="91170-129">Consulte a propriedade de [ \_ tipos de conteúdo de pasta WPD \_ \_ \_ permitida](miscellaneous-properties.md) para obter informações sobre restrições de pasta.</span><span class="sxs-lookup"><span data-stu-id="91170-129">See the [WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED](miscellaneous-properties.md) property for information on folder restrictions.</span></span><br/> |
| <span data-ttu-id="91170-130">**\_ \_ HRESULT comum de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="91170-130">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                   | <span data-ttu-id="91170-131">erro de VT \_</span><span class="sxs-lookup"><span data-stu-id="91170-131">VT\_ERROR</span></span>   | <span data-ttu-id="91170-132">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="91170-132">Required.</span></span> <span data-ttu-id="91170-133">Um **HRESULT** que indica êxito ou falha ao manipular o comando.</span><span class="sxs-lookup"><span data-stu-id="91170-133">An **HRESULT** that indicates success or failure of handling the command.</span></span> <span data-ttu-id="91170-134">Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="91170-134">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="91170-135">Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados.</span><span class="sxs-lookup"><span data-stu-id="91170-135">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="91170-136">**\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="91170-136">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>       | <span data-ttu-id="91170-137">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="91170-137">VT\_UI4</span></span>     | <span data-ttu-id="91170-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="91170-138">Optional.</span></span> <span data-ttu-id="91170-139">Um código de erro específico do driver.</span><span class="sxs-lookup"><span data-stu-id="91170-139">A driver-specific error code.</span></span> <span data-ttu-id="91170-140">Normalmente, isso é usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.</span><span class="sxs-lookup"><span data-stu-id="91170-140">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a><span data-ttu-id="91170-141">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="91170-141">Calling Methods</span></span>

<span data-ttu-id="91170-142">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="91170-142">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="91170-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91170-143">Requirements</span></span>



| <span data-ttu-id="91170-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="91170-144">Requirement</span></span> | <span data-ttu-id="91170-145">Valor</span><span class="sxs-lookup"><span data-stu-id="91170-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="91170-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91170-146">Header</span></span><br/> | <dl> <span data-ttu-id="91170-147"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="91170-147"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




