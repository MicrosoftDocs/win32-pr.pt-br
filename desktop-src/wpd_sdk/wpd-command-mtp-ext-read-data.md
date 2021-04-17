---
description: O comando \_ de \_ \_ dados de leitura ext do comando WPD \_ \_ recupera dados do dispositivo após o comando WPD do comando \_ \_ MTP \_ ext \_ Execute \_ \_ com \_ dados \_ para \_ ler o comando é executado.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782717"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a><span data-ttu-id="592be-103">Comando \_ de \_ dados de leitura do MTP ext de comandos \_ \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="592be-103">WPD\_COMMAND\_MTP\_EXT\_READ\_DATA Command</span></span>

<span data-ttu-id="592be-104">O comando de **\_ \_ \_ \_ \_ dados de leitura ext do comando WPD** recupera dados do dispositivo após o comando WPD do comando **\_ \_ MTP \_ ext \_ Execute \_ \_ com \_ dados \_ para \_ ler** o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="592be-104">The **WPD\_COMMAND\_MTP\_EXT\_READ\_DATA** command retrieves data from the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="592be-105">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="592be-105">Command category</span></span>

<span data-ttu-id="592be-106">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="592be-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="592be-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="592be-107">Parameters</span></span>

<span data-ttu-id="592be-108">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="592be-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="592be-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="592be-109">Parameter</span></span>                                                   | <span data-ttu-id="592be-110">VarType</span><span class="sxs-lookup"><span data-stu-id="592be-110">VarType</span></span>             | <span data-ttu-id="592be-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="592be-111">Description</span></span>                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="592be-112">**\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="592be-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>              | <span data-ttu-id="592be-113">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="592be-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="592be-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="592be-114">Required.</span></span> <span data-ttu-id="592be-115">Identifica o contexto que foi retornado pela chamada anterior ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="592be-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="592be-116">**\_a propriedade \_ WPD \_ \_ \_ \_ de bytes de transferência de extensão MTP \_ para \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="592be-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_READ**</span></span> | <span data-ttu-id="592be-117">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="592be-117">VT\_UI4</span></span>             | <span data-ttu-id="592be-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="592be-118">Required.</span></span> <span data-ttu-id="592be-119">Especifica o número de bytes a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="592be-119">Specifies the number of bytes to read.</span></span>                                       |
| <span data-ttu-id="592be-120">**\_dados de \_ transferência do MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="592be-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                 | <span data-ttu-id="592be-121">\_UI1 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="592be-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="592be-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="592be-122">Required.</span></span> <span data-ttu-id="592be-123">Identifica o buffer no qual os dados do dispositivo são copiados.</span><span class="sxs-lookup"><span data-stu-id="592be-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="592be-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="592be-124">Return Value</span></span>

<span data-ttu-id="592be-125">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="592be-125">The driver returns the following results.</span></span>



| <span data-ttu-id="592be-126">Resultado</span><span class="sxs-lookup"><span data-stu-id="592be-126">Result</span></span>                                                  | <span data-ttu-id="592be-127">VarType</span><span class="sxs-lookup"><span data-stu-id="592be-127">VarType</span></span>             | <span data-ttu-id="592be-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="592be-128">Description</span></span>                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| <span data-ttu-id="592be-129">**\_leitura de \_ bytes de transferência de extensão MTP da propriedade \_ \_ \_ WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="592be-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_READ**</span></span> | <span data-ttu-id="592be-130">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="592be-130">VT\_UI4</span></span>             | <span data-ttu-id="592be-131">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="592be-131">Required.</span></span> <span data-ttu-id="592be-132">Especifica o número de bytes recebidos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="592be-132">Specifies the number of bytes received from the device.</span></span> |
| <span data-ttu-id="592be-133">**\_dados de \_ transferência do MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="592be-133">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>             | <span data-ttu-id="592be-134">\_UI1 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="592be-134">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="592be-135">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="592be-135">Required.</span></span> <span data-ttu-id="592be-136">O buffer que contém os dados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="592be-136">The buffer that contains the device data.</span></span>               |



 

## <a name="calling-methods"></a><span data-ttu-id="592be-137">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="592be-137">Calling Methods</span></span>

<span data-ttu-id="592be-138">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="592be-138">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="592be-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="592be-139">Requirements</span></span>



| <span data-ttu-id="592be-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="592be-140">Requirement</span></span> | <span data-ttu-id="592be-141">Valor</span><span class="sxs-lookup"><span data-stu-id="592be-141">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="592be-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="592be-142">Header</span></span><br/> | <dl> <span data-ttu-id="592be-143"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="592be-143"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="592be-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="592be-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592be-145">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="592be-145">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




