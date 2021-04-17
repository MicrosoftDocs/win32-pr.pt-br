---
description: O comando WPD de protocolo de \_ \_ \_ execução MTP ext \_ \_ \_ com \_ dados \_ para \_ gravar comando envia um bloco de comando MTP, seguido por uma fase de dados. Os dados são enviados do host para o dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791522"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a><span data-ttu-id="2392c-104">Comando \_ WPD \_ MTP \_ ext \_ comando \_ \_ com \_ dados \_ para \_ gravar comando</span><span class="sxs-lookup"><span data-stu-id="2392c-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE Command</span></span>

<span data-ttu-id="2392c-105">O comando WPD de protocolo de **\_ \_ \_ execução MTP ext \_ \_ \_ com \_ dados \_ para \_ gravar** comando envia um bloco de comando MTP, seguido por uma fase de dados.</span><span class="sxs-lookup"><span data-stu-id="2392c-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command sends an MTP command block, which is followed by a data phase.</span></span> <span data-ttu-id="2392c-106">Os dados são enviados do host para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2392c-106">The data is sent from the host to the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="2392c-107">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="2392c-107">Command category</span></span>

<span data-ttu-id="2392c-108">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2392c-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="2392c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2392c-109">Parameters</span></span>

<span data-ttu-id="2392c-110">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2392c-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="2392c-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2392c-111">Parameter</span></span>                                                | <span data-ttu-id="2392c-112">VarType</span><span class="sxs-lookup"><span data-stu-id="2392c-112">VarType</span></span> | <span data-ttu-id="2392c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2392c-113">Description</span></span>                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2392c-114">**\_código de \_ operação do MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2392c-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>             | <span data-ttu-id="2392c-115">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="2392c-115">VT\_UI4</span></span> | <span data-ttu-id="2392c-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="2392c-116">Required.</span></span> <span data-ttu-id="2392c-117">Identifica um código de operação MTP estendido pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="2392c-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                              |
| <span data-ttu-id="2392c-118">**\_parâmetros de \_ \_ operação de extensão MTP de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2392c-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span>           | <span data-ttu-id="2392c-119">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="2392c-119">VT\_UI4</span></span> | <span data-ttu-id="2392c-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="2392c-120">Required.</span></span> <span data-ttu-id="2392c-121">Uma coleção **IPortableDevicePropVariantCollection** que identifica os parâmetros necessários para o código de operação do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="2392c-121">An **IPortableDevicePropVariantCollection** collection that identifies the required parameters for the vendor operation code.</span></span> |
| <span data-ttu-id="2392c-122">**\_ \_ \_ \_ \_ Tamanho total dos \_ dados da transferência de extensão MTP \_ da propriedade WPD**</span><span class="sxs-lookup"><span data-stu-id="2392c-122">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span> | <span data-ttu-id="2392c-123">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="2392c-123">VT\_UI8</span></span> | <span data-ttu-id="2392c-124">Obrigatório. especifica o tamanho total dos dados, em bytes, excluindo qualquer sobrecarga, a ser enviada ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2392c-124">Required.Specifies the total data size, in bytes, excluding any overhead, to be sent to device.</span></span>                                         |



 

## <a name="return-value"></a><span data-ttu-id="2392c-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2392c-125">Return Value</span></span>

<span data-ttu-id="2392c-126">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="2392c-126">The driver returns the following results.</span></span>



| <span data-ttu-id="2392c-127">Resultado</span><span class="sxs-lookup"><span data-stu-id="2392c-127">Result</span></span>                                                       | <span data-ttu-id="2392c-128">VarType</span><span class="sxs-lookup"><span data-stu-id="2392c-128">VarType</span></span>    | <span data-ttu-id="2392c-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="2392c-129">Description</span></span>                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2392c-130">**\_tamanho do \_ \_ buffer de \_ \_ transferência ideal \_ de MTP ext \_ da propriedade WPD**</span><span class="sxs-lookup"><span data-stu-id="2392c-130">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="2392c-131">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="2392c-131">VT\_UI4</span></span>    | <span data-ttu-id="2392c-132">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="2392c-132">Required.</span></span> <span data-ttu-id="2392c-133">Especifica o tamanho ideal do buffer de transferência.</span><span class="sxs-lookup"><span data-stu-id="2392c-133">Specifies the optimal size of the transfer buffer.</span></span>                       |
| <span data-ttu-id="2392c-134">**\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2392c-134">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="2392c-135">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="2392c-135">VT\_LPWSTR</span></span> | <span data-ttu-id="2392c-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2392c-136">Optional.</span></span> <span data-ttu-id="2392c-137">Um identificador de contexto que o driver usa para transferências de dados subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2392c-137">A context identifier that the driver uses for subsequent data transfers.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="2392c-138">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="2392c-138">Calling Methods</span></span>

<span data-ttu-id="2392c-139">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="2392c-139">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="2392c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2392c-140">Requirements</span></span>



| <span data-ttu-id="2392c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2392c-141">Requirement</span></span> | <span data-ttu-id="2392c-142">Valor</span><span class="sxs-lookup"><span data-stu-id="2392c-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2392c-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2392c-143">Header</span></span><br/> | <dl> <span data-ttu-id="2392c-144"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="2392c-144"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2392c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2392c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2392c-146">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="2392c-146">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




