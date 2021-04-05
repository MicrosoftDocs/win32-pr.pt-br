---
description: Especifica quais dispositivos de áudio o DSP de captura de voz usa para capturar e renderizar áudio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Propriedade MFPKEY_WMAAECMA_DEVICE_INDEXES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827549"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a><span data-ttu-id="d92ae-103">\_Propriedade de \_ índices de dispositivo MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="d92ae-103">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES Property</span></span>

<span data-ttu-id="d92ae-104">Especifica quais dispositivos de áudio o DSP de captura de voz usa para capturar e renderizar áudio.</span><span class="sxs-lookup"><span data-stu-id="d92ae-104">Specifies which audio devices the Voice Capture DSP uses for capturing and rendering audio.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d92ae-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d92ae-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d92ae-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d92ae-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d92ae-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d92ae-107">Data Type</span></span>

<span data-ttu-id="d92ae-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="d92ae-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d92ae-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d92ae-109">Default Value</span></span>

<span data-ttu-id="d92ae-110">(-1,-1).</span><span class="sxs-lookup"><span data-stu-id="d92ae-110">(-1, -1).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d92ae-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="d92ae-111">Applies To</span></span>

-   [<span data-ttu-id="d92ae-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="d92ae-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="d92ae-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d92ae-113">Remarks</span></span>

<span data-ttu-id="d92ae-114">Defina essa propriedade se você estiver usando o DSP no modo de origem.</span><span class="sxs-lookup"><span data-stu-id="d92ae-114">Set this property if you are using the DSP in source mode.</span></span> <span data-ttu-id="d92ae-115">O DSP ignora essa propriedade no modo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d92ae-115">The DSP ignores this property in filter mode.</span></span>

<span data-ttu-id="d92ae-116">O valor da propriedade é a **palavra** de 2 16 bits s empacotada em um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="d92ae-116">The value of the property is two 16-bit **WORD** s packed into a **DWORD**.</span></span> <span data-ttu-id="d92ae-117">Os 16 bits superiores especificam o dispositivo de renderização de áudio (normalmente um palestrante) e os 16 bits inferiores especificam o dispositivo de captura (normalmente um microfone).</span><span class="sxs-lookup"><span data-stu-id="d92ae-117">The upper 16 bits specify the audio rendering device (typically a speaker), and the lower 16 bits specify the capture device (typically a microphone).</span></span> <span data-ttu-id="d92ae-118">Cada dispositivo é especificado como um índice na coleção de dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="d92ae-118">Each device is specified as an index into the audio device collection.</span></span> <span data-ttu-id="d92ae-119">Se o índice for-1, o dispositivo padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="d92ae-119">If the index is -1, the default device is used.</span></span>

<span data-ttu-id="d92ae-120">O índice do dispositivo corresponde ao índice da coleção usado na interface [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) .</span><span class="sxs-lookup"><span data-stu-id="d92ae-120">The device index corresponds to the collection index used in the [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) interface.</span></span> <span data-ttu-id="d92ae-121">O aplicativo deve reproduzir a voz de extremidade final por meio do dispositivo de renderização selecionado.</span><span class="sxs-lookup"><span data-stu-id="d92ae-121">The application must play the far-end voice through the selected rendering device.</span></span> <span data-ttu-id="d92ae-122">(A voz de ponta é a voz da pessoa na outra extremidade da linha telefônica, que é reproduzida pelo orador no computador do usuário.) Se o dispositivo de renderização selecionado não tiver um fluxo ativo, o DSP não poderá processar nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d92ae-122">(The far-end voice is the voice of the person on the other end of the telephone line, which is played through the speaker on the user's computer.) If the selected rendering device does not have an active stream, the DSP cannot process any output.</span></span>

<span data-ttu-id="d92ae-123">O valor padrão dessa propriedade é (-1,-1).</span><span class="sxs-lookup"><span data-stu-id="d92ae-123">The default value of this property is (-1, -1).</span></span>

<span data-ttu-id="d92ae-124">O exemplo a seguir mostra como inicializar o **PROPVARIANT** para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d92ae-124">The following example shows how to initialize the **PROPVARIANT** for this property.</span></span>


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a><span data-ttu-id="d92ae-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d92ae-125">Requirements</span></span>



| <span data-ttu-id="d92ae-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d92ae-126">Requirement</span></span> | <span data-ttu-id="d92ae-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d92ae-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d92ae-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d92ae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d92ae-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d92ae-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d92ae-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d92ae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d92ae-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d92ae-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d92ae-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d92ae-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d92ae-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d92ae-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d92ae-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d92ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92ae-135">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d92ae-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d92ae-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="d92ae-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
