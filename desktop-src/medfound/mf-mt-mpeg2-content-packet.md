---
description: Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica se os pacotes de transporte contêm cabeçalhos de pacote de conteúdo.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Atributo MF_MT_MPEG2_CONTENT_PACKET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829116"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a><span data-ttu-id="0e4fd-103">Atributo de pacote de conteúdo do MF \_ MT \_ MPEG2 \_ \_</span><span class="sxs-lookup"><span data-stu-id="0e4fd-103">MF\_MT\_MPEG2\_CONTENT\_PACKET attribute</span></span>

<span data-ttu-id="0e4fd-104">Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica se os pacotes de transporte contêm cabeçalhos de pacote de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0e4fd-104">For a media type that describes an MPEG-2 transport stream (TS), specifies whether the transport packets contain Content Packet headers.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e4fd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0e4fd-105">Data type</span></span>

<span data-ttu-id="0e4fd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0e4fd-106">**UINT32**</span></span>



| <span data-ttu-id="0e4fd-107">Valor</span><span class="sxs-lookup"><span data-stu-id="0e4fd-107">Value</span></span>                                                                                                | <span data-ttu-id="0e4fd-108">Significado</span><span class="sxs-lookup"><span data-stu-id="0e4fd-108">Meaning</span></span>                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0e4fd-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0e4fd-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0e4fd-110">Nenhum cabeçalho de pacote de conteúdo é adicionado.</span><span class="sxs-lookup"><span data-stu-id="0e4fd-110">No Content Packet headers are added.</span></span><br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <span data-ttu-id="0e4fd-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0e4fd-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0e4fd-112">A 200 a 1.000 intervalos de milissegundos, um cabeçalho de pacote de conteúdo de 14 bytes é adicionado ao início do pacote de transporte, conforme definido pela Associação de ARIB (setores de rádio e empresas) padrão.</span><span class="sxs-lookup"><span data-stu-id="0e4fd-112">At 200–1000 millisecond intervals, a 14-byte Content Packet header is added to the beginning of the transport packet, as defined by the Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0e4fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e4fd-113">Requirements</span></span>



| <span data-ttu-id="0e4fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e4fd-114">Requirement</span></span> | <span data-ttu-id="0e4fd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0e4fd-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e4fd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e4fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e4fd-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e4fd-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0e4fd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e4fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e4fd-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e4fd-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0e4fd-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e4fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e4fd-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e4fd-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e4fd-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e4fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e4fd-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e4fd-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




