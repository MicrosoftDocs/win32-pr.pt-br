---
description: Especifica o tamanho das unidades de acesso ao vídeo, em bytes. Essa propriedade só se aplica a modos de controle de taxa de bits variável (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Propriedade AVEncVideoCodedVideoAccessUnitSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919713"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a><span data-ttu-id="b1502-104">Propriedade AVEncVideoCodedVideoAccessUnitSize</span><span class="sxs-lookup"><span data-stu-id="b1502-104">AVEncVideoCodedVideoAccessUnitSize property</span></span>

<span data-ttu-id="b1502-105">Especifica o tamanho das unidades de acesso ao vídeo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b1502-105">Specifies the size of the video access units, in bytes.</span></span> <span data-ttu-id="b1502-106">Essa propriedade só se aplica a modos de controle de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="b1502-106">This property applies only to variable bit rate (VBR) control modes.</span></span>

<span data-ttu-id="b1502-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b1502-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1502-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b1502-108">Data type</span></span>

<span data-ttu-id="b1502-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b1502-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b1502-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="b1502-110">Property GUID</span></span>

<span data-ttu-id="b1502-111">**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**</span><span class="sxs-lookup"><span data-stu-id="b1502-111">**CODECAPI\_AVEncVideoCodedVideoAccessUnitSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="b1502-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b1502-112">Property value</span></span>

<span data-ttu-id="b1502-113">Essa propriedade é retornada como um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="b1502-113">This property is returned as a range of values.</span></span> <span data-ttu-id="b1502-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="b1502-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1502-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1502-115">Requirements</span></span>



| <span data-ttu-id="b1502-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1502-116">Requirement</span></span> | <span data-ttu-id="b1502-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b1502-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1502-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1502-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1502-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b1502-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b1502-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1502-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1502-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b1502-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b1502-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1502-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1502-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1502-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1502-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1502-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1502-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="b1502-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b1502-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b1502-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




