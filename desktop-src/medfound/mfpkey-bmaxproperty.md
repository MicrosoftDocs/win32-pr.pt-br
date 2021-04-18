---
description: Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por MFPKEY \_ RMAX).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: Propriedade MFPKEY_BMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811532"
---
# <a name="mfpkey_bmax-property"></a><span data-ttu-id="3272e-103">\_Propriedade MFPKEY BMAX</span><span class="sxs-lookup"><span data-stu-id="3272e-103">MFPKEY\_BMAX Property</span></span>

<span data-ttu-id="3272e-104">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="3272e-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by [MFPKEY\_RMAX](mfpkey-rmaxproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3272e-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3272e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3272e-106">g \_ wszWMVCBMax</span><span class="sxs-lookup"><span data-stu-id="3272e-106">g\_wszWMVCBMax</span></span>

## <a name="data-type"></a><span data-ttu-id="3272e-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3272e-107">Data Type</span></span>

<span data-ttu-id="3272e-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="3272e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="3272e-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="3272e-109">Default Value</span></span>

<span data-ttu-id="3272e-110">Sem padrão.</span><span class="sxs-lookup"><span data-stu-id="3272e-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="3272e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3272e-111">Remarks</span></span>

<span data-ttu-id="3272e-112">Você deve definir esse valor para a codificação de taxa de bits de pico restrita.</span><span class="sxs-lookup"><span data-stu-id="3272e-112">You must set this value for peak-constrained VBR encoding.</span></span> <span data-ttu-id="3272e-113">Depois de começar a processar amostras, você não deve consultar esse valor até concluir a codificação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="3272e-113">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="3272e-114">O codec interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="3272e-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="3272e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3272e-115">Requirements</span></span>



| <span data-ttu-id="3272e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3272e-116">Requirement</span></span> | <span data-ttu-id="3272e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3272e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3272e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3272e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3272e-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3272e-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3272e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3272e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3272e-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3272e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3272e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3272e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3272e-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3272e-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3272e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3272e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3272e-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3272e-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




