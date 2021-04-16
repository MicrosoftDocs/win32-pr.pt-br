---
description: Especifica o número de quadros após o quadro atual que o codec avaliará antes de codificar o quadro atual.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Propriedade MFPKEY_LOOKAHEAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761016"
---
# <a name="mfpkey_lookahead-property"></a><span data-ttu-id="d7504-103">\_Propriedade LOOKAHEAD de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="d7504-103">MFPKEY\_LOOKAHEAD Property</span></span>

<span data-ttu-id="d7504-104">Especifica o número de quadros após o quadro atual que o codec avaliará antes de codificar o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="d7504-104">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d7504-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d7504-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d7504-106">g \_ wszWMVCLookAhead</span><span class="sxs-lookup"><span data-stu-id="d7504-106">g\_wszWMVCLookAhead</span></span>

## <a name="data-type"></a><span data-ttu-id="d7504-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d7504-107">Data Type</span></span>

<span data-ttu-id="d7504-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="d7504-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d7504-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d7504-109">Default Value</span></span>

<span data-ttu-id="d7504-110">0</span><span class="sxs-lookup"><span data-stu-id="d7504-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="d7504-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7504-111">Remarks</span></span>

<span data-ttu-id="d7504-112">Quando o codec usa antecipadamente, ele pode codificar o vídeo com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="d7504-112">When the codec uses lookahead, it can encode the video more efficiently.</span></span>

<span data-ttu-id="d7504-113">O objeto gravador do SDK do Windows Media Format espera que o codec codifique cada exemplo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d7504-113">The writer object of the Windows Media Format SDK expects the codec to encode each sample immediately.</span></span> <span data-ttu-id="d7504-114">Como resultado, esse recurso não funciona corretamente no software que usa o objeto do gravador (incluindo o Windows Media Encoder e o Windows Media Player).</span><span class="sxs-lookup"><span data-stu-id="d7504-114">As a result, this feature does not work properly in software that uses the writer object (including Windows Media Encoder and Windows Media Player).</span></span> <span data-ttu-id="d7504-115">Todas as extensões de unidade de dados associadas a quadros de vídeo serão anexadas ao quadro de saída errado.</span><span class="sxs-lookup"><span data-stu-id="d7504-115">Any data unit extensions associated with video frames will be attached to the wrong output frame.</span></span> <span data-ttu-id="d7504-116">O número de quadros pelos quais as extensões de unidade de dados são colocadas incorretas é igual ao número de quadros de antecipação que são usados.</span><span class="sxs-lookup"><span data-stu-id="d7504-116">The number of frames by which the data unit extensions are misplaced is equal to the number of frames of lookahead that are used.</span></span>

<span data-ttu-id="d7504-117">Os valores de lookahead válidos variam de 0 a 16 quadros.</span><span class="sxs-lookup"><span data-stu-id="d7504-117">Valid lookahead values range from 0 to 16 frames.</span></span> <span data-ttu-id="d7504-118">O valor recomendado é 16.</span><span class="sxs-lookup"><span data-stu-id="d7504-118">The recommended value is 16.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7504-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7504-119">Requirements</span></span>



| <span data-ttu-id="d7504-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7504-120">Requirement</span></span> | <span data-ttu-id="d7504-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d7504-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7504-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7504-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7504-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d7504-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7504-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7504-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7504-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7504-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7504-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7504-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7504-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7504-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7504-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7504-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7504-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7504-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




