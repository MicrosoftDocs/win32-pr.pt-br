---
description: Especifica o aumento Delta entre a imagem quantizador do quadro âncora e a quantizador da imagem do quadro B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: Propriedade MFPKEY_BDELTAQP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810759"
---
# <a name="mfpkey_bdeltaqp-property"></a><span data-ttu-id="a0738-103">\_Propriedade MFPKEY BDELTAQP</span><span class="sxs-lookup"><span data-stu-id="a0738-103">MFPKEY\_BDELTAQP Property</span></span>

<span data-ttu-id="a0738-104">Especifica o aumento Delta entre a imagem quantizador do quadro âncora e a quantizador da imagem do quadro B.</span><span class="sxs-lookup"><span data-stu-id="a0738-104">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a0738-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a0738-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a0738-106">g \_ wszWMVCBDeltaQP</span><span class="sxs-lookup"><span data-stu-id="a0738-106">g\_wszWMVCBDeltaQP</span></span>

## <a name="data-type"></a><span data-ttu-id="a0738-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="a0738-107">Data Type</span></span>

<span data-ttu-id="a0738-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="a0738-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a0738-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="a0738-109">Default Value</span></span>

<span data-ttu-id="a0738-110">0</span><span class="sxs-lookup"><span data-stu-id="a0738-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="a0738-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0738-111">Remarks</span></span>

<span data-ttu-id="a0738-112">O Picture quantizador (QP) é uma medida de como o quadro é compactado.</span><span class="sxs-lookup"><span data-stu-id="a0738-112">Picture quantizer (QP) is a measurement of how compressed a frame is.</span></span> <span data-ttu-id="a0738-113">Valores mais altos representam taxas de compactação maiores.</span><span class="sxs-lookup"><span data-stu-id="a0738-113">Higher values represent higher compression ratios.</span></span> <span data-ttu-id="a0738-114">A QP pode ser definida em incrementos de meio ponto.</span><span class="sxs-lookup"><span data-stu-id="a0738-114">The QP can be set in half-point increments.</span></span> <span data-ttu-id="a0738-115">Normalmente, um quadro B é compactado em um QP igual a ou 0,5 maior do que o QP do quadro âncora.</span><span class="sxs-lookup"><span data-stu-id="a0738-115">A B-frame is typically compressed at a QP the same as or 0.5 higher than the anchor frame's QP.</span></span> <span data-ttu-id="a0738-116">Ao especificar um Delta de QP de B superior a 0, é possível compactar quadros B a uma taxa de compactação ainda maior.</span><span class="sxs-lookup"><span data-stu-id="a0738-116">By specifying a B-frame QP delta higher than 0, it is possible to compress B-frames at an even higher compression ratio.</span></span>

<span data-ttu-id="a0738-117">O Delta QP de quadro B só pode ser definido em incrementos de ponto inteiro.</span><span class="sxs-lookup"><span data-stu-id="a0738-117">The B-frame delta QP can be set only in whole-point increments.</span></span> <span data-ttu-id="a0738-118">Essa propriedade deve ser definida como um valor inteiro de 0 a 31.</span><span class="sxs-lookup"><span data-stu-id="a0738-118">This property must be set to an integer value from 0 to 31.</span></span> <span data-ttu-id="a0738-119">O valor recomendado é 1.</span><span class="sxs-lookup"><span data-stu-id="a0738-119">The recommended value is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0738-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0738-120">Requirements</span></span>



| <span data-ttu-id="a0738-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0738-121">Requirement</span></span> | <span data-ttu-id="a0738-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a0738-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0738-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0738-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a0738-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0738-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0738-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0738-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a0738-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0738-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0738-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0738-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0738-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0738-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0738-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0738-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0738-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a0738-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




