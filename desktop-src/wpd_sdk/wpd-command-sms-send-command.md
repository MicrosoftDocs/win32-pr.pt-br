---
description: O comando \_ de \_ envio de SMS do comando WPD \_ inicia o envio de uma mensagem SMS (Short Message Service) por um objeto funcional do SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: WPD_COMMAND_SMS_SEND comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790238"
---
# <a name="wpd_command_sms_send-command"></a><span data-ttu-id="c62ea-103">Comando \_ de \_ envio de SMS de comandos WPD \_</span><span class="sxs-lookup"><span data-stu-id="c62ea-103">WPD\_COMMAND\_SMS\_SEND Command</span></span>

<span data-ttu-id="c62ea-104">O comando de **\_ envio de \_ SMS \_ do comando WPD** inicia o envio de uma mensagem SMS (Short Message Service) por um objeto funcional do SMS.</span><span class="sxs-lookup"><span data-stu-id="c62ea-104">The **WPD\_COMMAND\_SMS\_SEND** command initiates the sending of a short message service (SMS) message by an SMS functional object.</span></span>

## <a name="command-category"></a><span data-ttu-id="c62ea-105">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="c62ea-105">Command category</span></span>

<span data-ttu-id="c62ea-106">**Categoria de WPD do \_ \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="c62ea-106">**WPD\_CATEGORY\_SMS**</span></span>

## <a name="parameters"></a><span data-ttu-id="c62ea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c62ea-107">Parameters</span></span>

<span data-ttu-id="c62ea-108">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c62ea-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="c62ea-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c62ea-109">Parameter</span></span>                              | <span data-ttu-id="c62ea-110">VarType</span><span class="sxs-lookup"><span data-stu-id="c62ea-110">VarType</span></span>             | <span data-ttu-id="c62ea-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c62ea-111">Description</span></span>                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62ea-112">\_destino de \_ \_ comando comum de propriedade \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c62ea-112">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="c62ea-113">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="c62ea-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="c62ea-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c62ea-114">Required.</span></span> <span data-ttu-id="c62ea-115">A ID de objeto do objeto funcional do SMS que deve enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c62ea-115">The object ID of the SMS functional object that should send the message.</span></span> <span data-ttu-id="c62ea-116">Diferentes objetos funcionais do SMS podem ter configurações diferentes.</span><span class="sxs-lookup"><span data-stu-id="c62ea-116">Different SMS functional objects can have different settings.</span></span>                                                                                     |
| <span data-ttu-id="c62ea-117">\_destinatário de \_ SMS da propriedade WPD \_</span><span class="sxs-lookup"><span data-stu-id="c62ea-117">WPD\_PROPERTY\_SMS\_RECIPIENT</span></span>          | <span data-ttu-id="c62ea-118">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="c62ea-118">VT\_LPWSTR</span></span>          | <span data-ttu-id="c62ea-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c62ea-119">Required.</span></span> <span data-ttu-id="c62ea-120">O URI do destinatário.</span><span class="sxs-lookup"><span data-stu-id="c62ea-120">The URI of the recipient.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="c62ea-121">\_tipo de \_ \_ mensagem SMS da propriedade \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c62ea-121">WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE</span></span>      | <span data-ttu-id="c62ea-122">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="c62ea-122">VT\_UI4</span></span>             | <span data-ttu-id="c62ea-123">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c62ea-123">Required.</span></span> <span data-ttu-id="c62ea-124">Um enumerador de [**\_ \_ tipos de mensagem SMS**](sms-message-types.md) que indica o tipo de mensagem (texto ou binário).</span><span class="sxs-lookup"><span data-stu-id="c62ea-124">An [**SMS\_MESSAGE\_TYPES**](sms-message-types.md) enumerator that indicates the type of message (text or binary).</span></span>                                                                                                        |
| <span data-ttu-id="c62ea-125">\_mensagem de \_ \_ texto SMS da propriedade \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c62ea-125">WPD\_PROPERTY\_SMS\_TEXT\_MESSAGE</span></span>      | <span data-ttu-id="c62ea-126">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="c62ea-126">VT\_LPWSTR</span></span>          | <span data-ttu-id="c62ea-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c62ea-127">Optional.</span></span> <span data-ttu-id="c62ea-128">Se **o \_ \_ tipo de \_ mensagem \_ de SMS de propriedade WPD** indicar uma mensagem de texto, essa será a cadeia de caracteres de mensagem; caso contrário, esse parâmetro não será incluído.</span><span class="sxs-lookup"><span data-stu-id="c62ea-128">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a text message, this is the message string; otherwise, this parameter is not included.</span></span>                                                                                  |
| <span data-ttu-id="c62ea-129">\_mensagem de \_ binário de SMS de propriedade WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c62ea-129">WPD\_PROPERTY\_SMS\_BINARY\_MESSAGE</span></span>    | <span data-ttu-id="c62ea-130">\_UI1 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="c62ea-130">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="c62ea-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c62ea-131">Optional.</span></span> <span data-ttu-id="c62ea-132">Se **o \_ \_ tipo de \_ mensagem \_ de SMS de propriedade WPD** indicar uma mensagem binária, esse será um ponteiro para uma matriz de bytes; caso contrário, esse parâmetro não será incluído.</span><span class="sxs-lookup"><span data-stu-id="c62ea-132">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a binary message, this is a pointer to an array of bytes; otherwise, this parameter is not included.</span></span> <span data-ttu-id="c62ea-133">A primeira DWORD do valor é o comprimento da matriz, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c62ea-133">The first DWORD of the value is the length of the array, in bytes.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="c62ea-134">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c62ea-134">Return Value</span></span>

<span data-ttu-id="c62ea-135">O driver deve retornar os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="c62ea-135">The driver should return the following results.</span></span>



| <span data-ttu-id="c62ea-136">Resultado</span><span class="sxs-lookup"><span data-stu-id="c62ea-136">Result</span></span>                                         | <span data-ttu-id="c62ea-137">VarType</span><span class="sxs-lookup"><span data-stu-id="c62ea-137">VarType</span></span>   | <span data-ttu-id="c62ea-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="c62ea-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62ea-139">**\_ \_ HRESULT comum de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c62ea-139">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="c62ea-140">erro de VT \_</span><span class="sxs-lookup"><span data-stu-id="c62ea-140">VT\_ERROR</span></span> | <span data-ttu-id="c62ea-141">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c62ea-141">Required.</span></span> <span data-ttu-id="c62ea-142">Um **HRESULT** que indica êxito ou falha ao executar o comando.</span><span class="sxs-lookup"><span data-stu-id="c62ea-142">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="c62ea-143">Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="c62ea-143">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="c62ea-144">Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados.</span><span class="sxs-lookup"><span data-stu-id="c62ea-144">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="c62ea-145">**\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c62ea-145">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="c62ea-146">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="c62ea-146">VT\_UI4</span></span>   | <span data-ttu-id="c62ea-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c62ea-147">Optional.</span></span> <span data-ttu-id="c62ea-148">Um código de erro específico do driver.</span><span class="sxs-lookup"><span data-stu-id="c62ea-148">A driver-specific error code.</span></span> <span data-ttu-id="c62ea-149">Normalmente, isso é usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.</span><span class="sxs-lookup"><span data-stu-id="c62ea-149">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="c62ea-150">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="c62ea-150">Calling Methods</span></span>

<span data-ttu-id="c62ea-151">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="c62ea-151">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="c62ea-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c62ea-152">Requirements</span></span>



| <span data-ttu-id="c62ea-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="c62ea-153">Requirement</span></span> | <span data-ttu-id="c62ea-154">Valor</span><span class="sxs-lookup"><span data-stu-id="c62ea-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62ea-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c62ea-155">Header</span></span><br/> | <dl> <span data-ttu-id="c62ea-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c62ea-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62ea-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="c62ea-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62ea-158">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="c62ea-158">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




