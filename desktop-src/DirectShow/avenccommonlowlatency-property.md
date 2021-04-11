---
description: Especifica se o fluxo de saída deve ser estruturado para que o fluxo codificado tenha uma latência de decodificação baixa.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propriedade AVEncCommonLowLatency (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163864"
---
# <a name="avenccommonlowlatency-property"></a><span data-ttu-id="44404-103">Propriedade AVEncCommonLowLatency</span><span class="sxs-lookup"><span data-stu-id="44404-103">AVEncCommonLowLatency property</span></span>

<span data-ttu-id="44404-104">Especifica se o fluxo de saída deve ser estruturado para que o fluxo codificado tenha uma latência de decodificação baixa.</span><span class="sxs-lookup"><span data-stu-id="44404-104">Specifies whether the output stream should be structured so that the encoded stream has a low decoding latency.</span></span>

<span data-ttu-id="44404-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="44404-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="44404-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44404-106">Data type</span></span>

<span data-ttu-id="44404-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="44404-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="44404-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="44404-108">Property GUID</span></span>

<span data-ttu-id="44404-109">**CODECAPI \_ AVEncCommonLowLatency**</span><span class="sxs-lookup"><span data-stu-id="44404-109">**CODECAPI\_AVEncCommonLowLatency**</span></span>

## <a name="remarks"></a><span data-ttu-id="44404-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="44404-110">Remarks</span></span>

<span data-ttu-id="44404-111">A decodificação da latência é definida como a quantidade de dados que o decodificador deve armazenar em buffer.</span><span class="sxs-lookup"><span data-stu-id="44404-111">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="44404-112">Por exemplo, definir essa propriedade como **Variant \_ true** em um codificador de vídeo MPEG limita os tipos de estruturas GOP que o codificador pode usar.</span><span class="sxs-lookup"><span data-stu-id="44404-112">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

## <a name="requirements"></a><span data-ttu-id="44404-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44404-113">Requirements</span></span>



| <span data-ttu-id="44404-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="44404-114">Requirement</span></span> | <span data-ttu-id="44404-115">Valor</span><span class="sxs-lookup"><span data-stu-id="44404-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44404-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44404-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44404-117">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44404-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="44404-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44404-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44404-119">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44404-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="44404-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44404-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="44404-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44404-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44404-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="44404-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44404-123">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="44404-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="44404-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="44404-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




