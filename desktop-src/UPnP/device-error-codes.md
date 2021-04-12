---
title: Códigos de erro do dispositivo
description: Os métodos InvokeAction e QueryStateVariable retornam valores HRESULT que podem indicar um erro de dispositivo (ou seja, um erro que é recebido de um dispositivo certificado pelo UPnP).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104454421"
---
# <a name="device-error-codes"></a><span data-ttu-id="b952a-103">Códigos de erro do dispositivo</span><span class="sxs-lookup"><span data-stu-id="b952a-103">Device Error Codes</span></span>

<span data-ttu-id="b952a-104">Os métodos [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) retornam valores **HRESULT** que podem indicar um erro de dispositivo (ou seja, um erro que é recebido de um dispositivo certificado pelo UPnP).</span><span class="sxs-lookup"><span data-stu-id="b952a-104">The [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods return **HRESULT** values that might indicate a device error (that is, an error that is received from a UPnP-certified device).</span></span> <span data-ttu-id="b952a-105">Se um erro for recebido de um dispositivo, o método ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) ou [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) retornará um valor **HRESULT** com base no código de erro do dispositivo, conforme explicado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b952a-105">If an error is received from a device, the method ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) or [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) returns an **HRESULT** value that is based on the device error code, as explained in this topic.</span></span> <span data-ttu-id="b952a-106">Como uma conversão é aplicada ao código de erro do dispositivo para produzir um valor **HRESULT** , você não pode ler o código de erro do dispositivo diretamente do valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b952a-106">Because a conversion is applied to the device error code to produce an **HRESULT** value, you cannot read the device error code directly from the **HRESULT** value.</span></span>

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a><span data-ttu-id="b952a-107">Conversão de um código de erro de dispositivo para um HRESULT</span><span class="sxs-lookup"><span data-stu-id="b952a-107">Conversion of a Device Error Code to an HRESULT</span></span>

<span data-ttu-id="b952a-108">Há códigos de erro padrão e não padrão do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b952a-108">There are both standard and non-standard device error codes.</span></span> <span data-ttu-id="b952a-109">Os códigos padrão têm o mesmo significado em todos os dispositivos certificados pelo UPnP e têm valores inferiores a 600.</span><span class="sxs-lookup"><span data-stu-id="b952a-109">The standard codes have the same meaning across all UPnP-certified devices and have values that are less than 600.</span></span> <span data-ttu-id="b952a-110">Os códigos não padrão são específicos do fornecedor e têm valores variados de 600 a 899.</span><span class="sxs-lookup"><span data-stu-id="b952a-110">The non-standard codes are vendor-specific and have values ranging from 600 through 899.</span></span>

<span data-ttu-id="b952a-111">Se o código de erro do dispositivo é ou não padrão determina como o valor **HRESULT** é gerado:</span><span class="sxs-lookup"><span data-stu-id="b952a-111">Whether or not the device error code is standard determines how the **HRESULT** value is generated:</span></span>

-   <span data-ttu-id="b952a-112">Um código de erro de dispositivo padrão é mapeado para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b952a-112">A standard device error code is mapped to an **HRESULT** value.</span></span>

<!-- -->

-   <span data-ttu-id="b952a-113">Um código de erro de dispositivo não padrão é inserido no valor **HRESULT** aplicando uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="b952a-113">A non-standard device error code is embedded in the **HRESULT** value by applying a formula.</span></span>

<span data-ttu-id="b952a-114">Esses dois procedimentos podem ser revertidos para determinar o código de erro do dispositivo a partir de um valor **HRESULT** específico.</span><span class="sxs-lookup"><span data-stu-id="b952a-114">Both of these procedures can be reversed to determine the device error code from a particular **HRESULT** value.</span></span>

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a><span data-ttu-id="b952a-115">Derivando um código de erro de dispositivo de um valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="b952a-115">Deriving a Device Error Code from an HRESULT Value</span></span>

<span data-ttu-id="b952a-116">Se o valor **HRESULT** for maior ou igual a um **UPnP e a \_ \_ \_ \_ base específica da ação** (0x80040300) e menor ou igual a **UPnP e a \_ \_ ação \_ específica \_ Max** (0x8004042B), o código de erro do dispositivo não será padrão — Use a fórmula na seção a seguir para determinar o código de erro.</span><span class="sxs-lookup"><span data-stu-id="b952a-116">If the **HRESULT** value is greater than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_BASE** (0x80040300) and less than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_MAX** (0x8004042B), the device error code is nonstandard — use the formula in the following section to determine the error code.</span></span> <span data-ttu-id="b952a-117">Caso contrário, o código de erro do dispositivo é padrão: Use a tabela na seção mapeamento para códigos de erro de dispositivo padrão, que fornece o mapeamento do valor **HRESULT** para o código de erro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b952a-117">Otherwise, the device error code is standard — use the table in the Mapping for Standard Device Error Codes section, which provides the mapping from the **HRESULT** value to the device error code.</span></span>

<span data-ttu-id="b952a-118">Para obter uma descrição de texto do erro após uma chamada para [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), defina o parâmetro *pvarRetVal* como uma matriz vazia.</span><span class="sxs-lookup"><span data-stu-id="b952a-118">For a text description of the error after a call to [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), set the *pvarRetVal* parameter to an empty array.</span></span> <span data-ttu-id="b952a-119">No retorno, esse parâmetro conterá uma descrição de texto do erro, caso tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="b952a-119">Upon return, this parameter will contain a text description of the error, if any occurred.</span></span>

### <a name="formula-for-nonstandard-device-error-codes"></a><span data-ttu-id="b952a-120">Fórmula para códigos de erro não padrão do dispositivo</span><span class="sxs-lookup"><span data-stu-id="b952a-120">Formula for Nonstandard Device Error Codes</span></span>

<span data-ttu-id="b952a-121">Use a fórmula a seguir se a **ação de UPnP \_ e a \_ \_ \_ base especificarem** a partir de uma ação de UPnP e a **\_ \_ Action \_ \_** específicas </span><span class="sxs-lookup"><span data-stu-id="b952a-121">Use the following formula if **UPNP\_E\_ACTION\_SPECIFIC\_BASE** ≤ **HRESULT** ≤**UPNP\_E\_ACTION\_SPECIFIC\_MAX**.</span></span>

<span data-ttu-id="b952a-122">Código de erro do dispositivo = (**HRESULT**  -  **UPnP \_ E a \_ \_ \_ base específica da ação**) + **\_ \_ \_ base específica da ação de falha**</span><span class="sxs-lookup"><span data-stu-id="b952a-122">Device Error Code = (**HRESULT** - **UPNP\_E\_ACTION\_SPECIFIC\_BASE**) + **FAULT\_ACTION\_SPECIFIC\_BASE**</span></span>

<span data-ttu-id="b952a-123">Substituindo os valores numéricos reais, a equação é: código de erro do dispositivo = (**HRESULT** -0x80040300) + 0x0258</span><span class="sxs-lookup"><span data-stu-id="b952a-123">Substituting the actual numeric values, the equation is: Device Error Code = (**HRESULT** - 0x80040300) + 0x0258</span></span>

### <a name="mapping-for-standard-device-error-codes"></a><span data-ttu-id="b952a-124">Mapeamento para códigos de erro de dispositivo padrão</span><span class="sxs-lookup"><span data-stu-id="b952a-124">Mapping for Standard Device Error Codes</span></span>

<span data-ttu-id="b952a-125">Use o mapeamento a seguir se a  <  **\_ \_ \_ \_ base específica de ação E UPnP** do HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b952a-125">Use the following mapping if **HRESULT** < **UPNP\_E\_ACTION\_SPECIFIC\_BASE**.</span></span>



| <span data-ttu-id="b952a-126">Valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="b952a-126">HRESULT value</span></span>                    | <span data-ttu-id="b952a-127">Código de erro do dispositivo</span><span class="sxs-lookup"><span data-stu-id="b952a-127">Device Error Code</span></span>                | <span data-ttu-id="b952a-128">Valor real</span><span class="sxs-lookup"><span data-stu-id="b952a-128">Actual value</span></span> |
|----------------------------------|----------------------------------|--------------|
| <span data-ttu-id="b952a-129">\_ \_ ação inválida E UPnP \_</span><span class="sxs-lookup"><span data-stu-id="b952a-129">UPNP\_E\_INVALID\_ACTION</span></span>         | <span data-ttu-id="b952a-130">\_ação inválida de falha \_</span><span class="sxs-lookup"><span data-stu-id="b952a-130">FAULT\_INVALID\_ACTION</span></span>           | <span data-ttu-id="b952a-131">401</span><span class="sxs-lookup"><span data-stu-id="b952a-131">401</span></span>          |
| <span data-ttu-id="b952a-132">\_argumentos UPnP E \_ inválidos \_</span><span class="sxs-lookup"><span data-stu-id="b952a-132">UPNP\_E\_INVALID\_ARGUMENTS</span></span>      | <span data-ttu-id="b952a-133">ARG. de falha \_ inválido \_</span><span class="sxs-lookup"><span data-stu-id="b952a-133">FAULT\_INVALID\_ARG</span></span>              | <span data-ttu-id="b952a-134">402</span><span class="sxs-lookup"><span data-stu-id="b952a-134">402</span></span>          |
| <span data-ttu-id="b952a-135">UPNP \_ E \_ fora \_ de \_ sincronização</span><span class="sxs-lookup"><span data-stu-id="b952a-135">UPNP\_E\_OUT\_OF\_SYNC</span></span>           | <span data-ttu-id="b952a-136">\_número de \_ sequência \_ inválido de falha</span><span class="sxs-lookup"><span data-stu-id="b952a-136">FAULT\_INVALID\_SEQUENCE\_NUMBER</span></span> | <span data-ttu-id="b952a-137">403</span><span class="sxs-lookup"><span data-stu-id="b952a-137">403</span></span>          |
| <span data-ttu-id="b952a-138">\_variável UPnP E \_ inválida \_</span><span class="sxs-lookup"><span data-stu-id="b952a-138">UPNP\_E\_INVALID\_VARIABLE</span></span>       | <span data-ttu-id="b952a-139">\_variável inválida de falha \_</span><span class="sxs-lookup"><span data-stu-id="b952a-139">FAULT\_INVALID\_VARIABLE</span></span>         | <span data-ttu-id="b952a-140">404</span><span class="sxs-lookup"><span data-stu-id="b952a-140">404</span></span>          |
| <span data-ttu-id="b952a-141">\_ \_ \_ falha na solicitação de ação E UPnP \_</span><span class="sxs-lookup"><span data-stu-id="b952a-141">UPNP\_E\_ACTION\_REQUEST\_FAILED</span></span> | <span data-ttu-id="b952a-142">\_ \_ erro interno do dispositivo de falha \_</span><span class="sxs-lookup"><span data-stu-id="b952a-142">FAULT\_DEVICE\_INTERNAL\_ERROR</span></span>   | <span data-ttu-id="b952a-143">501</span><span class="sxs-lookup"><span data-stu-id="b952a-143">501</span></span>          |



 

## <a name="more-information"></a><span data-ttu-id="b952a-144">Mais informações</span><span class="sxs-lookup"><span data-stu-id="b952a-144">More Information</span></span>

<span data-ttu-id="b952a-145">Os códigos de erro do dispositivo são especificados na [arquitetura de dispositivo UPnP versão 1,0](https://openconnectivity.org/resources/documents.asp).</span><span class="sxs-lookup"><span data-stu-id="b952a-145">Device error codes are specified in [UPnP Device Architecture version 1.0](https://openconnectivity.org/resources/documents.asp).</span></span> <span data-ttu-id="b952a-146">As constantes mencionadas neste tópico são definidas nos arquivos UPnP. h e UPnP. idl.</span><span class="sxs-lookup"><span data-stu-id="b952a-146">The constants mentioned in this topic are defined in the files Upnp.h and Upnp.idl.</span></span>

 

 




