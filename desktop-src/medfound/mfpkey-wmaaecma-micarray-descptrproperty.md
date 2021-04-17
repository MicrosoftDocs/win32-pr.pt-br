---
description: Especifica a geometria da matriz do microfone para o DSP de captura de voz.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Propriedade MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813266"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a><span data-ttu-id="736a5-103">\_Propriedade MFPKEY WMAAECMA \_ MICARRAY \_ DESCPTR</span><span class="sxs-lookup"><span data-stu-id="736a5-103">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR Property</span></span>

<span data-ttu-id="736a5-104">Especifica a geometria da matriz do microfone para o DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="736a5-104">Specifies the microphone array geometry for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="736a5-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="736a5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="736a5-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="736a5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="736a5-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="736a5-107">Data Type</span></span>

<span data-ttu-id="736a5-108">\_blob VT</span><span class="sxs-lookup"><span data-stu-id="736a5-108">VT\_BLOB</span></span>

## <a name="applies-to"></a><span data-ttu-id="736a5-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="736a5-109">Applies To</span></span>

-   [<span data-ttu-id="736a5-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="736a5-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="736a5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="736a5-111">Remarks</span></span>

<span data-ttu-id="736a5-112">O valor dessa propriedade é uma estrutura [**de \_ \_ \_ geometria da matriz do MIC KSAUDIO**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) .</span><span class="sxs-lookup"><span data-stu-id="736a5-112">The value of this property is a [**KSAUDIO\_MIC\_ARRAY\_GEOMETRY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) structure.</span></span> <span data-ttu-id="736a5-113">Essa estrutura é definida no arquivo de cabeçalho KsMedia. h.</span><span class="sxs-lookup"><span data-stu-id="736a5-113">This structure is defined in the header file KsMedia.h.</span></span> <span data-ttu-id="736a5-114">Para obter a geometria da matriz do microfone, consulte o dispositivo de áudio para obter a \_ propriedade de geometria da matriz do MIC de áudio KSPROPERTY \_ \_ \_ chamando o método **IKsControl:: KSPROPERTY** no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="736a5-114">To get the microphone array geometry, query the audio device for the KSPROPERTY\_AUDIO\_MIC\_ARRAY\_GEOMETRY property by calling the **IKsControl::KSProperty** method on the device.</span></span> <span data-ttu-id="736a5-115">Para obter mais informações sobre matrizes de microfone, baixe o white paper [como criar e usar matrizes de microfone para o Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span><span class="sxs-lookup"><span data-stu-id="736a5-115">For more information on microphone arrays, download the white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

<span data-ttu-id="736a5-116">Defina essa propriedade se você estiver usando o DSP no modo de filtro e o processamento da matriz de microfone estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="736a5-116">Set this property if you are using the DSP in filter mode and microphone array processing is enabled.</span></span> <span data-ttu-id="736a5-117">Se você estiver usando o DSP no modo de origem, o DSP consultará automaticamente o dispositivo para obter as informações de geometria.</span><span class="sxs-lookup"><span data-stu-id="736a5-117">If you are using the DSP in source mode, the DSP automatically queries the device for the geometry information.</span></span>

## <a name="requirements"></a><span data-ttu-id="736a5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="736a5-118">Requirements</span></span>



| <span data-ttu-id="736a5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="736a5-119">Requirement</span></span> | <span data-ttu-id="736a5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="736a5-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="736a5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="736a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="736a5-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="736a5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="736a5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="736a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="736a5-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="736a5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="736a5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="736a5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="736a5-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="736a5-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="736a5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="736a5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="736a5-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="736a5-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="736a5-129">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="736a5-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
