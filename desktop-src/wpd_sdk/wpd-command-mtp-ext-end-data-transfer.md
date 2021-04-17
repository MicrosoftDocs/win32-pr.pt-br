---
description: O comando \_ de \_ transferência de dados de extensão final MTP do comando WPD \_ \_ \_ \_ conclui uma transferência de dados e uma resposta de leitura do dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812155"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a><span data-ttu-id="1bdba-103">Comando \_ de \_ transferência de dados do MTP \_ ext \_ end \_ \_</span><span class="sxs-lookup"><span data-stu-id="1bdba-103">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER Command</span></span>

<span data-ttu-id="1bdba-104">O comando de **\_ transferência de \_ \_ dados de extensão \_ \_ \_ final MTP do comando WPD** conclui uma transferência de dados e uma resposta de leitura do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1bdba-104">The **WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER** command completes a data transfer and read response from the device.</span></span> <span data-ttu-id="1bdba-105">A transferência é iniciada pelo comando [**WPD \_ de \_ \_ execução MTP \_ ext \_ \_ com \_ dados \_ para \_ ler**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) o comando ou o comando WPD de [**\_ \_ execução MTP \_ ext \_ \_ \_ com \_ dados \_ para \_ gravar**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) o comando.</span><span class="sxs-lookup"><span data-stu-id="1bdba-105">The transfer is initiated by either the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) command or the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) command.</span></span>

## <a name="command-category"></a><span data-ttu-id="1bdba-106">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="1bdba-106">Command category</span></span>

<span data-ttu-id="1bdba-107">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1bdba-107">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="1bdba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bdba-108">Parameters</span></span>

<span data-ttu-id="1bdba-109">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1bdba-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="1bdba-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bdba-110">Parameter</span></span>                                      | <span data-ttu-id="1bdba-111">VarType</span><span class="sxs-lookup"><span data-stu-id="1bdba-111">VarType</span></span>    | <span data-ttu-id="1bdba-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bdba-112">Description</span></span>                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1bdba-113">**\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1bdba-113">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span> | <span data-ttu-id="1bdba-114">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="1bdba-114">VT\_LPWSTR</span></span> | <span data-ttu-id="1bdba-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1bdba-115">Required.</span></span> <span data-ttu-id="1bdba-116">Identifica o contexto que é retornado por uma chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="1bdba-116">Identifies the context that is returned by an earlier method call.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="1bdba-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1bdba-117">Return Value</span></span>

<span data-ttu-id="1bdba-118">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="1bdba-118">The driver returns the following results.</span></span>



| <span data-ttu-id="1bdba-119">Resultado</span><span class="sxs-lookup"><span data-stu-id="1bdba-119">Result</span></span>                                        | <span data-ttu-id="1bdba-120">VarType</span><span class="sxs-lookup"><span data-stu-id="1bdba-120">VarType</span></span> | <span data-ttu-id="1bdba-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bdba-121">Description</span></span>                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdba-122">**\_código de \_ resposta de MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1bdba-122">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="1bdba-123">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="1bdba-123">VT\_UI4</span></span> | <span data-ttu-id="1bdba-124">Necessário. o código de resposta para o código de operação do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="1bdba-124">Required.The response code to the vendor operation code.</span></span>                                                                                |
| <span data-ttu-id="1bdba-125">**\_parâmetros de \_ resposta do MTP \_ ext de \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1bdba-125">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="1bdba-126">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="1bdba-126">VT\_UI4</span></span> | <span data-ttu-id="1bdba-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1bdba-127">Optional.</span></span> <span data-ttu-id="1bdba-128">Uma coleção **IPortableDevicePropVariantCollection** que identifica os parâmetros de resposta.</span><span class="sxs-lookup"><span data-stu-id="1bdba-128">An **IPortableDevicePropVariantCollection** collection that identifies any response parameters.</span></span> <span data-ttu-id="1bdba-129">Esta coleção pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="1bdba-129">This collection can be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="1bdba-130">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="1bdba-130">Calling Methods</span></span>

<span data-ttu-id="1bdba-131">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="1bdba-131">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bdba-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bdba-132">Requirements</span></span>



| <span data-ttu-id="1bdba-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bdba-133">Requirement</span></span> | <span data-ttu-id="1bdba-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1bdba-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdba-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bdba-135">Header</span></span><br/> | <dl> <span data-ttu-id="1bdba-136"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bdba-136"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bdba-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bdba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bdba-138">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="1bdba-138">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

