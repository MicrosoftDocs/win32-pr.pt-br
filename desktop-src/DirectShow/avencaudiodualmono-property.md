---
description: Propriedade AVEncAudioDualMono – especifica se o áudio de 2 canais está codificado como estéreo ou duplo mono.
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Propriedade AVEncAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096574"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="d2094-103">Propriedade AVEncAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="d2094-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="d2094-104">Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.</span><span class="sxs-lookup"><span data-stu-id="d2094-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="d2094-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d2094-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2094-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d2094-106">Data type</span></span>

<span data-ttu-id="d2094-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d2094-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d2094-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="d2094-108">Property GUID</span></span>

<span data-ttu-id="d2094-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="d2094-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="d2094-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d2094-110">Property value</span></span>

<span data-ttu-id="d2094-111">O valor dessa propriedade é um membro da enumeração [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="d2094-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2094-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2094-112">Remarks</span></span>

<span data-ttu-id="d2094-113">Essa propriedade não se aplica a codificadores de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="d2094-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="d2094-114">Para áudio MPEG, use a propriedade [**AVEncMPACodingMode**](avencmpacodingmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d2094-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2094-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2094-115">Requirements</span></span>



| <span data-ttu-id="d2094-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2094-116">Requirement</span></span> | <span data-ttu-id="d2094-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d2094-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2094-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2094-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2094-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2094-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d2094-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2094-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2094-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2094-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d2094-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2094-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2094-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2094-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2094-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d2094-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2094-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="d2094-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d2094-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d2094-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

