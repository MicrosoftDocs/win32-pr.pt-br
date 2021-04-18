---
description: Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits de variável restrita (VBR) em sua taxa de bits média (especificada por MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: Propriedade MFPKEY_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781616"
---
# <a name="mfpkey_bavg-property"></a><span data-ttu-id="1fe0d-103">\_Propriedade MFPKEY BAVG</span><span class="sxs-lookup"><span data-stu-id="1fe0d-103">MFPKEY\_BAVG Property</span></span>

<span data-ttu-id="1fe0d-104">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits de variável restrita (VBR) em sua taxa de bits média (especificada por [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="1fe0d-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by [MFPKEY\_RAVG](mfpkey-ravgproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1fe0d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1fe0d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1fe0d-106">g \_ wszWMVCBAvg</span><span class="sxs-lookup"><span data-stu-id="1fe0d-106">g\_wszWMVCBAvg</span></span>

## <a name="data-type"></a><span data-ttu-id="1fe0d-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="1fe0d-107">Data Type</span></span>

<span data-ttu-id="1fe0d-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="1fe0d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1fe0d-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="1fe0d-109">Default Value</span></span>

<span data-ttu-id="1fe0d-110">Nenhum valor padrão, mas o codec calculará um valor apropriado com base nas outras configurações de taxa de bits restritas.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-110">No default value, but the codec will compute an appropriate value based on the other constrained VBR settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fe0d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fe0d-111">Remarks</span></span>

<span data-ttu-id="1fe0d-112">Esse valor é calculado pelo codec após a passagem da codificação final.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-112">This value is computed by the codec after the final encoding pass.</span></span> <span data-ttu-id="1fe0d-113">Você não deve consultar esse valor até que a codificação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-113">You should not query for this value until after encoding is complete.</span></span> <span data-ttu-id="1fe0d-114">O codec interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe0d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fe0d-115">Requirements</span></span>



| <span data-ttu-id="1fe0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fe0d-116">Requirement</span></span> | <span data-ttu-id="1fe0d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1fe0d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe0d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fe0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe0d-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1fe0d-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1fe0d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fe0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe0d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fe0d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1fe0d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fe0d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fe0d-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fe0d-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fe0d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fe0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe0d-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1fe0d-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




