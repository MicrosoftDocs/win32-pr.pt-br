---
description: Especifica como o decodificador Reproduz áudio mono duplo.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Propriedade AVDecAudioDualMonoReproMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646045"
---
# <a name="avdecaudiodualmonorepromode-property"></a><span data-ttu-id="736bd-103">Propriedade AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="736bd-103">AVDecAudioDualMonoReproMode property</span></span>

<span data-ttu-id="736bd-104">Especifica como o decodificador Reproduz áudio mono duplo.</span><span class="sxs-lookup"><span data-stu-id="736bd-104">Specifies how the decoder reproduces dual mono audio.</span></span>

<span data-ttu-id="736bd-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="736bd-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="736bd-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="736bd-106">Data type</span></span>

<span data-ttu-id="736bd-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="736bd-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="736bd-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="736bd-108">Property GUID</span></span>

<span data-ttu-id="736bd-109">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="736bd-109">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="736bd-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="736bd-110">Property value</span></span>

<span data-ttu-id="736bd-111">O valor dessa propriedade é um membro da enumeração [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) .</span><span class="sxs-lookup"><span data-stu-id="736bd-111">The value of this property is a member of the [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="736bd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="736bd-112">Remarks</span></span>

<span data-ttu-id="736bd-113">Essas propriedades se aplicam somente quando o fluxo de bits de entrada do decodificador contém áudio mono duplo.</span><span class="sxs-lookup"><span data-stu-id="736bd-113">This properties applies only when the decoder's input bit stream contains dual mono audio.</span></span> <span data-ttu-id="736bd-114">Para testar essa condição, obtenha o valor da propriedade [AVDecAudioDualMono](avdecaudiodualmono-property.md) .</span><span class="sxs-lookup"><span data-stu-id="736bd-114">To test this condition, get the value of the [AVDecAudioDualMono](avdecaudiodualmono-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="736bd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="736bd-115">Requirements</span></span>



| <span data-ttu-id="736bd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="736bd-116">Requirement</span></span> | <span data-ttu-id="736bd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="736bd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="736bd-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="736bd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="736bd-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="736bd-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="736bd-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="736bd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="736bd-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="736bd-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="736bd-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="736bd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="736bd-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="736bd-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="736bd-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="736bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="736bd-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="736bd-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="736bd-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="736bd-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




