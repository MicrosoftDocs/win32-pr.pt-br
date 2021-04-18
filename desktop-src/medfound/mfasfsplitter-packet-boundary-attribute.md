---
description: Especifica se um buffer contém o início de um pacote ASF (Advanced Systems Format).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Atributo MFASFSPLITTER_PACKET_BOUNDARY (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752151"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a><span data-ttu-id="d0fe4-103">Atributo de limite de \_ pacote MFASFSPLITTER \_</span><span class="sxs-lookup"><span data-stu-id="d0fe4-103">MFASFSPLITTER\_PACKET\_BOUNDARY attribute</span></span>

<span data-ttu-id="d0fe4-104">Especifica se um buffer contém o início de um pacote ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="d0fe4-104">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="d0fe4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d0fe4-105">Data type</span></span>

<span data-ttu-id="d0fe4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d0fe4-106">**UINT32**</span></span>

<span data-ttu-id="d0fe4-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0fe4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0fe4-108">Remarks</span></span>

<span data-ttu-id="d0fe4-109">Se um buffer de mídia expor a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) por meio de **QueryInterface** e o valor desse atributo for diferente de zero, o divisor de ASF tratará o buffer como o início de um novo pacote.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-109">If a media buffer exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface through **QueryInterface**, and the value of this attribute is nonzero, the ASF splitter treats the buffer as the start of a new packet.</span></span>

<span data-ttu-id="d0fe4-110">Esse atributo se aplicará se você estiver usando o divisor de ASF para analisar dados ASF.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-110">This attribute applies if you are using the ASF splitter to parse ASF data.</span></span> <span data-ttu-id="d0fe4-111">Se os dados do ASF tiverem comprimentos de pacotes variáveis, você deverá definir esse atributo nos buffers de mídia que passar para o método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="d0fe4-111">If your ASF data has variable packet lengths, you must set this attribute on the media buffers that you pass to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="d0fe4-112">Defina o atributo como **true** se o buffer contiver o início de um novo pacote.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-112">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="d0fe4-113">Se o buffer contiver uma continuação do pacote anterior, defina o atributo como **false**.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-113">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="d0fe4-114">Os buffers não podem abranger vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-114">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="d0fe4-115">Para dados ASF com tamanhos de pacotes fixos, esse atributo não é necessário e um buffer pode abranger vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-115">For ASF data with fixed packet sizes, this attribute is not required, and a buffer can can span multiple packets.</span></span>

<span data-ttu-id="d0fe4-116">Observe que as implementações padrão do [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) fornecido pelo Media Foundation não expõem [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="d0fe4-116">Note that the standard implementations of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) provided by Media Foundation do not expose [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="d0fe4-117">Para usar esse atributo, você deve fornecer sua própria implementação de **IMFMediaBuffer**; por exemplo, encapsulando os buffers retornados por [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span><span class="sxs-lookup"><span data-stu-id="d0fe4-117">To use this attribute, you must provide your own implementation of **IMFMediaBuffer**; for example, by wrapping the buffers returned by [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0fe4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0fe4-118">Requirements</span></span>



| <span data-ttu-id="d0fe4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0fe4-119">Requirement</span></span> | <span data-ttu-id="d0fe4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d0fe4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fe4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0fe4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d0fe4-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0fe4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d0fe4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0fe4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d0fe4-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0fe4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d0fe4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0fe4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0fe4-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe4-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0fe4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0fe4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fe4-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0fe4-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0fe4-129">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="d0fe4-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0fe4-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d0fe4-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d0fe4-131">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="d0fe4-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d0fe4-132">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="d0fe4-132">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




