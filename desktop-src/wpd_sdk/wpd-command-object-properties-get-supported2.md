---
description: Recupera as propriedades com suporte por um objeto.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764976"
---
# <a name="wpd_command_object_properties_get_supported-command"></a><span data-ttu-id="268fa-103">\_As propriedades do objeto de comando WPD \_ recebem o \_ \_ \_ comando com suporte</span><span class="sxs-lookup"><span data-stu-id="268fa-103">WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED Command</span></span>

<span data-ttu-id="268fa-104">O **comando \_ \_ \_ \_ \_ com suporte das propriedades do objeto de comando WPD** recupera as propriedades com suporte de um objeto.</span><span class="sxs-lookup"><span data-stu-id="268fa-104">The **WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED** command retrieves the properties supported by an object.</span></span>

## <a name="command-category"></a><span data-ttu-id="268fa-105">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="268fa-105">Command Category</span></span>

<span data-ttu-id="268fa-106">**\_Propriedades do \_ objeto de categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="268fa-106">**WPD\_CATEGORY\_OBJECT\_PROPERTIES**</span></span>

## <a name="parameters"></a><span data-ttu-id="268fa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="268fa-107">Parameters</span></span>

<span data-ttu-id="268fa-108">O driver espera o seguinte parâmetro.</span><span class="sxs-lookup"><span data-stu-id="268fa-108">The driver expects the following parameter.</span></span>



| <span data-ttu-id="268fa-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="268fa-109">Parameter</span></span>                                         | <span data-ttu-id="268fa-110">VarType</span><span class="sxs-lookup"><span data-stu-id="268fa-110">VarType</span></span>        | <span data-ttu-id="268fa-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="268fa-111">Description</span></span>                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="268fa-112">**\_ID do \_ objeto de propriedades do objeto de propriedade WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="268fa-112">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_OBJECT\_ID**</span></span> | <span data-ttu-id="268fa-113">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="268fa-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="268fa-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="268fa-114">Required.</span></span> <span data-ttu-id="268fa-115">A ID do objeto que contém as propriedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="268fa-115">The ID of the object that contains the requested properties.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="268fa-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="268fa-116">Return Value</span></span>

<span data-ttu-id="268fa-117">O driver deve retornar os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="268fa-117">The driver should return the following results.</span></span>



| <span data-ttu-id="268fa-118">Resultado</span><span class="sxs-lookup"><span data-stu-id="268fa-118">Result</span></span>                                                | <span data-ttu-id="268fa-119">VarType</span><span class="sxs-lookup"><span data-stu-id="268fa-119">VarType</span></span>         | <span data-ttu-id="268fa-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="268fa-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="268fa-121">**\_chaves de \_ propriedade de propriedades do objeto de propriedade WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="268fa-121">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_PROPERTY\_KEYS**</span></span> | <span data-ttu-id="268fa-122">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="268fa-122">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="268fa-123">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="268fa-123">Required.</span></span> <span data-ttu-id="268fa-124">Uma interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que especifica todas as propriedades com suporte.</span><span class="sxs-lookup"><span data-stu-id="268fa-124">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that specifies all of the supported properties.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="268fa-125">**\_ \_ HRESULT comum de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="268fa-125">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                    | <span data-ttu-id="268fa-126">**erro de VT \_**</span><span class="sxs-lookup"><span data-stu-id="268fa-126">**VT\_ERROR**</span></span>   | <span data-ttu-id="268fa-127">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="268fa-127">Required.</span></span> <span data-ttu-id="268fa-128">Um valor **HRESULT** que indica êxito ou falha geral.</span><span class="sxs-lookup"><span data-stu-id="268fa-128">An **HRESULT** value that indicates overall success or failure.</span></span> <span data-ttu-id="268fa-129">Os possíveis valores de resultado incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="268fa-129">Possible result values include [Windows Portable Devices error codes](error-constants.md).</span></span> <span data-ttu-id="268fa-130">Se o chamador fizer uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 ( \_ não \_ há suporte para o erro)** , mas, caso contrário, não será necessário retornar nenhum outro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="268fa-130">If the caller makes an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** but is otherwise not required to return any other result value.</span></span> |
| <span data-ttu-id="268fa-131">**\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="268fa-131">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>        | <span data-ttu-id="268fa-132">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="268fa-132">**VT\_UI4**</span></span>     | <span data-ttu-id="268fa-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="268fa-133">Optional.</span></span> <span data-ttu-id="268fa-134">Um código de erro específico do driver.</span><span class="sxs-lookup"><span data-stu-id="268fa-134">A driver-specific error code.</span></span> <span data-ttu-id="268fa-135">Isso é normalmente usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.</span><span class="sxs-lookup"><span data-stu-id="268fa-135">This is typically used only for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="268fa-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="268fa-136">Requirements</span></span>



| <span data-ttu-id="268fa-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="268fa-137">Requirement</span></span> | <span data-ttu-id="268fa-138">Valor</span><span class="sxs-lookup"><span data-stu-id="268fa-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="268fa-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="268fa-139">Header</span></span><br/> | <dl> <span data-ttu-id="268fa-140"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="268fa-140"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="268fa-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="268fa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268fa-142">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="268fa-142">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




