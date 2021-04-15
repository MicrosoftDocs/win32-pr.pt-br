---
description: Contém os tipos de entrada registrados para uma Media Foundation transformação (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: Atributo MFT_INPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502277"
---
# <a name="mft_input_types_attributes-attribute"></a><span data-ttu-id="de45a-103">\_Atributo de \_ atributos de tipos de entrada de MFT \_</span><span class="sxs-lookup"><span data-stu-id="de45a-103">MFT\_INPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="de45a-104">Contém os tipos de entrada registrados para uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="de45a-104">Contains the registered input types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="de45a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="de45a-105">Data type</span></span>

<span data-ttu-id="de45a-106">**MFT \_ Informações de tipo de registro armazenadas como byte \_ \_ \[ \]** **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="de45a-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="de45a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="de45a-107">Get/set</span></span>

<span data-ttu-id="de45a-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="de45a-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="de45a-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="de45a-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="de45a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="de45a-110">Remarks</span></span>

<span data-ttu-id="de45a-111">Esse atributo é definido nos ponteiros do [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="de45a-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="de45a-112">Esse atributo contém uma matriz de estruturas de informações de tipo de registro de MFT que descrevem um ou mais formatos de entrada com suporte no MFT. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)</span><span class="sxs-lookup"><span data-stu-id="de45a-112">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more input formats supported by the MFT.</span></span> <span data-ttu-id="de45a-113">Esses valores são extraídos do registro e são destinados como uma dica ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de45a-113">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="de45a-114">O MFT pode dar suporte a formatos adicionais.</span><span class="sxs-lookup"><span data-stu-id="de45a-114">The MFT might support additional formats.</span></span> <span data-ttu-id="de45a-115">Para definir o formato de entrada real, você deve criar o MFT e chamar [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="de45a-115">To set the actual input format, you must create the MFT and call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="de45a-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="de45a-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="de45a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de45a-117">Requirements</span></span>



| <span data-ttu-id="de45a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="de45a-118">Requirement</span></span> | <span data-ttu-id="de45a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="de45a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de45a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de45a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de45a-121">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="de45a-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="de45a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de45a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de45a-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="de45a-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="de45a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de45a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de45a-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="de45a-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de45a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="de45a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de45a-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de45a-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de45a-128">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="de45a-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




