---
description: Especifica o fim de uma passagem de codificação.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: Propriedade MFPKEY_ENDOFPASS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827911"
---
# <a name="mfpkey_endofpass-property"></a><span data-ttu-id="65148-103">\_Propriedade MFPKEY ENDOFPASS</span><span class="sxs-lookup"><span data-stu-id="65148-103">MFPKEY\_ENDOFPASS Property</span></span>

<span data-ttu-id="65148-104">Especifica o fim de uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="65148-104">Specifies the end of an encoding pass.</span></span>

## <a name="data-type"></a><span data-ttu-id="65148-105">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="65148-105">Data Type</span></span>

<span data-ttu-id="65148-106">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="65148-106">**VT\_BOOL**</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="65148-107">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="65148-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="65148-108">g \_ wszWMVCEndOfPass</span><span class="sxs-lookup"><span data-stu-id="65148-108">g\_wszWMVCEndOfPass</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="65148-109">Tipo de dados para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="65148-109">Data Type for IPropertyBag</span></span>

<span data-ttu-id="65148-110">Nenhum tipo de dados é necessário.</span><span class="sxs-lookup"><span data-stu-id="65148-110">No data type is required.</span></span> <span data-ttu-id="65148-111">Para definir essa propriedade, passe uma **variante** não inicializada.</span><span class="sxs-lookup"><span data-stu-id="65148-111">To set this property, pass an uninitialized **VARIANT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="65148-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="65148-112">Remarks</span></span>

<span data-ttu-id="65148-113">Essa propriedade não é uma propriedade normal porque tem o mesmo efeito, independentemente de o valor ser VARIANT \_ true ou Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="65148-113">This property is not a normal property because it has the same effect regardless of whether the value is VARIANT\_TRUE or VARIANT\_FALSE.</span></span> <span data-ttu-id="65148-114">Você deve definir essa propriedade depois de processar os últimos exemplos de entrada para uma passagem de pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="65148-114">You must set this property after you process the last input samples for a preprocessing pass.</span></span> <span data-ttu-id="65148-115">Se você estiver executando várias passagens, deverá definir essa propriedade no final de cada passagem de pré-processamento (no momento, nenhum dos codecs oferece suporte a mais de um).</span><span class="sxs-lookup"><span data-stu-id="65148-115">If you are performing multiple passes, you must set this property at the end of each preprocessing pass (at present none of the codecs supports more than one).</span></span> <span data-ttu-id="65148-116">Se você não definir essa propriedade, o codec irá pressupor que você ainda está passando exemplos para pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="65148-116">If you do not set this property, the codec will assume that you are still passing samples for preprocessing.</span></span>

## <a name="requirements"></a><span data-ttu-id="65148-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65148-117">Requirements</span></span>



| <span data-ttu-id="65148-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65148-118">Requirement</span></span> | <span data-ttu-id="65148-119">Valor</span><span class="sxs-lookup"><span data-stu-id="65148-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65148-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65148-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65148-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="65148-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65148-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65148-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65148-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65148-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65148-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65148-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65148-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="65148-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65148-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="65148-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65148-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="65148-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




