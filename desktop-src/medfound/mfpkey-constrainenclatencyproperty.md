---
description: Especifica se o codificador é restrito por um requisito de latência máxima.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: Propriedade MFPKEY_CONSTRAINENCLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810700"
---
# <a name="mfpkey_constrainenclatency-property"></a><span data-ttu-id="b4a95-103">\_Propriedade MFPKEY CONSTRAINENCLATENCY</span><span class="sxs-lookup"><span data-stu-id="b4a95-103">MFPKEY\_CONSTRAINENCLATENCY Property</span></span>

<span data-ttu-id="b4a95-104">Especifica se o codificador é restrito por um requisito de latência máxima.</span><span class="sxs-lookup"><span data-stu-id="b4a95-104">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b4a95-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b4a95-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b4a95-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b4a95-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b4a95-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="b4a95-107">Data Type</span></span>

<span data-ttu-id="b4a95-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="b4a95-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="b4a95-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="b4a95-109">Default Value</span></span>

<span data-ttu-id="b4a95-110">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="b4a95-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a95-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4a95-111">Remarks</span></span>

<span data-ttu-id="b4a95-112">Se você deixar essa propriedade com o valor padrão de **Variant \_ false**, o codificador enumerará um conjunto padrão de modos que têm cerca de 2000 milissegundos de latência do codificador.</span><span class="sxs-lookup"><span data-stu-id="b4a95-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 2000 milliseconds of encoder latency.</span></span> <span data-ttu-id="b4a95-113">Se você definir essa propriedade como **Variant \_ true**, também deverá especificar uma latência máxima do codificador definindo a propriedade [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a95-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum encoder latency by setting the [**MFPKEY\_MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) property.</span></span> <span data-ttu-id="b4a95-114">Nesse caso, o codificador cria modos que atendem ao requisito de latência e enumera apenas esses modos.</span><span class="sxs-lookup"><span data-stu-id="b4a95-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="b4a95-115">O codificador garante um exemplo de saída assim que o codificador recebeu entrada para um período de tempo igual a **MFPKEY \_ MAXENCLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="b4a95-115">The encoder guarantees an output sample as soon as the encoder has received input for a time period equal to **MFPKEY\_MAXENCLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a95-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a95-116">Requirements</span></span>



| <span data-ttu-id="b4a95-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a95-117">Requirement</span></span> | <span data-ttu-id="b4a95-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b4a95-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a95-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4a95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a95-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4a95-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b4a95-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4a95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a95-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4a95-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4a95-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4a95-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4a95-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a95-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a95-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4a95-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a95-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4a95-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
