---
description: Especifica o tempo necessário para reproduzir um arquivo ASF (Advanced Systems Format), em unidades de 100 nanossegundos.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: Atributo MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922174"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a><span data-ttu-id="d1ad8-103">\_Atributo de \_ \_ duração de reprodução de arquivo MF PD ASF \_ \_</span><span class="sxs-lookup"><span data-stu-id="d1ad8-103">MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION attribute</span></span>

<span data-ttu-id="d1ad8-104">Especifica o tempo necessário para reproduzir um arquivo ASF (Advanced Systems Format), em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="d1ad8-104">Specifies the time needed to play an Advanced Systems Format (ASF) file, in 100-nanosecond units.</span></span>

<span data-ttu-id="d1ad8-105">Esse valor inclui o tempo de preversão.</span><span class="sxs-lookup"><span data-stu-id="d1ad8-105">This value includes the preroll time.</span></span> <span data-ttu-id="d1ad8-106">Para recuperar a duração real da reprodução, obtenha o valor do atributo de [**\_ \_ duração de PD do MF**](mf-pd-duration-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ad8-106">To retrieve the actual playback duration, get the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute.</span></span> <span data-ttu-id="d1ad8-107">No entanto, se o valor de preroll for maior que a duração da reprodução, o valor da **\_ \_ duração de PD de MF** será zero.</span><span class="sxs-lookup"><span data-stu-id="d1ad8-107">However, if the preroll value is greater than the play duration, the value of **MF\_PD\_DURATION** is zero.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1ad8-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d1ad8-108">Data type</span></span>

<span data-ttu-id="d1ad8-109">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d1ad8-109">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="d1ad8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1ad8-110">Remarks</span></span>

<span data-ttu-id="d1ad8-111">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="d1ad8-111">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="d1ad8-112">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="d1ad8-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="d1ad8-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1ad8-113">Examples</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a><span data-ttu-id="d1ad8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1ad8-114">Requirements</span></span>



| <span data-ttu-id="d1ad8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1ad8-115">Requirement</span></span> | <span data-ttu-id="d1ad8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d1ad8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ad8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ad8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ad8-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1ad8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d1ad8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ad8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ad8-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1ad8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d1ad8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1ad8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ad8-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ad8-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1ad8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1ad8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ad8-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1ad8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1ad8-125">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="d1ad8-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="d1ad8-126">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="d1ad8-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="d1ad8-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d1ad8-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="d1ad8-128">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="d1ad8-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1ad8-129">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="d1ad8-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="d1ad8-130">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="d1ad8-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




