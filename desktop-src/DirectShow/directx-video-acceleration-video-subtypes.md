---
description: Os seguintes subtipos são usados por decodificadores que usam a DXVA (aceleração de vídeo do DirectX).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Subtipos de vídeo de aceleração de vídeo DirectX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760752"
---
# <a name="directx-video-acceleration-video-subtypes"></a><span data-ttu-id="4138f-103">Subtipos de vídeo de aceleração de vídeo DirectX</span><span class="sxs-lookup"><span data-stu-id="4138f-103">DirectX Video Acceleration Video Subtypes</span></span>

<span data-ttu-id="4138f-104">Os seguintes subtipos são usados por decodificadores que usam a DXVA (aceleração de vídeo do DirectX).</span><span class="sxs-lookup"><span data-stu-id="4138f-104">The following subtypes are used by decoders that are using DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="4138f-105">AI44 e IA44 são superfícies com um valor de bits por pixel de 8.</span><span class="sxs-lookup"><span data-stu-id="4138f-105">AI44 and IA44 are surfaces with a bits-per-pixel value of 8.</span></span> <span data-ttu-id="4138f-106">Há 4 bits e 4 bits de *um*. *Eu* represente um índice em uma paleta YUV de 16 entradas.</span><span class="sxs-lookup"><span data-stu-id="4138f-106">There are 4 bits of I and 4 bits of *A*. *I* represents an index into a 16-entry YUV palette.</span></span> <span data-ttu-id="4138f-107">*Um* representa 4 bits de informações de transparência (também conhecidas por pixel-Alpha).</span><span class="sxs-lookup"><span data-stu-id="4138f-107">*A* represents 4 bits of transparency information (also known as per-pixel-alpha).</span></span> <span data-ttu-id="4138f-108">Portanto, as superfícies AI44 e IA44 permitem 16 cores diferentes com 16 valores de transparência diferentes ou 256 representações de pixel diferentes.</span><span class="sxs-lookup"><span data-stu-id="4138f-108">Therefore, AI44 and IA44 surfaces allow for 16 different colors at 16 different transparency values, or 256 different pixel representations.</span></span> <span data-ttu-id="4138f-109">Com o AI44, o alfa é armazenado no Hi-Nibble, em IA44 o alfa é armazenado no meio-Nibble.</span><span class="sxs-lookup"><span data-stu-id="4138f-109">With AI44 the alpha is stored in the hi-nibble, in IA44 the alpha is stored in the lo-nibble.</span></span> <span data-ttu-id="4138f-110">Ambos os formatos são muito úteis para imagens de subimagem de DVD e imagens Line21 e Teletext.</span><span class="sxs-lookup"><span data-stu-id="4138f-110">Both formats are very useful for DVD sub-picture images and Line21 and Teletext images.</span></span> <span data-ttu-id="4138f-111">A Microsoft prefere a versão AI44 porque é um pouco mais fácil gerar texto usando esse formato.</span><span class="sxs-lookup"><span data-stu-id="4138f-111">Microsoft prefers the AI44 version because it is slightly easier to generate text using this format.</span></span>

| <span data-ttu-id="4138f-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="4138f-112">Subtype</span></span>            | <span data-ttu-id="4138f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4138f-113">Description</span></span>                                                 |
|--------------------|-------------------------------------------------------------|
| <span data-ttu-id="4138f-114">MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="4138f-114">MEDIASUBTYPE\_AI44</span></span> | <span data-ttu-id="4138f-115">Para subimagems e sobreposições de texto.</span><span class="sxs-lookup"><span data-stu-id="4138f-115">For subpicture and text overlays.</span></span> <span data-ttu-id="4138f-116">Consulte a descrição anterior.</span><span class="sxs-lookup"><span data-stu-id="4138f-116">See previous description.</span></span> |
| <span data-ttu-id="4138f-117">MEDIASUBTYPE \_ IA44</span><span class="sxs-lookup"><span data-stu-id="4138f-117">MEDIASUBTYPE\_IA44</span></span> | <span data-ttu-id="4138f-118">Para subimagems e sobreposições de texto.</span><span class="sxs-lookup"><span data-stu-id="4138f-118">For subpicture and text overlays.</span></span> <span data-ttu-id="4138f-119">Consulte a descrição anterior.</span><span class="sxs-lookup"><span data-stu-id="4138f-119">See previous description.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4138f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4138f-120">Requirements</span></span>



| <span data-ttu-id="4138f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4138f-121">Requirement</span></span> | <span data-ttu-id="4138f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4138f-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4138f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4138f-123">Header</span></span><br/> | <dl> <span data-ttu-id="4138f-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4138f-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4138f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4138f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4138f-126">Subtipos de vídeo</span><span class="sxs-lookup"><span data-stu-id="4138f-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




