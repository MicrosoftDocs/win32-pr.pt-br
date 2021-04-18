---
description: Contém os tipos de saída registrados para uma Media Foundation transformação (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Atributo MFT_OUTPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786164"
---
# <a name="mft_output_types_attributes-attribute"></a><span data-ttu-id="e01ed-103">\_Atributo de \_ atributos de tipos de saída de MFT \_</span><span class="sxs-lookup"><span data-stu-id="e01ed-103">MFT\_OUTPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="e01ed-104">Contém os tipos de saída registrados para uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="e01ed-104">Contains the registered output types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="e01ed-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e01ed-105">Data type</span></span>

<span data-ttu-id="e01ed-106">**MFT \_ Informações de tipo de registro armazenadas como byte \_ \_ \[ \]** **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="e01ed-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="remarks"></a><span data-ttu-id="e01ed-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e01ed-107">Remarks</span></span>

<span data-ttu-id="e01ed-108">Esse atributo é definido nos ponteiros do [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="e01ed-108">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="e01ed-109">Esse atributo contém uma matriz de estruturas de informações de tipo de registro de MFT que descrevem um ou mais formatos de saída com suporte pelo MFT. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)</span><span class="sxs-lookup"><span data-stu-id="e01ed-109">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more output formats supported by the MFT.</span></span> <span data-ttu-id="e01ed-110">Esses valores são extraídos do registro e são destinados como uma dica ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e01ed-110">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="e01ed-111">O MFT pode dar suporte a formatos adicionais.</span><span class="sxs-lookup"><span data-stu-id="e01ed-111">The MFT might support additional formats.</span></span> <span data-ttu-id="e01ed-112">Para definir o formato de saída real, você deve criar o MFT e chamar [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="e01ed-112">To set the actual output format, you must create the MFT and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="e01ed-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e01ed-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e01ed-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e01ed-114">Requirements</span></span>



| <span data-ttu-id="e01ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e01ed-115">Requirement</span></span> | <span data-ttu-id="e01ed-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e01ed-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e01ed-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e01ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e01ed-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e01ed-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e01ed-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e01ed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e01ed-120">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e01ed-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e01ed-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e01ed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e01ed-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e01ed-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e01ed-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e01ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e01ed-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e01ed-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e01ed-125">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="e01ed-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




