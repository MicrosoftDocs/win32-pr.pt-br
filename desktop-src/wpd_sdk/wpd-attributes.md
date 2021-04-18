---
description: Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de parâmetro para métodos e eventos de um serviço de dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Atributos de parâmetro (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793372"
---
# <a name="parameter-attributes"></a><span data-ttu-id="dd87d-103">Atributos de parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd87d-103">Parameter Attributes</span></span>

<span data-ttu-id="dd87d-104">Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de parâmetro para métodos e eventos de um serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd87d-104">For Windows 7, Windows Portable Devices supports the following parameter attributes for methods and events of a device service.</span></span> <span data-ttu-id="dd87d-105">Esses atributos são retornados pelos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="dd87d-105">These attributes are returned by the these methods:</span></span>

-   [<span data-ttu-id="dd87d-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="dd87d-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [<span data-ttu-id="dd87d-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="dd87d-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| <span data-ttu-id="dd87d-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="dd87d-108">Attribute</span></span>                                            | <span data-ttu-id="dd87d-109">VarType</span><span class="sxs-lookup"><span data-stu-id="dd87d-109">VarType</span></span>         | <span data-ttu-id="dd87d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd87d-110">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd87d-111">**\_ \_ valor padrão do atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-111">**WPD\_PARAMETER\_ATTRIBUTE\_DEFAULT\_VALUE**</span></span>        | <span data-ttu-id="dd87d-112">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="dd87d-112">VT\_*XXXX*</span></span>      | <span data-ttu-id="dd87d-113">O valor padrão do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dd87d-113">The default value of the parameter.</span></span>                                                                                                                                                         |
| <span data-ttu-id="dd87d-114">**\_elementos de \_ enumeração de atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-114">**WPD\_PARAMETER\_ATTRIBUTE\_ENUMERATION\_ELEMENTS**</span></span> | <span data-ttu-id="dd87d-115">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="dd87d-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="dd87d-116">Uma interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém os valores de enumeração para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dd87d-116">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface that contains the enumeration values for the parameter.</span></span>                                   |
| <span data-ttu-id="dd87d-117">**\_formulário de \_ atributo de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-117">**WPD\_PARAMETER\_ATTRIBUTE\_FORM**</span></span>                  | <span data-ttu-id="dd87d-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="dd87d-118">**VT\_UI4**</span></span>     | <span data-ttu-id="dd87d-119">A forma de valores de parâmetro válidos permitidos.</span><span class="sxs-lookup"><span data-stu-id="dd87d-119">The form of valid parameter values allowed.</span></span>                                                                                                                                                 |
| <span data-ttu-id="dd87d-120">**\_ \_ tamanho máximo do atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-120">**WPD\_PARAMETER\_ATTRIBUTE\_MAX\_SIZE**</span></span>             | <span data-ttu-id="dd87d-121">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="dd87d-121">**VT\_UI8**</span></span>     | <span data-ttu-id="dd87d-122">O tamanho máximo do parâmetro, em bytes.</span><span class="sxs-lookup"><span data-stu-id="dd87d-122">The maximum size of the parameter, in bytes .</span></span>                                                                                                                                               |
| <span data-ttu-id="dd87d-123">**\_nome do \_ atributo de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-123">**WPD\_PARAMETER\_ATTRIBUTE\_NAME**</span></span>                  | <span data-ttu-id="dd87d-124">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-124">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="dd87d-125">Uma cadeia de caracteres que especifica o nome amigável de script de um parâmetro de evento ou método.</span><span class="sxs-lookup"><span data-stu-id="dd87d-125">A string that specifies the script-friendly name of an event or method parameter.</span></span> <span data-ttu-id="dd87d-126">Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="dd87d-126">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span>                                                 |
| <span data-ttu-id="dd87d-127">**\_ordem de \_ atributo de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-127">**WPD\_PARAMETER\_ATTRIBUTE\_ORDER**</span></span>                 | <span data-ttu-id="dd87d-128">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="dd87d-128">**VT\_UI4**</span></span>     | <span data-ttu-id="dd87d-129">O índice de ordem de parâmetro com base em zero, para que um valor de Order igual a 0 corresponda ao primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dd87d-129">The zero-based parameter-order index, so that an order value of 0 corresponds to the first parameter.</span></span>                                                                                       |
| <span data-ttu-id="dd87d-130">**\_ \_ \_ intervalo mínimo de atributos de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-130">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MIN**</span></span>            | <span data-ttu-id="dd87d-131">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="dd87d-131">VT\_*XXXX*</span></span>      | <span data-ttu-id="dd87d-132">O valor máximo para um parâmetro do formulário intervalo de \_ formulário de atributo de parâmetro de WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dd87d-132">The maximum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="dd87d-133">**\_ \_ \_ intervalo máximo de atributos de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-133">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MAX**</span></span>            | <span data-ttu-id="dd87d-134">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="dd87d-134">VT\_*XXXX*</span></span>      | <span data-ttu-id="dd87d-135">O valor mínimo para um parâmetro do formulário intervalo de \_ formulário de atributo de parâmetro de WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dd87d-135">The minimum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="dd87d-136">**\_etapa do \_ intervalo do atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-136">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_STEP**</span></span>           | <span data-ttu-id="dd87d-137">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="dd87d-137">VT\_*XXXX*</span></span>      | <span data-ttu-id="dd87d-138">O valor de etapa para um parâmetro do formulário \_ intervalo de formulário de atributo de parâmetro WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dd87d-138">The step value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                          |
| <span data-ttu-id="dd87d-139">**\_ \_ expressão regular de atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-139">**WPD\_PARAMETER\_ATTRIBUTE\_REGULAR\_EXPRESSION**</span></span>   | <span data-ttu-id="dd87d-140">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-140">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="dd87d-141">Uma expressão regular que especifica valores aceitáveis para parâmetros da forma \_ \_ \_ \_ \_ expressão regular do formato de atributo de parâmetro de WPD.</span><span class="sxs-lookup"><span data-stu-id="dd87d-141">A regular expression that specifies acceptable values for parameters of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION.</span></span>                                                      |
| <span data-ttu-id="dd87d-142">**\_tipo de \_ uso de atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-142">**WPD\_PARAMETER\_ATTRIBUTE\_USAGE\_TYPE**</span></span>           | <span data-ttu-id="dd87d-143">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="dd87d-143">**VT\_UI4**</span></span>     | <span data-ttu-id="dd87d-144">Um inteiro que especifica o uso de um parâmetro de método, por exemplo, in/out. Os valores válidos são do tipo de enumeração de [**\_ tipos de \_ uso \_ de parâmetro WPD**](wpd-parameter-usage-types.md) .</span><span class="sxs-lookup"><span data-stu-id="dd87d-144">An integer that specifies the usage of a method parameter, for example, in/out. Valid values are of the [**WPD\_PARAMETER\_USAGE\_TYPES**](wpd-parameter-usage-types.md) enumeration type.</span></span> |
| <span data-ttu-id="dd87d-145">**\_VarType de \_ atributo de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dd87d-145">**WPD\_PARAMETER\_ATTRIBUTE\_VARTYPE**</span></span>               | <span data-ttu-id="dd87d-146">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="dd87d-146">**VT\_UI4**</span></span>     | <span data-ttu-id="dd87d-147">O VarType do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dd87d-147">The parameter VarType.</span></span>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="dd87d-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd87d-148">Requirements</span></span>



| <span data-ttu-id="dd87d-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd87d-149">Requirement</span></span> | <span data-ttu-id="dd87d-150">Valor</span><span class="sxs-lookup"><span data-stu-id="dd87d-150">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd87d-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd87d-151">Header</span></span><br/> | <dl> <span data-ttu-id="dd87d-152"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd87d-152"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd87d-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd87d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd87d-154">**Propriedades e atributos**</span><span class="sxs-lookup"><span data-stu-id="dd87d-154">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




