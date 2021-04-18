---
description: Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Propriedade AVEncAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a5b684638133a1449fc849348cdfd8627533fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105780449"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="455d9-103">Propriedade AVEncAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="455d9-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="455d9-104">Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.</span><span class="sxs-lookup"><span data-stu-id="455d9-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="455d9-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="455d9-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="455d9-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="455d9-106">Data type</span></span>

<span data-ttu-id="455d9-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="455d9-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="455d9-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="455d9-108">Property GUID</span></span>

<span data-ttu-id="455d9-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="455d9-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="455d9-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="455d9-110">Property value</span></span>

<span data-ttu-id="455d9-111">O valor dessa propriedade é um membro da enumeração [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="455d9-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="455d9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="455d9-112">Remarks</span></span>

<span data-ttu-id="455d9-113">Essa propriedade não se aplica a codificadores de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="455d9-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="455d9-114">Para áudio MPEG, use a propriedade [**AVEncMPACodingMode**](avencmpacodingmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="455d9-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="455d9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="455d9-115">Requirements</span></span>



| <span data-ttu-id="455d9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="455d9-116">Requirement</span></span> | <span data-ttu-id="455d9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="455d9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="455d9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="455d9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="455d9-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="455d9-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="455d9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="455d9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="455d9-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="455d9-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="455d9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="455d9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="455d9-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="455d9-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="455d9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="455d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455d9-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="455d9-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="455d9-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="455d9-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

