---
description: Especifica o nível inicial do buffer de codificação, em bits. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Propriedade AVEncCommonBufferInLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087850"
---
# <a name="avenccommonbufferinlevel-property"></a><span data-ttu-id="3e646-104">Propriedade AVEncCommonBufferInLevel</span><span class="sxs-lookup"><span data-stu-id="3e646-104">AVEncCommonBufferInLevel property</span></span>

<span data-ttu-id="3e646-105">Especifica o nível inicial do buffer de codificação, em bits.</span><span class="sxs-lookup"><span data-stu-id="3e646-105">Specifies the initial level of the encoding buffer, in bits.</span></span> <span data-ttu-id="3e646-106">Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="3e646-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="3e646-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3e646-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e646-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3e646-108">Data type</span></span>

<span data-ttu-id="3e646-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="3e646-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3e646-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="3e646-110">Property GUID</span></span>

<span data-ttu-id="3e646-111">**CODECAPI \_ AVEncCommonBufferInLevel**</span><span class="sxs-lookup"><span data-stu-id="3e646-111">**CODECAPI\_AVEncCommonBufferInLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="3e646-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3e646-112">Property value</span></span>

<span data-ttu-id="3e646-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="3e646-113">This property has a linear range of values.</span></span> <span data-ttu-id="3e646-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="3e646-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e646-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e646-115">Remarks</span></span>

<span data-ttu-id="3e646-116">Para o vídeo MPEG, essa propriedade define a totalidade do verificador de buffer de vídeo (VBV) inicial.</span><span class="sxs-lookup"><span data-stu-id="3e646-116">For MPEG video, this property defines the initial video buffer verifier (VBV) fullness.</span></span> <span data-ttu-id="3e646-117">Ele dá suporte à concatenação de fluxos durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="3e646-117">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e646-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e646-118">Requirements</span></span>



| <span data-ttu-id="3e646-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e646-119">Requirement</span></span> | <span data-ttu-id="3e646-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3e646-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e646-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e646-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3e646-122">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3e646-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3e646-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e646-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3e646-124">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3e646-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3e646-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e646-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e646-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e646-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e646-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e646-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e646-128">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="3e646-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3e646-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3e646-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




