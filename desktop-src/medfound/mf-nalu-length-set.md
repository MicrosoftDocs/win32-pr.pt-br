---
description: Indica que as informações de comprimento de NALU serão enviadas como um BLOB com cada amostra de H. 264 compactada.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Atributo MF_NALU_LENGTH_SET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781617"
---
# <a name="mf_nalu_length_set-attribute"></a><span data-ttu-id="ca20c-103">\_Atributo de \_ conjunto de comprimento MF NALU \_</span><span class="sxs-lookup"><span data-stu-id="ca20c-103">MF\_NALU\_LENGTH\_SET attribute</span></span>

<span data-ttu-id="ca20c-104">Indica que as informações de comprimento de NALU serão enviadas como um **blob** com cada amostra de H. 264 compactada.</span><span class="sxs-lookup"><span data-stu-id="ca20c-104">Indicates that NALU length information will be sent as a **BLOB** with each compressed H.264 sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="ca20c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ca20c-105">Data type</span></span>

<span data-ttu-id="ca20c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ca20c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ca20c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca20c-107">Remarks</span></span>

<span data-ttu-id="ca20c-108">Defina esse atributo no tipo de mídia de entrada de MEDIASUBTYPE \_ H264.</span><span class="sxs-lookup"><span data-stu-id="ca20c-108">Set this attribute on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="ca20c-109">Defina \_ \_ o tamanho do NALU MF \_ definido no tipo de mídia de entrada do decodificador H. 264, indicando que cada amostra de entrada terá um comprimento de NALU disponível e cada amostra de entrada contém uma imagem primária completa.</span><span class="sxs-lookup"><span data-stu-id="ca20c-109">Set MF\_NALU\_LENGTH\_SET on input media type of H.264 decoder, indicating each input sample will have a NALU length available and each input sample contains one complete primary picture.</span></span>

<span data-ttu-id="ca20c-110">O **blob** que contém as informações de comprimento de NALU pode ser recuperado do atributo de [ \_ informações de \_ comprimento \_ MF NALU](mf-nalu-length-information.md) no exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca20c-110">The **BLOB** containing the NALU length information can be retrieved from [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) attribute on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca20c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca20c-111">Requirements</span></span>



| <span data-ttu-id="ca20c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca20c-112">Requirement</span></span> | <span data-ttu-id="ca20c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ca20c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca20c-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca20c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ca20c-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ca20c-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ca20c-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca20c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ca20c-117">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ca20c-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ca20c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca20c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca20c-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca20c-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca20c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca20c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca20c-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca20c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ca20c-122">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="ca20c-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




