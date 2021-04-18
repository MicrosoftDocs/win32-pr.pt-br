---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de áudio.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Propriedades de áudio (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781203"
---
# <a name="audio-properties"></a><span data-ttu-id="d6d1a-103">Propriedades de áudio</span><span class="sxs-lookup"><span data-stu-id="d6d1a-103">Audio Properties</span></span>

<span data-ttu-id="d6d1a-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de áudio.</span><span class="sxs-lookup"><span data-stu-id="d6d1a-104">Windows Portable Devices supports the following audio properties.</span></span>



| <span data-ttu-id="d6d1a-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d6d1a-105">Property</span></span>                         | <span data-ttu-id="d6d1a-106">VarType</span><span class="sxs-lookup"><span data-stu-id="d6d1a-106">VarType</span></span>     | <span data-ttu-id="d6d1a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6d1a-107">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d1a-108">**\_profundidade de \_ bit de áudio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-108">**WPD\_AUDIO\_BIT\_DEPTH**</span></span>       | <span data-ttu-id="d6d1a-109">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-109">**VT\_UI4**</span></span> | <span data-ttu-id="d6d1a-110">A profundidade de bits do áudio.</span><span class="sxs-lookup"><span data-stu-id="d6d1a-110">The bit-depth of the audio.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="d6d1a-111">**taxa de bits de \_ áudio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-111">**WPD\_AUDIO\_BITRATE**</span></span>          | <span data-ttu-id="d6d1a-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-112">**VT\_UI4**</span></span> | <span data-ttu-id="d6d1a-113">A taxa de bits do áudio, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d6d1a-113">The bit rate of the audio, in bits per second.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="d6d1a-114">**\_alinhamento de \_ bloco de áudio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-114">**WPD\_AUDIO\_BLOCK\_ALIGNMENT**</span></span> | <span data-ttu-id="d6d1a-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-115">**VT\_UI4**</span></span> | <span data-ttu-id="d6d1a-116">O alinhamento de bloco do arquivo de áudio, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d6d1a-116">The block alignment of the audio file, in bytes.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="d6d1a-117">**\_contagem de \_ canais de áudio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-117">**WPD\_AUDIO\_CHANNEL\_COUNT**</span></span>   | <span data-ttu-id="d6d1a-118">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-118">**VT\_R4**</span></span>  | <span data-ttu-id="d6d1a-119">O número de canais neste arquivo de áudio, por exemplo, 1, 2 ou 5,1.</span><span class="sxs-lookup"><span data-stu-id="d6d1a-119">The number of channels in this audio file, for example, 1, 2, or 5.1.</span></span>                                                                                                                                              |
| <span data-ttu-id="d6d1a-120">**\_código de \_ formato de áudio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-120">**WPD\_AUDIO\_FORMAT\_CODE**</span></span>     | <span data-ttu-id="d6d1a-121">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-121">**VT\_UI4**</span></span> | <span data-ttu-id="d6d1a-122">O número de código do formato WAVE registrado.</span><span class="sxs-lookup"><span data-stu-id="d6d1a-122">The registered WAVE format code number.</span></span> <span data-ttu-id="d6d1a-123">Para obter uma lista de formatos de onda registrados, confira o artigo [códigos FOURCC registrados e formatos de onda](https://msdn2.microsoft.com/library/ms867195.aspx) no site do MSDN.</span><span class="sxs-lookup"><span data-stu-id="d6d1a-123">For a listing of registered WAVE formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d6d1a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6d1a-124">Requirements</span></span>



| <span data-ttu-id="d6d1a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6d1a-125">Requirement</span></span> | <span data-ttu-id="d6d1a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d6d1a-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d1a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6d1a-127">Header</span></span><br/> | <dl> <span data-ttu-id="d6d1a-128"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6d1a-128"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d1a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6d1a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d1a-130">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="d6d1a-130">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




