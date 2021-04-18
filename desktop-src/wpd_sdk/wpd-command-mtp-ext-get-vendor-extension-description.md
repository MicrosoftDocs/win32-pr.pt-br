---
description: O comando WPD de \_ \_ MTP \_ ext \_ Get de extensão de fornecedor da a linha \_ \_ \_ de comando recupera a cadeia de caracteres de descrição de extensão de fornecedor. Essa cadeia de caracteres é definida por um conjunto de DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793305"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a><span data-ttu-id="51f45-104">Comando \_ WPD \_ MTP \_ ext \_ \_ extensão Get Vendor \_ \_ Description</span><span class="sxs-lookup"><span data-stu-id="51f45-104">WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION Command</span></span>

<span data-ttu-id="51f45-105">O comando **WPD de \_ \_ MTP \_ ext Get de \_ \_ extensão de fornecedor \_ \_** da a linha de comando recupera a cadeia de caracteres de descrição de extensão de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="51f45-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION** command retrieves the vendor-extension description string.</span></span> <span data-ttu-id="51f45-106">Essa cadeia de caracteres é definida por um conjunto de **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="51f45-106">This string is defined by a **DeviceInfo** dataset.</span></span>

## <a name="command-category"></a><span data-ttu-id="51f45-107">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="51f45-107">Command category</span></span>

<span data-ttu-id="51f45-108">**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="51f45-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="51f45-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51f45-109">Parameters</span></span>

<span data-ttu-id="51f45-110">Este comando não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="51f45-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51f45-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="51f45-111">Return Value</span></span>

<span data-ttu-id="51f45-112">O driver retorna os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="51f45-112">The driver returns the following results.</span></span>



| <span data-ttu-id="51f45-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="51f45-113">Result</span></span>                                                      | <span data-ttu-id="51f45-114">VarType</span><span class="sxs-lookup"><span data-stu-id="51f45-114">VarType</span></span>    | <span data-ttu-id="51f45-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="51f45-115">Description</span></span>                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| <span data-ttu-id="51f45-116">**\_Descrição da \_ \_ extensão de \_ fornecedor MTP ext \_ \_ de propriedade WPD**</span><span class="sxs-lookup"><span data-stu-id="51f45-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_EXTENSION\_DESCRIPTION**</span></span> | <span data-ttu-id="51f45-117">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="51f45-117">VT\_LPWSTR</span></span> | <span data-ttu-id="51f45-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="51f45-118">Required.</span></span> <span data-ttu-id="51f45-119">Especifica a cadeia de caracteres de descrição de extensão de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="51f45-119">Specifies the vendor-extension description string.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="51f45-120">Chamando métodos</span><span class="sxs-lookup"><span data-stu-id="51f45-120">Calling Methods</span></span>

<span data-ttu-id="51f45-121">Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="51f45-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="51f45-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51f45-122">Requirements</span></span>



| <span data-ttu-id="51f45-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f45-123">Requirement</span></span> | <span data-ttu-id="51f45-124">Valor</span><span class="sxs-lookup"><span data-stu-id="51f45-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f45-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51f45-125">Header</span></span><br/> | <dl> <span data-ttu-id="51f45-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f45-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51f45-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="51f45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f45-128">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="51f45-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




