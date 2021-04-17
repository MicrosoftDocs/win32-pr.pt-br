---
description: Especifica se a complexidade do algoritmo de codificação de áudio está restrita.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: Propriedade MFPKEY_CONSTRAINENCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797554"
---
# <a name="mfpkey_constrainencomplexity-property"></a><span data-ttu-id="66e26-103">\_Propriedade MFPKEY CONSTRAINENCOMPLEXITY</span><span class="sxs-lookup"><span data-stu-id="66e26-103">MFPKEY\_CONSTRAINENCOMPLEXITY Property</span></span>

<span data-ttu-id="66e26-104">Especifica se a complexidade do algoritmo de codificação de áudio está restrita.</span><span class="sxs-lookup"><span data-stu-id="66e26-104">Specifies whether the complexity of the audio encoding algorithm is constrained.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="66e26-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="66e26-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="66e26-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="66e26-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="66e26-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="66e26-107">Data Type</span></span>

<span data-ttu-id="66e26-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="66e26-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="66e26-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="66e26-109">Default Value</span></span>

<span data-ttu-id="66e26-110">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="66e26-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="66e26-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="66e26-111">Remarks</span></span>

<span data-ttu-id="66e26-112">Se você deixar essa propriedade com seu valor padrão de **variante \_ false**, o codificador de áudio usará seu algoritmo padrão.</span><span class="sxs-lookup"><span data-stu-id="66e26-112">If you leave this property at its default value of **VARIANT\_FALSE**, the audio encoder uses its default algorithm.</span></span> <span data-ttu-id="66e26-113">O algoritmo padrão depende do tipo de saída e da versão do Windows em execução.</span><span class="sxs-lookup"><span data-stu-id="66e26-113">The default algorithm depends on the output type and which version of Windows is running.</span></span> <span data-ttu-id="66e26-114">A tabela a seguir descreve o comportamento padrão para as diferentes combinações.</span><span class="sxs-lookup"><span data-stu-id="66e26-114">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="66e26-115">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="66e26-115">Operating system</span></span> | <span data-ttu-id="66e26-116">Comportamento padrão</span><span class="sxs-lookup"><span data-stu-id="66e26-116">Default behavior</span></span>                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e26-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66e26-117">Windows Vista</span></span>    | <span data-ttu-id="66e26-118">Para todos os tipos de saída, o codificador de áudio usa o algoritmo mais complexo por padrão.</span><span class="sxs-lookup"><span data-stu-id="66e26-118">For all output types, the audio encoder uses the most complex algorithm by default.</span></span>                                                                                                                 |
| <span data-ttu-id="66e26-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66e26-119">Windows 7</span></span>        | <span data-ttu-id="66e26-120">Para tipos de saída standard e Professional, o codificador de áudio usa o algoritmo mais complexo por padrão.</span><span class="sxs-lookup"><span data-stu-id="66e26-120">For Standard and Professional output types, the audio encoder uses the most complex algorithm by default.</span></span> <span data-ttu-id="66e26-121">Para tipos de saída sem perdas, o codificador de áudio usa o algoritmo menos complexo por padrão.</span><span class="sxs-lookup"><span data-stu-id="66e26-121">For Lossless output types, the audio encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="66e26-122">Se você definir essa propriedade como **Variant \_ true**, também deverá especificar um valor de complexidade definindo a propriedade [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="66e26-122">If you set this property to **VARIANT\_TRUE**, you must also specify a complexity value by setting the [**MFPKEY\_ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e26-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66e26-123">Requirements</span></span>



| <span data-ttu-id="66e26-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="66e26-124">Requirement</span></span> | <span data-ttu-id="66e26-125">Valor</span><span class="sxs-lookup"><span data-stu-id="66e26-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66e26-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66e26-126">Minimum supported client</span></span><br/> | <span data-ttu-id="66e26-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66e26-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="66e26-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66e26-128">Minimum supported server</span></span><br/> | <span data-ttu-id="66e26-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66e26-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66e26-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66e26-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e26-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="66e26-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e26-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="66e26-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e26-133">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66e26-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
