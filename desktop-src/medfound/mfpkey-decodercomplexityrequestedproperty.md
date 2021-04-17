---
description: Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: Propriedade MFPKEY_DECODERCOMPLEXITYREQUESTED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790470"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a><span data-ttu-id="3aa3b-103">\_Propriedade MFPKEY DECODERCOMPLEXITYREQUESTED</span><span class="sxs-lookup"><span data-stu-id="3aa3b-103">MFPKEY\_DECODERCOMPLEXITYREQUESTED Property</span></span>

<span data-ttu-id="3aa3b-104">Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-104">Specifies the device conformance template that you want to use for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="3aa3b-105">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3aa3b-105">Data Type</span></span>

<span data-ttu-id="3aa3b-106">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="3aa3b-106">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="3aa3b-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="3aa3b-107">Default Value</span></span>

<span data-ttu-id="3aa3b-108">1</span><span class="sxs-lookup"><span data-stu-id="3aa3b-108">1</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3aa3b-109">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3aa3b-109">Constant for IPropertyBag</span></span>

<span data-ttu-id="3aa3b-110">g \_ wszWMVCDecoderComplexityRequested</span><span class="sxs-lookup"><span data-stu-id="3aa3b-110">g\_wszWMVCDecoderComplexityRequested</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="3aa3b-111">Tipo de dados para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3aa3b-111">Data Type for IPropertyBag</span></span>

<span data-ttu-id="3aa3b-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="3aa3b-112">VT\_BSTR</span></span>

## <a name="default-value-for-ipropertybag"></a><span data-ttu-id="3aa3b-113">Valor padrão para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3aa3b-113">Default Value for IPropertyBag</span></span>

<span data-ttu-id="3aa3b-114">MP</span><span class="sxs-lookup"><span data-stu-id="3aa3b-114">"MP"</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa3b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aa3b-115">Remarks</span></span>

<span data-ttu-id="3aa3b-116">O codec tentará codificar o conteúdo usando o modelo de conformidade do dispositivo especificado por esse valor.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-116">The codec will attempt to encode the content using the device conformance template specified by this value.</span></span> <span data-ttu-id="3aa3b-117">O modelo real para o qual o conteúdo codificado está em conformidade pode ser recuperado da propriedade [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) após a codificação.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-117">The actual template to which the encoded content conforms can be retrieved from the [MFPKEY\_DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) property after encoding.</span></span>

<span data-ttu-id="3aa3b-118">Essa propriedade deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-118">This property must be one of the following values.</span></span>



| <span data-ttu-id="3aa3b-119">Valor para IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="3aa3b-119">Value for IPropertyStore</span></span> | <span data-ttu-id="3aa3b-120">Valor para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3aa3b-120">Value for IPropertyBag</span></span> | <span data-ttu-id="3aa3b-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aa3b-121">Description</span></span>         |
|--------------------------|------------------------|---------------------|
| <span data-ttu-id="3aa3b-122">0</span><span class="sxs-lookup"><span data-stu-id="3aa3b-122">0</span></span>                        | <span data-ttu-id="3aa3b-123">SP3</span><span class="sxs-lookup"><span data-stu-id="3aa3b-123">"SP"</span></span>                   | <span data-ttu-id="3aa3b-124">Perfil simples</span><span class="sxs-lookup"><span data-stu-id="3aa3b-124">simple profile</span></span>      |
| <span data-ttu-id="3aa3b-125">1</span><span class="sxs-lookup"><span data-stu-id="3aa3b-125">1</span></span>                        | <span data-ttu-id="3aa3b-126">MP</span><span class="sxs-lookup"><span data-stu-id="3aa3b-126">"MP"</span></span>                   | <span data-ttu-id="3aa3b-127">Perfil principal</span><span class="sxs-lookup"><span data-stu-id="3aa3b-127">main profile</span></span>        |
| <span data-ttu-id="3aa3b-128">2</span><span class="sxs-lookup"><span data-stu-id="3aa3b-128">2</span></span>                        | <span data-ttu-id="3aa3b-129">CP</span><span class="sxs-lookup"><span data-stu-id="3aa3b-129">"CP"</span></span>                   | <span data-ttu-id="3aa3b-130">Não tem mais suporte</span><span class="sxs-lookup"><span data-stu-id="3aa3b-130">no longer supported</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3aa3b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa3b-131">Requirements</span></span>



| <span data-ttu-id="3aa3b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa3b-132">Requirement</span></span> | <span data-ttu-id="3aa3b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3aa3b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa3b-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aa3b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa3b-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3aa3b-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3aa3b-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aa3b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa3b-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3aa3b-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3aa3b-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3aa3b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aa3b-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3b-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa3b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aa3b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa3b-141">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3aa3b-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




