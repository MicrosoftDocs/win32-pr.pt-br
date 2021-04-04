---
description: Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem da saída do codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: Propriedade MFPKEY_CRISP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661878"
---
# <a name="mfpkey_crisp-property"></a><span data-ttu-id="acb7a-103">\_Propriedade MFPKEY Crisp</span><span class="sxs-lookup"><span data-stu-id="acb7a-103">MFPKEY\_CRISP Property</span></span>

<span data-ttu-id="acb7a-104">Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem da saída do codec.</span><span class="sxs-lookup"><span data-stu-id="acb7a-104">Specifies a numeric representation of the tradeoff between motion smoothness and image quality of codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="acb7a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="acb7a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="acb7a-106">g \_ wszWMVCCrisp</span><span class="sxs-lookup"><span data-stu-id="acb7a-106">g\_wszWMVCCrisp</span></span>

## <a name="data-type"></a><span data-ttu-id="acb7a-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="acb7a-107">Data Type</span></span>

<span data-ttu-id="acb7a-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="acb7a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="acb7a-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="acb7a-109">Default Value</span></span>

<span data-ttu-id="acb7a-110">75</span><span class="sxs-lookup"><span data-stu-id="acb7a-110">75</span></span>

## <a name="remarks"></a><span data-ttu-id="acb7a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="acb7a-111">Remarks</span></span>

<span data-ttu-id="acb7a-112">Esse valor inteiro pode variar de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="acb7a-112">This integer value can range from 0 to 100.</span></span> <span data-ttu-id="acb7a-113">Quanto maior o valor, mais o codec otimizará a codificação para a qualidade da imagem de quadros individuais, o que geralmente reduz a suavidade do movimento.</span><span class="sxs-lookup"><span data-stu-id="acb7a-113">The higher the value, the more the codec will optimize encoding for the image quality of individual frames, which usually reduces motion smoothness.</span></span>

<span data-ttu-id="acb7a-114">Essa propriedade deve ser definida somente para a codificação de taxa de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="acb7a-114">This property should be set only for constant-bit-rate (CBR) encoding.</span></span> <span data-ttu-id="acb7a-115">As otimizações para a codificação de taxa de bits variável (VBR) funcionam de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="acb7a-115">The optimizations for variable-bit-rate (VBR) encoding work differently.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb7a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acb7a-116">Requirements</span></span>



| <span data-ttu-id="acb7a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="acb7a-117">Requirement</span></span> | <span data-ttu-id="acb7a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="acb7a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acb7a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb7a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="acb7a-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="acb7a-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="acb7a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb7a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="acb7a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="acb7a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acb7a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="acb7a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb7a-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb7a-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acb7a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="acb7a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb7a-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acb7a-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




