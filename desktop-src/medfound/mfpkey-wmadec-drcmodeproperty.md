---
description: Especifica o modo de controle de intervalo dinâmico que será usado pelo decodificador de áudio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: Propriedade MFPKEY_WMADEC_DRCMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164922"
---
# <a name="mfpkey_wmadec_drcmode-property"></a><span data-ttu-id="9fa7c-103">\_Propriedade MFPKEY WMADEC \_ DRCMODE</span><span class="sxs-lookup"><span data-stu-id="9fa7c-103">MFPKEY\_WMADEC\_DRCMODE Property</span></span>

<span data-ttu-id="9fa7c-104">Especifica o modo de controle de intervalo dinâmico que será usado pelo decodificador de áudio.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-104">Specifies the dynamic range control mode that the audio decoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9fa7c-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9fa7c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9fa7c-106">g \_ wszWMACDRCSetting</span><span class="sxs-lookup"><span data-stu-id="9fa7c-106">g\_wszWMACDRCSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="9fa7c-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="9fa7c-107">Data Type</span></span>

<span data-ttu-id="9fa7c-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="9fa7c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9fa7c-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="9fa7c-109">Default Value</span></span>

<span data-ttu-id="9fa7c-110">0</span><span class="sxs-lookup"><span data-stu-id="9fa7c-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="9fa7c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fa7c-111">Remarks</span></span>

<span data-ttu-id="9fa7c-112">Esse valor inteiro varia de 0 a 2.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-112">This integer value ranges from 0 to 2.</span></span> <span data-ttu-id="9fa7c-113">Quanto maior o valor, menor o intervalo dinâmico da saída de áudio descompactado.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-113">The greater the value, the smaller the dynamic range of the uncompressed audio output.</span></span> <span data-ttu-id="9fa7c-114">Um valor de 0 sinaliza o codec para não executar nenhum controle de intervalo dinâmico, ou seja, o codec não alterará o intervalo dinâmico inerente do conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-114">A value of 0 signals the codec to perform no dynamic range control, that is, the codec will not alter the inherent dynamic range of the encoded content.</span></span>

<span data-ttu-id="9fa7c-115">Se esse valor for definido como 1 ou 2, o codec usará as seguintes propriedades para determinar o controle de intervalo dinâmico necessário:</span><span class="sxs-lookup"><span data-stu-id="9fa7c-115">If this value is set to 1 or 2, the codec will use the following properties to determine the needed dynamic range control:</span></span>

-   [<span data-ttu-id="9fa7c-116">MFPKEY \_ WMADRC \_ AVGREF</span><span class="sxs-lookup"><span data-stu-id="9fa7c-116">MFPKEY\_WMADRC\_AVGREF</span></span>](mfpkey-wmadrc-avgrefproperty.md)
-   [<span data-ttu-id="9fa7c-117">MFPKEY \_ WMADRC \_ PEAKREF</span><span class="sxs-lookup"><span data-stu-id="9fa7c-117">MFPKEY\_WMADRC\_PEAKREF</span></span>](mfpkey-wmadrc-peakrefproperty.md)
-   [<span data-ttu-id="9fa7c-118">MFPKEY \_ WMADRC \_ AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="9fa7c-118">MFPKEY\_WMADRC\_AVGTARGET</span></span>](mfpkey-wmadrc-avgtargetproperty.md)
-   [<span data-ttu-id="9fa7c-119">MFPKEY \_ WMADRC \_ PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="9fa7c-119">MFPKEY\_WMADRC\_PEAKTARGET</span></span>](mfpkey-wmadrc-peaktargetproperty.md)

<span data-ttu-id="9fa7c-120">Se você não fornecer valores de destino, o codec fornecerá seu próprio.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-120">If you do not provide target values, the codec will provide its own.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa7c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fa7c-121">Requirements</span></span>



| <span data-ttu-id="9fa7c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fa7c-122">Requirement</span></span> | <span data-ttu-id="9fa7c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9fa7c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa7c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fa7c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa7c-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9fa7c-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9fa7c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fa7c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa7c-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9fa7c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9fa7c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fa7c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fa7c-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fa7c-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa7c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fa7c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa7c-131">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fa7c-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




