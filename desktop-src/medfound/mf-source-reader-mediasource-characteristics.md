---
description: Obtém as características da origem da mídia do leitor de origem.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Atributo MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297991"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a><span data-ttu-id="044a2-103">\_Atributo de \_ \_ \_ características Media Source do leitor de origem MF</span><span class="sxs-lookup"><span data-stu-id="044a2-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="044a2-104">Obtém as características da origem da mídia do [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="044a2-104">Gets the characteristics of the media source from the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="044a2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="044a2-105">Data type</span></span>

<span data-ttu-id="044a2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="044a2-106">**UINT32**</span></span>

<span data-ttu-id="044a2-107">O valor é um or **bit a** bit de sinalizadores da enumeração de [**\_ características do MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="044a2-107">The value is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="044a2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="044a2-108">Remarks</span></span>

<span data-ttu-id="044a2-109">Para obter esse atributo, chame o método [**IMFSourceReader:: Getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) no leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="044a2-109">To get this attribute, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method on the source reader.</span></span> <span data-ttu-id="044a2-110">Defina o parâmetro *dwStreamIndex* como **\_ \_ \_ mediaprovider do leitor de origem MF** e o parâmetro *GuidAttribute* como \_ características do leitor de origem MF \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="044a2-110">Set the *dwStreamIndex* parameter to **MF\_SOURCE\_READER\_MEDIASOURCE** and the *guidAttribute* parameter to MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS.</span></span>

<span data-ttu-id="044a2-111">O tipo **PROPVARIANT** para esse atributo é **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="044a2-111">The **PROPVARIANT** type for this attribute is **VT\_UI4**.</span></span>

## <a name="examples"></a><span data-ttu-id="044a2-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="044a2-112">Examples</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="044a2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="044a2-113">Requirements</span></span>



| <span data-ttu-id="044a2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="044a2-114">Requirement</span></span> | <span data-ttu-id="044a2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="044a2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="044a2-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044a2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="044a2-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="044a2-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="044a2-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044a2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="044a2-119">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="044a2-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="044a2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="044a2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="044a2-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="044a2-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044a2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="044a2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044a2-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="044a2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="044a2-124">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="044a2-124">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




