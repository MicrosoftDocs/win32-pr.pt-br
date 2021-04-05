---
description: Especifica a taxa média de bits do fluxo de áudio codificado, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: Propriedade AVEncAudioMeanBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e311686e6113003593c8a6dbe02a9fca1f30b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010048"
---
# <a name="avencaudiomeanbitrate-property"></a><span data-ttu-id="6ef4a-104">Propriedade AVEncAudioMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="6ef4a-104">AVEncAudioMeanBitRate property</span></span>

<span data-ttu-id="6ef4a-105">Especifica a taxa média de bits do fluxo de áudio codificado, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="6ef4a-105">Specifies the average bit rate of the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="6ef4a-106">Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="6ef4a-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="6ef4a-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6ef4a-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ef4a-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6ef4a-108">Data type</span></span>

<span data-ttu-id="6ef4a-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6ef4a-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6ef4a-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="6ef4a-110">Property GUID</span></span>

<span data-ttu-id="6ef4a-111">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="6ef4a-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="6ef4a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6ef4a-112">Property value</span></span>

<span data-ttu-id="6ef4a-113">Os codificadores podem implementar essa propriedade como um conjunto enumerado ou como um intervalo linear.</span><span class="sxs-lookup"><span data-stu-id="6ef4a-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef4a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ef4a-114">Requirements</span></span>



| <span data-ttu-id="6ef4a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ef4a-115">Requirement</span></span> | <span data-ttu-id="6ef4a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6ef4a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef4a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ef4a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef4a-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6ef4a-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6ef4a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ef4a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef4a-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6ef4a-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6ef4a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ef4a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ef4a-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ef4a-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef4a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ef4a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef4a-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="6ef4a-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6ef4a-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6ef4a-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




