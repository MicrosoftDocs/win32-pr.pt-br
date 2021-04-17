---
description: Especifica se o codificador é restrito por um requisito de latência de decodificador máximo.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: Propriedade MFPKEY_CONSTRAINDECLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790501"
---
# <a name="mfpkey_constraindeclatency-property"></a><span data-ttu-id="33961-103">\_Propriedade MFPKEY CONSTRAINDECLATENCY</span><span class="sxs-lookup"><span data-stu-id="33961-103">MFPKEY\_CONSTRAINDECLATENCY Property</span></span>

<span data-ttu-id="33961-104">Especifica se o codificador é restrito por um requisito de latência de decodificador máximo.</span><span class="sxs-lookup"><span data-stu-id="33961-104">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="33961-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="33961-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="33961-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="33961-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="33961-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="33961-107">Data Type</span></span>

<span data-ttu-id="33961-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="33961-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="33961-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="33961-109">Default Value</span></span>

<span data-ttu-id="33961-110">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="33961-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="33961-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="33961-111">Remarks</span></span>

<span data-ttu-id="33961-112">Se você deixar essa propriedade com seu valor padrão de **variante \_ false**, o codificador enumerará um conjunto padrão de modos que têm cerca de 1500 milissegundos de latência de decodificador.</span><span class="sxs-lookup"><span data-stu-id="33961-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 1500 milliseconds of decoder latency.</span></span> <span data-ttu-id="33961-113">Se você definir essa propriedade como **Variant \_ true**, também deverá especificar uma latência máxima de decodificador definindo a propriedade [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="33961-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum decoder latency by setting the [**MFPKEY\_MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) property.</span></span> <span data-ttu-id="33961-114">Nesse caso, o codificador cria modos que atendem ao requisito de latência e enumera apenas esses modos.</span><span class="sxs-lookup"><span data-stu-id="33961-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="33961-115">O codificador garante que os requisitos de preroll (tamanho do buffer do decodificador) sejam menores ou iguais a **MFPKEY \_ MAXDECLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="33961-115">The encoder ensures that the preroll requirements (decoder buffer size) are less than or equal to **MFPKEY\_MAXDECLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33961-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33961-116">Requirements</span></span>



| <span data-ttu-id="33961-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="33961-117">Requirement</span></span> | <span data-ttu-id="33961-118">Valor</span><span class="sxs-lookup"><span data-stu-id="33961-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33961-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33961-119">Minimum supported client</span></span><br/> | <span data-ttu-id="33961-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33961-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="33961-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33961-121">Minimum supported server</span></span><br/> | <span data-ttu-id="33961-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33961-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33961-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33961-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="33961-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33961-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33961-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="33961-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33961-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33961-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
