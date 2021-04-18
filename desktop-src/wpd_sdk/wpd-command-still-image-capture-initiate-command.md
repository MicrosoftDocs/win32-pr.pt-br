---
description: O comando \_ WPD \_ ainda \_ o \_ \_ comando Iniciar captura de imagem inicia uma captura de imagem ainda por um objeto funcional de imagem ainda. Se um novo objeto for criado como resultado de tirar uma foto, o driver deverá enviar o evento de \_ evento \_ adicionado do WPD \_ .
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796279"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a><span data-ttu-id="8ac46-104">Comando \_ WPD \_ ainda \_ \_ \_ comando Iniciar captura de imagem</span><span class="sxs-lookup"><span data-stu-id="8ac46-104">WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE Command</span></span>

<span data-ttu-id="8ac46-105">O comando **WPD ainda o comando \_ \_ \_ \_ \_ Iniciar captura de imagem** inicia uma captura de imagem ainda por um objeto funcional de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="8ac46-105">The **WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE** command initiates a still image capture by a still image functional object.</span></span> <span data-ttu-id="8ac46-106">Se um novo objeto for criado como resultado de tirar uma foto, o driver deverá enviar o evento **de \_ evento \_ \_ adicionado do WPD** .</span><span class="sxs-lookup"><span data-stu-id="8ac46-106">If a new object is created as a result of taking a picture, the driver should send the **WPD\_EVENT\_OBJECT\_ADDED** event.</span></span>

## <a name="command-category"></a><span data-ttu-id="8ac46-107">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="8ac46-107">Command category</span></span>

<span data-ttu-id="8ac46-108">**a \_ categoria \_ WPD \_ ainda \_ captura de imagem**</span><span class="sxs-lookup"><span data-stu-id="8ac46-108">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span>

## <a name="parameters"></a><span data-ttu-id="8ac46-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ac46-109">Parameters</span></span>

<span data-ttu-id="8ac46-110">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8ac46-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="8ac46-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ac46-111">Parameter</span></span>                              | <span data-ttu-id="8ac46-112">VarType</span><span class="sxs-lookup"><span data-stu-id="8ac46-112">VarType</span></span>    | <span data-ttu-id="8ac46-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ac46-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac46-114">\_destino de \_ \_ comando comum de propriedade \_ WPD</span><span class="sxs-lookup"><span data-stu-id="8ac46-114">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="8ac46-115">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="8ac46-115">VT\_LPWSTR</span></span> | <span data-ttu-id="8ac46-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8ac46-116">Required.</span></span> <span data-ttu-id="8ac46-117">A ID de objeto do objeto funcional de captura de imagem ainda no dispositivo que deve assumir a imagem. Cada objeto funcional de captura de imagem ainda pode ter configurações diferentes e pode se referir a um hardware diferente em um dispositivo (por exemplo, uma câmera frontal ou traseira de um telefone) e esse parâmetro indica qual deles usar.</span><span class="sxs-lookup"><span data-stu-id="8ac46-117">The object ID of the still image capture functional object on the device that should take the picture.Each still image capture functional object can have different settings, and may refer to different hardware on a device (for example, a front or back camera of a phone), and this parameter indicates which one to use.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8ac46-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8ac46-118">Return Value</span></span>

<span data-ttu-id="8ac46-119">O driver deve retornar os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="8ac46-119">The driver should return the following results.</span></span>



| <span data-ttu-id="8ac46-120">Resultado</span><span class="sxs-lookup"><span data-stu-id="8ac46-120">Result</span></span>                                         | <span data-ttu-id="8ac46-121">VarType</span><span class="sxs-lookup"><span data-stu-id="8ac46-121">VarType</span></span>   | <span data-ttu-id="8ac46-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ac46-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac46-123">**\_ \_ HRESULT comum de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8ac46-123">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="8ac46-124">erro de VT \_</span><span class="sxs-lookup"><span data-stu-id="8ac46-124">VT\_ERROR</span></span> | <span data-ttu-id="8ac46-125">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8ac46-125">Required.</span></span> <span data-ttu-id="8ac46-126">Um **HRESULT** que indica êxito ou falha ao executar o comando.</span><span class="sxs-lookup"><span data-stu-id="8ac46-126">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="8ac46-127">Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="8ac46-127">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="8ac46-128">Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados.</span><span class="sxs-lookup"><span data-stu-id="8ac46-128">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="8ac46-129">**\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8ac46-129">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="8ac46-130">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="8ac46-130">VT\_UI4</span></span>   | <span data-ttu-id="8ac46-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8ac46-131">Optional.</span></span> <span data-ttu-id="8ac46-132">Um código de erro específico do driver.</span><span class="sxs-lookup"><span data-stu-id="8ac46-132">A driver-specific error code.</span></span> <span data-ttu-id="8ac46-133">Esse valor normalmente é usado por fornecedores de dispositivo para melhorar o diagnóstico de erros de dispositivo ao usar seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8ac46-133">This value is typically used by device vendors to improve diagnosis of device errors while using their applications.</span></span> <span data-ttu-id="8ac46-134">Os aplicativos de uso geral podem ignorá-lo e confiar exclusivamente na \_ Propriedade WPD \_ comum \_ HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8ac46-134">General purpose applications would ignore it and rely solely on WPD\_PROPERTY\_COMMON\_HRESULT instead.</span></span>                                                                                                                   |



 

## <a name="calling-methods"></a><span data-ttu-id="8ac46-135">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="8ac46-135">Calling Methods</span></span>

<span data-ttu-id="8ac46-136">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="8ac46-136">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac46-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ac46-137">Requirements</span></span>



| <span data-ttu-id="8ac46-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ac46-138">Requirement</span></span> | <span data-ttu-id="8ac46-139">Valor</span><span class="sxs-lookup"><span data-stu-id="8ac46-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac46-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ac46-140">Header</span></span><br/> | <dl> <span data-ttu-id="8ac46-141"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac46-141"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac46-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ac46-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac46-143">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="8ac46-143">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




