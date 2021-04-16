---
description: Contém o nome do idioma de intercâmbio de mídia acessível (SAMI) que é definido para o fluxo.
ms.assetid: 3151c369-9d2b-4f03-9a4a-9b9267314dc1
title: Atributo MF_SD_SAMI_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd476c86ddde7d369265c5302192e4a7c01295f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761702"
---
# <a name="mf_sd_sami_language-attribute"></a><span data-ttu-id="1f78a-103">\_Atributo de \_ idioma de Sami SD MF \_</span><span class="sxs-lookup"><span data-stu-id="1f78a-103">MF\_SD\_SAMI\_LANGUAGE attribute</span></span>

<span data-ttu-id="1f78a-104">Contém o nome do idioma de intercâmbio de mídia acessível (SAMI) que é definido para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="1f78a-104">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span>

<span data-ttu-id="1f78a-105">Esse atributo está presente nos descritores de fluxo retornados da fonte de mídia SAMI.</span><span class="sxs-lookup"><span data-stu-id="1f78a-105">This attribute is present in the stream descriptors returned from the SAMI media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="1f78a-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1f78a-106">Data type</span></span>

<span data-ttu-id="1f78a-107">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="1f78a-107">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="1f78a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f78a-108">Remarks</span></span>

<span data-ttu-id="1f78a-109">O nome do idioma SAMI é especificado no arquivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="1f78a-109">The SAMI language name is specified in the SAMI file.</span></span>

<span data-ttu-id="1f78a-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1f78a-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f78a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f78a-111">Requirements</span></span>



| <span data-ttu-id="1f78a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f78a-112">Requirement</span></span> | <span data-ttu-id="1f78a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1f78a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f78a-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f78a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1f78a-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f78a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1f78a-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f78a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1f78a-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f78a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1f78a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f78a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f78a-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f78a-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f78a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f78a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f78a-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f78a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f78a-122">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="1f78a-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="1f78a-123">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="1f78a-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="1f78a-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1f78a-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="1f78a-125">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="1f78a-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f78a-126">**IMFSAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="1f78a-126">**IMFSAMIStyle**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)
</dt> </dl>

 

 




