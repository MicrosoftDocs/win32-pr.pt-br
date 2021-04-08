---
description: Habilita ou desabilita o modo de geração de miniatura em um decodificador de vídeo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propriedade AVDecVideoThumbnailGenerationMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920054"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a><span data-ttu-id="c4637-103">Propriedade AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="c4637-103">AVDecVideoThumbnailGenerationMode property</span></span>

<span data-ttu-id="c4637-104">Habilita ou desabilita o modo de geração de miniatura em um decodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c4637-104">Enables or disables thumbnail generation mode in a video decoder.</span></span>

<span data-ttu-id="c4637-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c4637-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c4637-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c4637-106">Data type</span></span>

<span data-ttu-id="c4637-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="c4637-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c4637-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="c4637-108">Property GUID</span></span>

<span data-ttu-id="c4637-109">**CODECAPI \_ AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="c4637-109">**CODECAPI\_AVDecVideoThumbnailGenerationMode**</span></span>

## <a name="remarks"></a><span data-ttu-id="c4637-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4637-110">Remarks</span></span>

<span data-ttu-id="c4637-111">Se o valor for **Variant \_ true**, o decodificador usará uma configuração otimizada para gerar imagens em miniatura rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c4637-111">If the value is **VARIANT\_TRUE**, the decoder uses a setting that is optimized to generate thumbnail images quickly.</span></span> <span data-ttu-id="c4637-112">(Por exemplo, ele pode ignorar os quadros B ou P.) Caso contrário, se o valor for **Variant \_ false**, o decodificador usará suas configurações de decodificação normais.</span><span class="sxs-lookup"><span data-stu-id="c4637-112">(For example, it might skip B or P frames.) Otherwise, if the value is **VARIANT\_FALSE**, the decoder uses its normal decoding settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4637-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4637-113">Requirements</span></span>



| <span data-ttu-id="c4637-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4637-114">Requirement</span></span> | <span data-ttu-id="c4637-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c4637-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4637-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4637-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c4637-117">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c4637-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c4637-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4637-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c4637-119">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c4637-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c4637-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4637-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4637-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4637-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4637-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4637-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4637-123">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="c4637-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c4637-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c4637-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




