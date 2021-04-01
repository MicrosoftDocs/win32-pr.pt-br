---
description: Especifica o número máximo de quadros de referência com suporte no codificador.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Propriedade CODECAPI_AVEncVideoMaxNumRefFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091877"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a><span data-ttu-id="027c8-103">\_Propriedade CODECAPI AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="027c8-103">CODECAPI\_AVEncVideoMaxNumRefFrame property</span></span>

<span data-ttu-id="027c8-104">Especifica o número máximo de quadros de referência com suporte no codificador.</span><span class="sxs-lookup"><span data-stu-id="027c8-104">Specifies the maximum reference frames supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="027c8-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="027c8-105">Data type</span></span>

<span data-ttu-id="027c8-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="027c8-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="027c8-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="027c8-107">Property GUID</span></span>

<span data-ttu-id="027c8-108">**CODECAPI \_ AVEncVideoMaxNumRefFrame**</span><span class="sxs-lookup"><span data-stu-id="027c8-108">**CODECAPI\_AVEncVideoMaxNumRefFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="027c8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="027c8-109">Remarks</span></span>

<span data-ttu-id="027c8-110">Para H. 264, isso é mapeado para a variável de conjunto de parâmetros de sequência **Max \_ num \_ ref \_ frames** , conforme definido na especificação H. 264.</span><span class="sxs-lookup"><span data-stu-id="027c8-110">For H.264, this maps to the Sequence Parameter Set variable **max\_num\_ref\_frames** as defined in H.264 specification.</span></span>

<span data-ttu-id="027c8-111">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="027c8-111">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="027c8-112">Os codificadores podem usar menos quadros de referência para obedecer ao nível especificado no fragmentado.</span><span class="sxs-lookup"><span data-stu-id="027c8-112">Encoders may use fewer reference frames in order to obey the level specified in the bitstream.</span></span>

<span data-ttu-id="027c8-113">Os codificadores devem dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="027c8-113">Encoders shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="027c8-114">Essa é uma propriedade estática, o que significa que ela só pode ser definida antes do início da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="027c8-114">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="027c8-115">O valor padrão recomendado é 2.</span><span class="sxs-lookup"><span data-stu-id="027c8-115">Recommended default value is 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="027c8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="027c8-116">Requirements</span></span>



| <span data-ttu-id="027c8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="027c8-117">Requirement</span></span> | <span data-ttu-id="027c8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="027c8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="027c8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="027c8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="027c8-120">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="027c8-120">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="027c8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="027c8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="027c8-122">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="027c8-122">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="027c8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="027c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="027c8-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="027c8-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027c8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="027c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027c8-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="027c8-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

