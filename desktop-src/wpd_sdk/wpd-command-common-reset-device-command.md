---
description: O comando \_ do \_ dispositivo de redefinição comum de comandos WPD \_ \_ redefine o dispositivo. Isso não significa reformatação; é equivalente a desligar e ligar o dispositivo novamente.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: WPD_COMMAND_COMMON_RESET_DEVICE comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760675"
---
# <a name="wpd_command_common_reset_device-command"></a><span data-ttu-id="842b0-104">Comando \_ de \_ \_ dispositivo de redefinição comum de comandos WPD \_</span><span class="sxs-lookup"><span data-stu-id="842b0-104">WPD\_COMMAND\_COMMON\_RESET\_DEVICE Command</span></span>

<span data-ttu-id="842b0-105">O comando do **\_ \_ \_ \_ dispositivo de redefinição comum de comandos WPD** redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="842b0-105">The **WPD\_COMMAND\_COMMON\_RESET\_DEVICE** command resets the device.</span></span> <span data-ttu-id="842b0-106">Isso não significa reformatação; é equivalente a desligar e ligar o dispositivo novamente.</span><span class="sxs-lookup"><span data-stu-id="842b0-106">This does not mean reformatting; it is equivalent to turning the device off and on again.</span></span>

## <a name="command-category"></a><span data-ttu-id="842b0-107">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="842b0-107">Command category</span></span>

<span data-ttu-id="842b0-108">**Categoria de WPD \_ \_ comum**</span><span class="sxs-lookup"><span data-stu-id="842b0-108">**WPD\_CATEGORY\_COMMON**</span></span>

## <a name="parameters"></a><span data-ttu-id="842b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="842b0-109">Parameters</span></span>

<span data-ttu-id="842b0-110">Este comando não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="842b0-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="842b0-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="842b0-111">Return Value</span></span>

<span data-ttu-id="842b0-112">O driver deve retornar os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="842b0-112">The driver should return the following results.</span></span>



| <span data-ttu-id="842b0-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="842b0-113">Result</span></span>                                         | <span data-ttu-id="842b0-114">VarType</span><span class="sxs-lookup"><span data-stu-id="842b0-114">VarType</span></span>   | <span data-ttu-id="842b0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="842b0-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="842b0-116">**\_ \_ HRESULT comum de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="842b0-116">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="842b0-117">erro de VT \_</span><span class="sxs-lookup"><span data-stu-id="842b0-117">VT\_ERROR</span></span> | <span data-ttu-id="842b0-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="842b0-118">Required.</span></span> <span data-ttu-id="842b0-119">Um **HRESULT** que indica êxito ou falha ao executar o comando.</span><span class="sxs-lookup"><span data-stu-id="842b0-119">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="842b0-120">Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="842b0-120">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="842b0-121">Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados.</span><span class="sxs-lookup"><span data-stu-id="842b0-121">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="842b0-122">**\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="842b0-122">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="842b0-123">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="842b0-123">VT\_UI4</span></span>   | <span data-ttu-id="842b0-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="842b0-124">Optional.</span></span> <span data-ttu-id="842b0-125">Um código de erro específico do driver.</span><span class="sxs-lookup"><span data-stu-id="842b0-125">A driver-specific error code.</span></span> <span data-ttu-id="842b0-126">Normalmente, isso é usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.</span><span class="sxs-lookup"><span data-stu-id="842b0-126">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="842b0-127">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="842b0-127">Calling Methods</span></span>

<span data-ttu-id="842b0-128">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="842b0-128">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="842b0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="842b0-129">Requirements</span></span>



| <span data-ttu-id="842b0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="842b0-130">Requirement</span></span> | <span data-ttu-id="842b0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="842b0-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="842b0-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="842b0-132">Header</span></span><br/> | <dl> <span data-ttu-id="842b0-133"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="842b0-133"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842b0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="842b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842b0-135">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="842b0-135">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




