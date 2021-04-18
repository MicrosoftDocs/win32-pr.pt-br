---
description: O comando \_ WPD \_ ext de provedor de \_ código de operação de \_ Get \_ com suporte \_ \_ do Não há nenhuma fase de dados subsequente associada a este comando.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763064"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a><span data-ttu-id="14a64-104">Comando WPD de \_ \_ MTP \_ ext de \_ \_ fornecedor com suporte \_ \_</span><span class="sxs-lookup"><span data-stu-id="14a64-104">WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES Command</span></span>

<span data-ttu-id="14a64-105">O comando **WPD \_ ext de provedor de código de \_ \_ \_ \_ \_ \_ operação de Get com suporte** do</span><span class="sxs-lookup"><span data-stu-id="14a64-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES** command sends an MTP command block.</span></span> <span data-ttu-id="14a64-106">Não há nenhuma fase de dados subsequente associada a este comando.</span><span class="sxs-lookup"><span data-stu-id="14a64-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="14a64-107">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="14a64-107">Command category</span></span>

<span data-ttu-id="14a64-108">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="14a64-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="14a64-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14a64-109">Parameters</span></span>

<span data-ttu-id="14a64-110">Este comando não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="14a64-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14a64-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="14a64-111">Return Value</span></span>

<span data-ttu-id="14a64-112">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="14a64-112">The driver returns the following results.</span></span>



| <span data-ttu-id="14a64-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="14a64-113">Result</span></span>                                                | <span data-ttu-id="14a64-114">VarType</span><span class="sxs-lookup"><span data-stu-id="14a64-114">VarType</span></span> | <span data-ttu-id="14a64-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="14a64-115">Description</span></span>                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a64-116">**\_códigos de \_ operação de fornecedor de MTP \_ ext de \_ \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="14a64-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_OPERATION\_CODES**</span></span> | <span data-ttu-id="14a64-117">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="14a64-117">VT\_UI4</span></span> | <span data-ttu-id="14a64-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="14a64-118">Required.</span></span> <span data-ttu-id="14a64-119">Um **IPortableDevicePropVariantCollection** que contém todos os códigos de operação estendidos pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="14a64-119">An **IPortableDevicePropVariantCollection** that contains all vendor-extended operation codes.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="14a64-120">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="14a64-120">Calling Methods</span></span>

<span data-ttu-id="14a64-121">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="14a64-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="14a64-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a64-122">Requirements</span></span>



| <span data-ttu-id="14a64-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a64-123">Requirement</span></span> | <span data-ttu-id="14a64-124">Valor</span><span class="sxs-lookup"><span data-stu-id="14a64-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a64-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14a64-125">Header</span></span><br/> | <dl> <span data-ttu-id="14a64-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="14a64-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a64-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="14a64-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a64-128">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="14a64-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




