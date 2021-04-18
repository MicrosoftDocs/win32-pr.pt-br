---
description: O \_ comando de formato de armazenamento de comando WPD \_ \_ formata um objeto funcional de armazenamento no dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: WPD_COMMAND_STORAGE_FORMAT comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748678"
---
# <a name="wpd_command_storage_format-command"></a><span data-ttu-id="f1623-103">\_Comando de \_ formato de armazenamento de comando WPD \_</span><span class="sxs-lookup"><span data-stu-id="f1623-103">WPD\_COMMAND\_STORAGE\_FORMAT Command</span></span>

<span data-ttu-id="f1623-104">O comando de **\_ formato de \_ armazenamento \_ de comando WPD** formata um objeto funcional de armazenamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1623-104">The **WPD\_COMMAND\_STORAGE\_FORMAT** command formats a storage functional object on the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="f1623-105">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="f1623-105">Command category</span></span>

<span data-ttu-id="f1623-106">**\_armazenamento de categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f1623-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="f1623-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1623-107">Parameters</span></span>

<span data-ttu-id="f1623-108">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f1623-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="f1623-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1623-109">Parameter</span></span>                          | <span data-ttu-id="f1623-110">VarType</span><span class="sxs-lookup"><span data-stu-id="f1623-110">VarType</span></span>    | <span data-ttu-id="f1623-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1623-111">Description</span></span>                                              |
|------------------------------------|------------|----------------------------------------------------------|
| <span data-ttu-id="f1623-112">\_ID do \_ objeto de armazenamento de propriedade WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1623-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="f1623-113">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="f1623-113">VT\_LPWSTR</span></span> | <span data-ttu-id="f1623-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f1623-114">Required.</span></span> <span data-ttu-id="f1623-115">A ID de objeto do meio de armazenamento a ser formatado.</span><span class="sxs-lookup"><span data-stu-id="f1623-115">The object ID of the storage medium to format.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="f1623-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f1623-116">Return Value</span></span>

<span data-ttu-id="f1623-117">O driver deve retornar os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="f1623-117">The driver should return the following results.</span></span>



| <span data-ttu-id="f1623-118">Resultado</span><span class="sxs-lookup"><span data-stu-id="f1623-118">Result</span></span>                                         | <span data-ttu-id="f1623-119">VarType</span><span class="sxs-lookup"><span data-stu-id="f1623-119">VarType</span></span>   | <span data-ttu-id="f1623-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1623-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1623-121">**\_ \_ HRESULT comum de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f1623-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="f1623-122">erro de VT \_</span><span class="sxs-lookup"><span data-stu-id="f1623-122">VT\_ERROR</span></span> | <span data-ttu-id="f1623-123">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f1623-123">Required.</span></span> <span data-ttu-id="f1623-124">Um **HRESULT** que indica êxito ou falha ao executar o comando.</span><span class="sxs-lookup"><span data-stu-id="f1623-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="f1623-125">Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="f1623-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="f1623-126">Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados.</span><span class="sxs-lookup"><span data-stu-id="f1623-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="f1623-127">**\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f1623-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="f1623-128">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="f1623-128">VT\_UI4</span></span>   | <span data-ttu-id="f1623-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f1623-129">Optional.</span></span> <span data-ttu-id="f1623-130">Um código de erro específico do driver.</span><span class="sxs-lookup"><span data-stu-id="f1623-130">A driver-specific error code.</span></span> <span data-ttu-id="f1623-131">Normalmente, isso é usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.</span><span class="sxs-lookup"><span data-stu-id="f1623-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="f1623-132">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="f1623-132">Calling Methods</span></span>

<span data-ttu-id="f1623-133">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="f1623-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1623-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1623-134">Requirements</span></span>



| <span data-ttu-id="f1623-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1623-135">Requirement</span></span> | <span data-ttu-id="f1623-136">Valor</span><span class="sxs-lookup"><span data-stu-id="f1623-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1623-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1623-137">Header</span></span><br/> | <dl> <span data-ttu-id="f1623-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1623-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1623-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1623-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1623-140">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="f1623-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




