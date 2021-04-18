---
description: O comando WPD de \_ \_ MTP \_ ext Command \_ \_ \_ sem \_ \_ comando de fase de dados envia um bloco de comando MTP. Não há nenhuma fase de dados subsequente associada a este comando.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763065"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a><span data-ttu-id="dbc49-104">Comando \_ WPD \_ MTP \_ ext \_ comando de execução \_ \_ sem \_ Data \_ Phase comando</span><span class="sxs-lookup"><span data-stu-id="dbc49-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE Command</span></span>

<span data-ttu-id="dbc49-105">O comando **WPD de \_ \_ MTP ext Command \_ \_ \_ \_ sem \_ \_** comando de fase de dados envia um bloco de comando MTP.</span><span class="sxs-lookup"><span data-stu-id="dbc49-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE** command sends an MTP command block.</span></span> <span data-ttu-id="dbc49-106">Não há nenhuma fase de dados subsequente associada a este comando.</span><span class="sxs-lookup"><span data-stu-id="dbc49-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="dbc49-107">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="dbc49-107">Command category</span></span>

<span data-ttu-id="dbc49-108">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dbc49-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="dbc49-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbc49-109">Parameters</span></span>

<span data-ttu-id="dbc49-110">O driver espera os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dbc49-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="dbc49-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbc49-111">Parameter</span></span>                                      | <span data-ttu-id="dbc49-112">VarType</span><span class="sxs-lookup"><span data-stu-id="dbc49-112">VarType</span></span> | <span data-ttu-id="dbc49-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbc49-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc49-114">**\_código de \_ operação do MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dbc49-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="dbc49-115">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="dbc49-115">VT\_UI4</span></span> | <span data-ttu-id="dbc49-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="dbc49-116">Required.</span></span> <span data-ttu-id="dbc49-117">Identifica um código de operação MTP estendido pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="dbc49-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="dbc49-118">**\_parâmetros de \_ \_ operação de extensão MTP de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dbc49-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="dbc49-119">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="dbc49-119">VT\_UI4</span></span> | <span data-ttu-id="dbc49-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="dbc49-120">Required.</span></span> <span data-ttu-id="dbc49-121">Um **IPortableDevicePropVariantCollection**, que identifica os parâmetros necessários para o código de operação do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="dbc49-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="dbc49-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="dbc49-122">Return Value</span></span>

<span data-ttu-id="dbc49-123">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="dbc49-123">The driver returns the following results.</span></span>



| <span data-ttu-id="dbc49-124">Resultado</span><span class="sxs-lookup"><span data-stu-id="dbc49-124">Result</span></span>                                        | <span data-ttu-id="dbc49-125">VarType</span><span class="sxs-lookup"><span data-stu-id="dbc49-125">VarType</span></span> | <span data-ttu-id="dbc49-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbc49-126">Description</span></span>                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc49-127">**\_código de \_ resposta de MTP \_ ext da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dbc49-127">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="dbc49-128">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="dbc49-128">VT\_UI4</span></span> | <span data-ttu-id="dbc49-129">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="dbc49-129">Required.</span></span> <span data-ttu-id="dbc49-130">O código de resposta para o código de operação do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="dbc49-130">The response code to the vendor operation code.</span></span>                                                                      |
| <span data-ttu-id="dbc49-131">**\_parâmetros de \_ resposta do MTP \_ ext de \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dbc49-131">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="dbc49-132">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="dbc49-132">VT\_UI4</span></span> | <span data-ttu-id="dbc49-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dbc49-133">Optional.</span></span> <span data-ttu-id="dbc49-134">Um **IPortableDevicePropVariantCollection** que identifica os parâmetros de resposta.</span><span class="sxs-lookup"><span data-stu-id="dbc49-134">An **IPortableDevicePropVariantCollection** that identifies any response parameters.</span></span> <span data-ttu-id="dbc49-135">Esta coleção pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="dbc49-135">This collection might be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="dbc49-136">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="dbc49-136">Calling Methods</span></span>

<span data-ttu-id="dbc49-137">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="dbc49-137">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc49-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc49-138">Requirements</span></span>



| <span data-ttu-id="dbc49-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc49-139">Requirement</span></span> | <span data-ttu-id="dbc49-140">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc49-140">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc49-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbc49-141">Header</span></span><br/> | <dl> <span data-ttu-id="dbc49-142"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc49-142"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc49-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbc49-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc49-144">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="dbc49-144">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




