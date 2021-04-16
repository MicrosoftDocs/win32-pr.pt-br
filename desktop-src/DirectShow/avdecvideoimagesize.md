---
description: Obtém o tamanho da imagem decodificada, em pixels.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Propriedade AVDecVideoImageSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757447"
---
# <a name="avdecvideoimagesize-property"></a><span data-ttu-id="41f2d-103">Propriedade AVDecVideoImageSize</span><span class="sxs-lookup"><span data-stu-id="41f2d-103">AVDecVideoImageSize property</span></span>

<span data-ttu-id="41f2d-104">Obtém o tamanho da imagem decodificada, em pixels.</span><span class="sxs-lookup"><span data-stu-id="41f2d-104">Gets the size of the decoded image, in pixels.</span></span>

<span data-ttu-id="41f2d-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="41f2d-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="41f2d-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="41f2d-106">Data type</span></span>

<span data-ttu-id="41f2d-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="41f2d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="41f2d-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="41f2d-108">Property GUID</span></span>

<span data-ttu-id="41f2d-109">**CODECAPI \_ AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="41f2d-109">**CODECAPI\_AVDecVideoImageSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="41f2d-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="41f2d-110">Property value</span></span>

<span data-ttu-id="41f2d-111">Os 16 bits altos contêm a largura e os 16 bits baixos contêm a altura.</span><span class="sxs-lookup"><span data-stu-id="41f2d-111">The high 16 bits contain the width, and the low 16 bits contain the height.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f2d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="41f2d-112">Remarks</span></span>

<span data-ttu-id="41f2d-113">O número de canais inclui o canal de baixo efeito de frequência (LFE), se presente.</span><span class="sxs-lookup"><span data-stu-id="41f2d-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f2d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41f2d-114">Requirements</span></span>



| <span data-ttu-id="41f2d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="41f2d-115">Requirement</span></span> | <span data-ttu-id="41f2d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="41f2d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41f2d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41f2d-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="41f2d-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="41f2d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41f2d-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="41f2d-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="41f2d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41f2d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f2d-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f2d-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41f2d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="41f2d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f2d-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="41f2d-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="41f2d-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="41f2d-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




