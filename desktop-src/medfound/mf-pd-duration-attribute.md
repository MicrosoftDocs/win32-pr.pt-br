---
description: Especifica a duração de uma apresentação, em unidades de 100 a nanossegundos.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: Atributo MF_PD_DURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812383"
---
# <a name="mf_pd_duration-attribute"></a><span data-ttu-id="47696-103">Atributo de duração de \_ PD MF \_</span><span class="sxs-lookup"><span data-stu-id="47696-103">MF\_PD\_DURATION attribute</span></span>

<span data-ttu-id="47696-104">Especifica a duração de uma apresentação, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="47696-104">Specifies the duration of a presentation, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="47696-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="47696-105">Data type</span></span>

<span data-ttu-id="47696-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="47696-106">**UINT64**</span></span>

<span data-ttu-id="47696-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="47696-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47696-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="47696-108">Remarks</span></span>

<span data-ttu-id="47696-109">As fontes de mídia podem definir esse atributo em um descritor de apresentação para indicar a duração da apresentação.</span><span class="sxs-lookup"><span data-stu-id="47696-109">Media sources can set this attribute on a presentation descriptor to indicate the duration of the presentation.</span></span>

<span data-ttu-id="47696-110">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="47696-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="47696-111">No entanto, o atributo nunca deve conter um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="47696-111">However, the attribute should never contain a negative value.</span></span>

<span data-ttu-id="47696-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="47696-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="47696-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47696-113">Examples</span></span>

<span data-ttu-id="47696-114">O exemplo a seguir mostra como obter a duração da apresentação de uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="47696-114">The following example shows how to get the presentation duration from a media source.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="47696-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47696-115">Requirements</span></span>



| <span data-ttu-id="47696-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="47696-116">Requirement</span></span> | <span data-ttu-id="47696-117">Valor</span><span class="sxs-lookup"><span data-stu-id="47696-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47696-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47696-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47696-119">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="47696-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="47696-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47696-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47696-121">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="47696-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="47696-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47696-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="47696-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="47696-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47696-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="47696-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47696-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47696-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="47696-126">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="47696-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="47696-127">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="47696-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="47696-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="47696-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="47696-129">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="47696-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="47696-130">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="47696-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




