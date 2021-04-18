---
description: Indica que Moov será gravado antes da caixa mdat no arquivo gerado.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Atributo MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773041"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a><span data-ttu-id="26a10-103">MF \_ MPEG4SINK \_ Moov \_ antes do \_ atributo MDAT</span><span class="sxs-lookup"><span data-stu-id="26a10-103">MF\_MPEG4SINK\_MOOV\_BEFORE\_MDAT attribute</span></span>

<span data-ttu-id="26a10-104">Indica que ' Moov ' será gravado antes da caixa ' mdat ' no arquivo gerado.</span><span class="sxs-lookup"><span data-stu-id="26a10-104">Indicates that 'moov' will be written before 'mdat' box in the generated file.</span></span>

## <a name="data-type"></a><span data-ttu-id="26a10-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="26a10-105">Data type</span></span>

<span data-ttu-id="26a10-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="26a10-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="26a10-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="26a10-107">Remarks</span></span>

<span data-ttu-id="26a10-108">O comportamento padrão do coletor de mídia do MPEG4 é gravar ' Moov ' após a caixa ' mdat '.</span><span class="sxs-lookup"><span data-stu-id="26a10-108">The default behavior of the mpeg4 media sink is to write 'moov' after 'mdat' box.</span></span> <span data-ttu-id="26a10-109">A configuração desse atributo faz com que o arquivo gerado grave ' Moov ' antes da caixa ' mdat '.</span><span class="sxs-lookup"><span data-stu-id="26a10-109">Setting this attribute causes the generated file to write 'moov' before 'mdat' box.</span></span>

<span data-ttu-id="26a10-110">Para que o coletor MPEG4 Use esse atributo, o fluxo de bytes transmitido não deve ser de busca lenta ou remoto para.</span><span class="sxs-lookup"><span data-stu-id="26a10-110">In order for the mpeg4 sink to use this attribute, the byte stream passed in must not be slow seek or remote for .</span></span>

<span data-ttu-id="26a10-111">Esse recurso envolve uma cópia de arquivo adicional/remuxing.</span><span class="sxs-lookup"><span data-stu-id="26a10-111">This feature involves an additional file copying/remuxing.</span></span>

## <a name="requirements"></a><span data-ttu-id="26a10-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26a10-112">Requirements</span></span>



| <span data-ttu-id="26a10-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="26a10-113">Requirement</span></span> | <span data-ttu-id="26a10-114">Valor</span><span class="sxs-lookup"><span data-stu-id="26a10-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26a10-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26a10-115">Minimum supported client</span></span><br/> | <span data-ttu-id="26a10-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="26a10-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="26a10-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26a10-117">Minimum supported server</span></span><br/> | <span data-ttu-id="26a10-118">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="26a10-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="26a10-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26a10-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="26a10-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26a10-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26a10-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="26a10-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a10-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26a10-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26a10-123">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="26a10-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




