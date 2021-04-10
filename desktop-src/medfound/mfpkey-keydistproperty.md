---
description: Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: Propriedade MFPKEY_KEYDIST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827906"
---
# <a name="mfpkey_keydist-property"></a><span data-ttu-id="91e1c-103">\_Propriedade MFPKEY KEYdist</span><span class="sxs-lookup"><span data-stu-id="91e1c-103">MFPKEY\_KEYDIST Property</span></span>

<span data-ttu-id="91e1c-104">Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.</span><span class="sxs-lookup"><span data-stu-id="91e1c-104">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="91e1c-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="91e1c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="91e1c-106">g \_ wszWMVCKeyframeDistance</span><span class="sxs-lookup"><span data-stu-id="91e1c-106">g\_wszWMVCKeyframeDistance</span></span>

## <a name="data-type"></a><span data-ttu-id="91e1c-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="91e1c-107">Data Type</span></span>

<span data-ttu-id="91e1c-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="91e1c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="91e1c-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="91e1c-109">Default Value</span></span>

<span data-ttu-id="91e1c-110">O valor padrão depende de qual versão do Windows está em execução, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="91e1c-110">The default value depends on which version of Windows is running, as shown in the following table.</span></span>



| <span data-ttu-id="91e1c-111">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="91e1c-111">Operating system</span></span> | <span data-ttu-id="91e1c-112">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="91e1c-112">Default value</span></span> |
|------------------|---------------|
| <span data-ttu-id="91e1c-113">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91e1c-113">Windows XP</span></span>       | <span data-ttu-id="91e1c-114">8000</span><span class="sxs-lookup"><span data-stu-id="91e1c-114">8000</span></span>          |
| <span data-ttu-id="91e1c-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91e1c-115">Windows Vista</span></span>    | <span data-ttu-id="91e1c-116">8000</span><span class="sxs-lookup"><span data-stu-id="91e1c-116">8000</span></span>          |
| <span data-ttu-id="91e1c-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91e1c-117">Windows 7</span></span>        | <span data-ttu-id="91e1c-118">2000</span><span class="sxs-lookup"><span data-stu-id="91e1c-118">2000</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="91e1c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="91e1c-119">Remarks</span></span>

<span data-ttu-id="91e1c-120">A lógica interna do codec determina o local real de cada quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="91e1c-120">The internal logic of the codec determines the actual location of each key frame.</span></span> <span data-ttu-id="91e1c-121">A distância entre dois quadros-chave pode ser menor que o valor dessa propriedade, no entanto, ela nunca será maior.</span><span class="sxs-lookup"><span data-stu-id="91e1c-121">The distance between any two key frames may be less than the value of this property, however, it will never be greater.</span></span>

## <a name="requirements"></a><span data-ttu-id="91e1c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91e1c-122">Requirements</span></span>



| <span data-ttu-id="91e1c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="91e1c-123">Requirement</span></span> | <span data-ttu-id="91e1c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="91e1c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91e1c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e1c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="91e1c-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="91e1c-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="91e1c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e1c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="91e1c-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91e1c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91e1c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91e1c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="91e1c-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="91e1c-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91e1c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="91e1c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e1c-132">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91e1c-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




