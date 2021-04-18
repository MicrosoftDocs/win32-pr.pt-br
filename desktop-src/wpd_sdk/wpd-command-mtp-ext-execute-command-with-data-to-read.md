---
description: O comando do WPD de \_ \_ MTP \_ ext Command \_ \_ \_ com \_ dados \_ para \_ ler comando envia um bloco de comando MTP, que será seguido por uma fase de dados. (Os dados são enviados do dispositivo para o host.).
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807879"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a><span data-ttu-id="c814a-104">Comando \_ WPD \_ \_ de MTP ext Command \_ \_ \_ com \_ dados \_ para \_ ler comando</span><span class="sxs-lookup"><span data-stu-id="c814a-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ Command</span></span>

<span data-ttu-id="c814a-105">O comando do **WPD de \_ \_ MTP \_ ext Command \_ \_ \_ com \_ dados \_ para \_ ler** comando envia um bloco de comando MTP, que será seguido por uma fase de dados.</span><span class="sxs-lookup"><span data-stu-id="c814a-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command sends an MTP command block, which will be followed by a data phase.</span></span> <span data-ttu-id="c814a-106">(Os dados são enviados do dispositivo para o host.)</span><span class="sxs-lookup"><span data-stu-id="c814a-106">(The data is sent from the device to the host.)</span></span>

## <a name="command-category"></a><span data-ttu-id="c814a-107">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="c814a-107">Command category</span></span>

<span data-ttu-id="c814a-108">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c814a-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="c814a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c814a-109">Parameters</span></span>

<span data-ttu-id="c814a-110">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c814a-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="c814a-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c814a-111">Parameter</span></span>                                      | <span data-ttu-id="c814a-112">VarType</span><span class="sxs-lookup"><span data-stu-id="c814a-112">VarType</span></span> | <span data-ttu-id="c814a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c814a-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c814a-114">**\_código de \_ operação do MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c814a-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="c814a-115">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="c814a-115">VT\_UI4</span></span> | <span data-ttu-id="c814a-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c814a-116">Required.</span></span> <span data-ttu-id="c814a-117">Identifica um código de operação MTP estendido pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c814a-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="c814a-118">**\_parâmetros de \_ \_ operação de extensão MTP de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c814a-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="c814a-119">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="c814a-119">VT\_UI4</span></span> | <span data-ttu-id="c814a-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c814a-120">Required.</span></span> <span data-ttu-id="c814a-121">Um **IPortableDevicePropVariantCollection**, que identifica os parâmetros necessários para o código de operação do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c814a-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="c814a-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c814a-122">Return Value</span></span>

<span data-ttu-id="c814a-123">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="c814a-123">The driver returns the following results.</span></span>



| <span data-ttu-id="c814a-124">Resultado</span><span class="sxs-lookup"><span data-stu-id="c814a-124">Result</span></span>                                                       | <span data-ttu-id="c814a-125">VarType</span><span class="sxs-lookup"><span data-stu-id="c814a-125">VarType</span></span>    | <span data-ttu-id="c814a-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="c814a-126">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c814a-127">**\_ \_ \_ \_ \_ Tamanho total dos \_ dados da transferência de extensão MTP \_ da propriedade WPD**</span><span class="sxs-lookup"><span data-stu-id="c814a-127">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span>     | <span data-ttu-id="c814a-128">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="c814a-128">VT\_UI8</span></span>    | <span data-ttu-id="c814a-129">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c814a-129">Required.</span></span> <span data-ttu-id="c814a-130">Retorna o tamanho total dos dados, em bytes, excluindo qualquer sobrecarga proveniente do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c814a-130">Returns the total data size, in bytes, excluding any overhead coming from the device.</span></span> <span data-ttu-id="c814a-131">Se o dispositivo relatar um DataSize desconhecido (0xFFFFFFFF), o driver deverá chamar **ReadData** repetidamente até que um pequeno bloco seja recebido</span><span class="sxs-lookup"><span data-stu-id="c814a-131">If the device reports unknown datasize (0xFFFFFFFF), the driver should call **ReadData** repeatedly until a short chunk is received</span></span> |
| <span data-ttu-id="c814a-132">**\_tamanho do \_ \_ buffer de \_ \_ transferência ideal \_ de MTP ext \_ da propriedade WPD**</span><span class="sxs-lookup"><span data-stu-id="c814a-132">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="c814a-133">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="c814a-133">VT\_UI4</span></span>    | <span data-ttu-id="c814a-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c814a-134">Optional.</span></span> <span data-ttu-id="c814a-135">Retorna o tamanho ideal do buffer de transferência.</span><span class="sxs-lookup"><span data-stu-id="c814a-135">Returns the optimal size of the transfer buffer.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="c814a-136">**\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c814a-136">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="c814a-137">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="c814a-137">VT\_LPWSTR</span></span> | <span data-ttu-id="c814a-138">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c814a-138">Required.</span></span> <span data-ttu-id="c814a-139">Especifica o identificador de contexto para transferências de dados subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c814a-139">Specifies the context identifier for subsequent data transfers.</span></span>                                                                                                                                                           |



 

## <a name="calling-methods"></a><span data-ttu-id="c814a-140">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="c814a-140">Calling Methods</span></span>

<span data-ttu-id="c814a-141">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="c814a-141">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="c814a-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c814a-142">Requirements</span></span>



| <span data-ttu-id="c814a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c814a-143">Requirement</span></span> | <span data-ttu-id="c814a-144">Valor</span><span class="sxs-lookup"><span data-stu-id="c814a-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c814a-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c814a-145">Header</span></span><br/> | <dl> <span data-ttu-id="c814a-146"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="c814a-146"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c814a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c814a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c814a-148">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="c814a-148">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




