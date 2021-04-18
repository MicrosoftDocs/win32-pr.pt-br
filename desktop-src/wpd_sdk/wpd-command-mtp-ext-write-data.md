---
description: O comando de \_ dados de gravação de extensão MTP do comando WPD \_ \_ \_ \_ envia dados para o dispositivo depois que o comando do WPD do comando \_ \_ MTP ext de \_ \_ execução \_ \_ com \_ dados \_ para \_ gravar é executado.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: WPD_COMMAND_MTP_EXT_WRITE_DATA comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789339"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a><span data-ttu-id="7988d-103">Comando \_ de \_ dados de gravação do MTP ext do comando \_ \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="7988d-103">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA Command</span></span>

<span data-ttu-id="7988d-104">O comando de **\_ dados de \_ \_ \_ gravação \_ de extensão MTP do comando WPD** envia dados para o dispositivo depois que o comando do WPD do comando **\_ \_ MTP ext de \_ \_ execução \_ \_ com \_ dados \_ para \_ gravar** é executado.</span><span class="sxs-lookup"><span data-stu-id="7988d-104">The **WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA** command sends data to the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="7988d-105">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="7988d-105">Command category</span></span>

<span data-ttu-id="7988d-106">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7988d-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="7988d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7988d-107">Parameters</span></span>

<span data-ttu-id="7988d-108">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7988d-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="7988d-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7988d-109">Parameter</span></span>                                                    | <span data-ttu-id="7988d-110">VarType</span><span class="sxs-lookup"><span data-stu-id="7988d-110">VarType</span></span>             | <span data-ttu-id="7988d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7988d-111">Description</span></span>                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7988d-112">**\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7988d-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="7988d-113">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="7988d-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="7988d-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7988d-114">Required.</span></span> <span data-ttu-id="7988d-115">Identifica o contexto que foi retornado pela chamada anterior ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7988d-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="7988d-116">**\_a propriedade \_ WPD \_ de transferência de extensão MTP \_ \_ \_ \_ de criação de bytes para \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="7988d-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_WRITE**</span></span> | <span data-ttu-id="7988d-117">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="7988d-117">VT\_UI4</span></span>             | <span data-ttu-id="7988d-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7988d-118">Required.</span></span> <span data-ttu-id="7988d-119">Especifica o número de bytes a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="7988d-119">Specifies the number of bytes to write.</span></span>                                      |
| <span data-ttu-id="7988d-120">**\_dados de \_ transferência do MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7988d-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                  | <span data-ttu-id="7988d-121">\_UI1 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="7988d-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="7988d-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7988d-122">Required.</span></span> <span data-ttu-id="7988d-123">Identifica o buffer no qual os dados do dispositivo são copiados.</span><span class="sxs-lookup"><span data-stu-id="7988d-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="7988d-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7988d-124">Return Value</span></span>

<span data-ttu-id="7988d-125">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="7988d-125">The driver returns the following results.</span></span>



| <span data-ttu-id="7988d-126">Resultado</span><span class="sxs-lookup"><span data-stu-id="7988d-126">Result</span></span>                                                     | <span data-ttu-id="7988d-127">VarType</span><span class="sxs-lookup"><span data-stu-id="7988d-127">VarType</span></span> | <span data-ttu-id="7988d-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="7988d-128">Description</span></span>                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| <span data-ttu-id="7988d-129">**\_bytes de \_ número de transferência de extensão MTP da propriedade WPD \_ \_ \_ \_ \_ gravados**</span><span class="sxs-lookup"><span data-stu-id="7988d-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_WRITTEN**</span></span> | <span data-ttu-id="7988d-130">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="7988d-130">VT\_UI4</span></span> | <span data-ttu-id="7988d-131">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7988d-131">Required.</span></span> <span data-ttu-id="7988d-132">Especifica o número de bytes enviados ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7988d-132">Specifies the number of bytes sent to the device..</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="7988d-133">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="7988d-133">Calling Methods</span></span>

<span data-ttu-id="7988d-134">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="7988d-134">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="7988d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7988d-135">Requirements</span></span>



| <span data-ttu-id="7988d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7988d-136">Requirement</span></span> | <span data-ttu-id="7988d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="7988d-137">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7988d-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7988d-138">Header</span></span><br/> | <dl> <span data-ttu-id="7988d-139"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="7988d-139"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7988d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7988d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7988d-141">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="7988d-141">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




