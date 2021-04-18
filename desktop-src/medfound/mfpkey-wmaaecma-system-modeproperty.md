---
description: Define o modo de processamento para o DSP de captura de voz.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Propriedade MFPKEY_WMAAECMA_SYSTEM_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764716"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a><span data-ttu-id="60ba1-103">\_Propriedade do \_ modo do sistema MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="60ba1-103">MFPKEY\_WMAAECMA\_SYSTEM\_MODE Property</span></span>

<span data-ttu-id="60ba1-104">Define o modo de processamento para o DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="60ba1-104">Sets the processing mode for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="60ba1-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="60ba1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="60ba1-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="60ba1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="60ba1-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="60ba1-107">Data Type</span></span>

<span data-ttu-id="60ba1-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="60ba1-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="60ba1-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="60ba1-109">Applies To</span></span>

-   [<span data-ttu-id="60ba1-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="60ba1-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="60ba1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="60ba1-111">Remarks</span></span>

<span data-ttu-id="60ba1-112">O valor dessa propriedade é um membro da enumeração do [ \_ \_ modo do sistema AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .</span><span class="sxs-lookup"><span data-stu-id="60ba1-112">The value of this property is a member of the [AEC\_SYSTEM\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) enumeration.</span></span>

<span data-ttu-id="60ba1-113">A propriedade deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="60ba1-113">The property must be one of the following values.</span></span>



| <span data-ttu-id="60ba1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="60ba1-114">Value</span></span> | <span data-ttu-id="60ba1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="60ba1-115">Description</span></span>                                 |
|-------|---------------------------------------------|
| <span data-ttu-id="60ba1-116">0</span><span class="sxs-lookup"><span data-stu-id="60ba1-116">0</span></span>     | <span data-ttu-id="60ba1-117">Modo somente do AEC (cancelamento de eco de áudio)</span><span class="sxs-lookup"><span data-stu-id="60ba1-117">Audio echo cancellation (AEC) only mode</span></span>     |
| <span data-ttu-id="60ba1-118">2</span><span class="sxs-lookup"><span data-stu-id="60ba1-118">2</span></span>     | <span data-ttu-id="60ba1-119">Modo somente de processamento de matriz de microfone (MAP)</span><span class="sxs-lookup"><span data-stu-id="60ba1-119">Microphone array processing (MAP) only mode</span></span> |
| <span data-ttu-id="60ba1-120">4</span><span class="sxs-lookup"><span data-stu-id="60ba1-120">4</span></span>     | <span data-ttu-id="60ba1-121">AEC e modo de mapa</span><span class="sxs-lookup"><span data-stu-id="60ba1-121">AEC and MAP mode</span></span>                            |
| <span data-ttu-id="60ba1-122">5</span><span class="sxs-lookup"><span data-stu-id="60ba1-122">5</span></span>     | <span data-ttu-id="60ba1-123">Nenhum AEC nem modo de mapa</span><span class="sxs-lookup"><span data-stu-id="60ba1-123">Neither AEC nor MAP mode</span></span>                    |



 

<span data-ttu-id="60ba1-124">Você deve definir essa propriedade antes de usar o DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="60ba1-124">You must set this property before using the Voice Capture DSP.</span></span> <span data-ttu-id="60ba1-125">Depois de definir essa propriedade, você pode usar o DSP com suas configurações padrão ou definir propriedades adicionais.</span><span class="sxs-lookup"><span data-stu-id="60ba1-125">After you set this property, you can use the DSP with its default settings, or set additional properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ba1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60ba1-126">Requirements</span></span>



| <span data-ttu-id="60ba1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ba1-127">Requirement</span></span> | <span data-ttu-id="60ba1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="60ba1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60ba1-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ba1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="60ba1-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60ba1-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="60ba1-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ba1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="60ba1-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60ba1-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60ba1-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60ba1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="60ba1-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ba1-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ba1-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="60ba1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ba1-136">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60ba1-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="60ba1-137">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="60ba1-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
