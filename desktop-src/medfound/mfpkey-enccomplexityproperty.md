---
description: Especifica a complexidade do algoritmo de codificação.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: Propriedade MFPKEY_ENCCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827912"
---
# <a name="mfpkey_enccomplexity-property"></a><span data-ttu-id="d5356-103">\_Propriedade MFPKEY ENCCOMPLEXITY</span><span class="sxs-lookup"><span data-stu-id="d5356-103">MFPKEY\_ENCCOMPLEXITY Property</span></span>

<span data-ttu-id="d5356-104">Especifica a complexidade do algoritmo de codificação.</span><span class="sxs-lookup"><span data-stu-id="d5356-104">Specifies the complexity of the encoding algorithm.</span></span> <span data-ttu-id="d5356-105">O valor é um inteiro entre 0 e 100, em que 0 especifica o algoritmo menos complexo e 100 especifica o algoritmo mais complexo.</span><span class="sxs-lookup"><span data-stu-id="d5356-105">The value is an integer between 0 and 100, where 0 specifies the least complex algorithm, and 100 specifies the most complex algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d5356-106">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d5356-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="d5356-107">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d5356-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d5356-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d5356-108">Data Type</span></span>

<span data-ttu-id="d5356-109">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d5356-109">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="d5356-110">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d5356-110">Default Value</span></span>

<span data-ttu-id="d5356-111">100 para áudio do Windows Media 10 e Windows Media Audio 10 Professional</span><span class="sxs-lookup"><span data-stu-id="d5356-111">100 for Windows Media Audio 10 and Windows Media Audio 10 Professional</span></span>

<span data-ttu-id="d5356-112">100 para a versão Windows Vista do Windows Media Audio 10 sem perdas</span><span class="sxs-lookup"><span data-stu-id="d5356-112">100 for the Windows Vista release of Windows Media Audio 10 Lossless</span></span>

<span data-ttu-id="d5356-113">0 para a versão do Windows 7 Windows Media Audio 10 sem perdas</span><span class="sxs-lookup"><span data-stu-id="d5356-113">0 for the Windows 7 release Windows Media Audio 10 Lossless</span></span>

## <a name="remarks"></a><span data-ttu-id="d5356-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5356-114">Remarks</span></span>

<span data-ttu-id="d5356-115">Se a propriedade [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiver um valor de **Variant \_ true**, o codificador ajustará a complexidade de seu algoritmo de acordo com o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d5356-115">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_TRUE**, the encoder adjusts the complexity of its algorithm according to the value of this property.</span></span>

<span data-ttu-id="d5356-116">Para o codificador do Windows Media Audio 10 e o codificador do Windows Media Audio 10 Professional, se o valor dessa propriedade for 100, o codificador colocará uma alta demanda na CPU e produzirá a saída de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="d5356-116">For the Windows Media Audio 10 encoder and the Windows Media Audio 10 Professional encoder, if the value of this property is 100, the encoder places a high demand on the CPU and produces the highest quality output.</span></span> <span data-ttu-id="d5356-117">Como o valor dessa propriedade diminui, a demanda na CPU diminui, mas a qualidade da saída também diminui.</span><span class="sxs-lookup"><span data-stu-id="d5356-117">As the value of this property decreases, the demand on the CPU decreases, but the quality of the output also decreases.</span></span>

<span data-ttu-id="d5356-118">Para o codificador Windows Media áudio 10 Lossless, se o valor dessa propriedade for 0, o codificador colocará uma baixa demanda na CPU.</span><span class="sxs-lookup"><span data-stu-id="d5356-118">For the Windows Media Audio 10 Lossless encoder, if the value of this property is 0, the encoder places a low demand on the CPU.</span></span> <span data-ttu-id="d5356-119">À medida que o valor dessa propriedade aumenta, a demanda da CPU aumenta e o tamanho da saída do codificador diminui ligeiramente.</span><span class="sxs-lookup"><span data-stu-id="d5356-119">As the value of this property increases, the demand on the CPU increases, and the size of the encoder output decreases slightly.</span></span> <span data-ttu-id="d5356-120">A saída é sem perdas, independentemente do valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d5356-120">The output is lossless regardless of the value of this property.</span></span>

<span data-ttu-id="d5356-121">Se você deixar essa propriedade com seu valor padrão de **variante \_ false**, o codificador usará seu algoritmo padrão.</span><span class="sxs-lookup"><span data-stu-id="d5356-121">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder uses its default algorithm.</span></span> <span data-ttu-id="d5356-122">O algoritmo padrão depende de qual codificador você está usando e qual versão do Windows está em execução.</span><span class="sxs-lookup"><span data-stu-id="d5356-122">The default algorithm depends on which encoder you are using and which version of Windows is running.</span></span> <span data-ttu-id="d5356-123">A tabela a seguir descreve o comportamento padrão para as diferentes combinações.</span><span class="sxs-lookup"><span data-stu-id="d5356-123">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="d5356-124">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d5356-124">Operating system</span></span> | <span data-ttu-id="d5356-125">Comportamento padrão</span><span class="sxs-lookup"><span data-stu-id="d5356-125">Default behavior</span></span>                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5356-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5356-126">Windows Vista</span></span>    | <span data-ttu-id="d5356-127">Os codificadores do Windows Media Audio 10, do Windows Media Audio 10 Professional e do Windows Media Audio 10 sem perdas usam o algoritmo mais complexo por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5356-127">The Windows Media Audio 10, Windows Media Audio 10 Professional, and Windows Media Audio 10 Lossless encoders all use the most complex algorithm by default.</span></span>                                                    |
| <span data-ttu-id="d5356-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5356-128">Windows 7</span></span>        | <span data-ttu-id="d5356-129">Os codificadores do Windows Media Audio 10 e do Windows Media Audio 10 Professional usam o algoritmo mais complexo por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5356-129">The Windows Media Audio 10 and Windows Media Audio 10 Professional encoders use the most complex algorithm by default.</span></span> <span data-ttu-id="d5356-130">O codificador do Windows Media Audio 10 sem perdas usa o algoritmo menos complexo por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5356-130">The Windows Media Audio 10 Lossless encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="d5356-131">Se a propriedade [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiver um valor de **Variant \_ false**, o codificador ignorará essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d5356-131">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_FALSE**, the encoder ignores this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5356-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5356-132">Requirements</span></span>



| <span data-ttu-id="d5356-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5356-133">Requirement</span></span> | <span data-ttu-id="d5356-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d5356-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5356-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5356-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d5356-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5356-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d5356-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5356-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d5356-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5356-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5356-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5356-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5356-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5356-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5356-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5356-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5356-142">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5356-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
