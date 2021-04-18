---
description: Especifica a entrada atual na caixa de descrição de exemplo para um tipo de mídia MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Atributo MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751579"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a><span data-ttu-id="60016-103">\_Atributo de \_ \_ entrada de \_ exemplo atual do MF MT MPEG4 \_</span><span class="sxs-lookup"><span data-stu-id="60016-103">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY attribute</span></span>

<span data-ttu-id="60016-104">Especifica a entrada atual na caixa de descrição de exemplo para um tipo de mídia MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="60016-104">Specifies the current entry in the sample description box for an MPEG-4 media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="60016-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="60016-105">Data type</span></span>

<span data-ttu-id="60016-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="60016-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="60016-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="60016-107">Get/set</span></span>

<span data-ttu-id="60016-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="60016-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="60016-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="60016-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="60016-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="60016-110">Applies to</span></span>

[<span data-ttu-id="60016-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="60016-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="60016-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="60016-112">Remarks</span></span>

<span data-ttu-id="60016-113">Em um arquivo MP4 ou 3GP, a caixa Descrição de exemplo descreve a codificação usada para um fluxo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="60016-113">In an MP4 or 3GP file, the sample description box describes the encoding used for a stream in the file.</span></span> <span data-ttu-id="60016-114">A caixa Descrição de exemplo pode conter várias entradas.</span><span class="sxs-lookup"><span data-stu-id="60016-114">The sample description box can contain multiple entries.</span></span> <span data-ttu-id="60016-115">Esse atributo especifica qual entrada usar.</span><span class="sxs-lookup"><span data-stu-id="60016-115">This attribute specifies which entry to use.</span></span> <span data-ttu-id="60016-116">O valor é um índice de base zero na lista.</span><span class="sxs-lookup"><span data-stu-id="60016-116">The value is a zero-based index into the list.</span></span>

<span data-ttu-id="60016-117">Atualmente, o único valor com suporte é 0.</span><span class="sxs-lookup"><span data-stu-id="60016-117">Currently, the only supported value is 0.</span></span> <span data-ttu-id="60016-118">O atributo foi definido para extensibilidade futura.</span><span class="sxs-lookup"><span data-stu-id="60016-118">The attribute has been defined for future extensibility.</span></span>

<span data-ttu-id="60016-119">A origem do arquivo MPEG-4 sempre define o valor como 0.</span><span class="sxs-lookup"><span data-stu-id="60016-119">The MPEG-4 file source always sets the value to 0.</span></span> <span data-ttu-id="60016-120">Os coletores de arquivos MP4 e 3GP ignoram o valor desse atributo se ele estiver presente.</span><span class="sxs-lookup"><span data-stu-id="60016-120">The MP4 and 3GP file sinks ignore the value of this attribute if it is present.</span></span>

<span data-ttu-id="60016-121">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="60016-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="60016-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60016-122">Requirements</span></span>



| <span data-ttu-id="60016-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60016-123">Requirement</span></span> | <span data-ttu-id="60016-124">Valor</span><span class="sxs-lookup"><span data-stu-id="60016-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60016-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60016-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60016-126">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="60016-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="60016-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60016-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60016-128">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="60016-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="60016-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60016-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="60016-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="60016-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60016-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="60016-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60016-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60016-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="60016-133">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="60016-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="60016-134">\_Descrição de \_ exemplo de MPEG4 \_ \_ do MF MT</span><span class="sxs-lookup"><span data-stu-id="60016-134">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




