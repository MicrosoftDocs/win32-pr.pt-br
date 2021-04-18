---
title: Estrutura de _WAVEFORMATEX
description: A estrutura \_WAVEFORMATEX define o formato dos dados de áudio em ondas.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Estrutura de _WAVEFORMATEX Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800186"
---
# <a name="_waveformatex-structure"></a><span data-ttu-id="a30fc-104">\_Estrutura WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="a30fc-104">\_WAVEFORMATEX structure</span></span>

<span data-ttu-id="a30fc-105">A estrutura **\_ WAVEFORMATEX** define o formato dos dados de Wave-Audio.</span><span class="sxs-lookup"><span data-stu-id="a30fc-105">The **\_WAVEFORMATEX** structure defines the format of waveform-audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30fc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a30fc-106">Syntax</span></span>


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a><span data-ttu-id="a30fc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a30fc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a30fc-108">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="a30fc-108">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="a30fc-109">Deve ser definido como um formato ou formatos com suporte pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a30fc-109">Must be set to a format or formats supported by the device.</span></span> <span data-ttu-id="a30fc-110">Observe que as versões anteriores do Windows Media Gerenciador de Dispositivos recomendadas usando \_ o \_ formato \_ de onda WMDM All para indicar suporte a todos os formatos.</span><span class="sxs-lookup"><span data-stu-id="a30fc-110">Note that previous versions of the Windows Media Device Manager recommended using WMDM\_WAVE\_FORMAT\_ALL to indicate support for all formats.</span></span> <span data-ttu-id="a30fc-111">No entanto, isso não é mais recomendado, pois os media players diferentes interpretarão isso de maneiras diferentes, e poucos dispositivos podem realmente reproduzir qualquer formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a30fc-111">However, this is no longer recommended, as different media players will interpret this in different ways, and few devices can truly play any file format.</span></span> <span data-ttu-id="a30fc-112">Agora é recomendável que você use os \_ valores válidos da prop do SqlEnum \_ \_ \_ \_ qualquer valor da enumeração de [**\_ \_ \_ \_ \_ formato de valores válidos de prop do WMDM enum**](wmdm-enum-prop-valid-values-form.md) ou melhor ainda especifique um intervalo de formatos com a estrutura de [**\_ \_ \_ intervalo de valores prop**](wmdm-prop-values-range.md) . do WMDM.</span><span class="sxs-lookup"><span data-stu-id="a30fc-112">It is now recommended that you use the WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY value of the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration, or better yet specify a range of formats with the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a30fc-113">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="a30fc-113">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="a30fc-114">Número de canais nos dados de formato de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="a30fc-114">Number of channels in the waveform-audio data.</span></span> <span data-ttu-id="a30fc-115">Os dados do monaural usam um canal e os dados estéreo usam dois canais.</span><span class="sxs-lookup"><span data-stu-id="a30fc-115">Monaural data uses one channel, and stereo data uses two channels.</span></span>

</dd> <dt>

<span data-ttu-id="a30fc-116">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="a30fc-116">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="a30fc-117">Taxa de amostragem, em amostras por segundo (hertz), em que cada canal deve ser reproduzido ou registrado.</span><span class="sxs-lookup"><span data-stu-id="a30fc-117">Sample rate, in samples per second (Hertz), at which each channel must be played or recorded.</span></span> <span data-ttu-id="a30fc-118">Os valores comuns para **nSamplesPerSec** são 8,0 kilohertz (kHz), 11, 25 khz, 22, 5 khz e 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="a30fc-118">Common values for **nSamplesPerSec** are 8.0 kilohertz (kHz), 11.025 kHz, 22.05 kHz, and 44.1 kHz.</span></span>

</dd> <dt>

<span data-ttu-id="a30fc-119">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="a30fc-119">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="a30fc-120">Taxa média de transferência de dados necessária para a marca de formato, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="a30fc-120">Required average data-transfer rate for the format tag, in bytes per second.</span></span> <span data-ttu-id="a30fc-121">O software de reprodução e de gravação pode estimar tamanhos de buffer usando o membro **nAvgBytesPerSec** .</span><span class="sxs-lookup"><span data-stu-id="a30fc-121">Playback and recording software can estimate buffer sizes by using the **nAvgBytesPerSec** member.</span></span>

</dd> <dt>

<span data-ttu-id="a30fc-122">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="a30fc-122">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="a30fc-123">Alinhamento de bloco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a30fc-123">Block alignment, in bytes.</span></span> <span data-ttu-id="a30fc-124">O alinhamento de bloco é a unidade atômica mínima de dados para o tipo de formato **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="a30fc-124">The block alignment is the minimum atomic unit of data for the **wFormatTag** format type.</span></span> <span data-ttu-id="a30fc-125">O software de reprodução e gravação deve processar vários bytes de **nBlockAlign** de dados por vez.</span><span class="sxs-lookup"><span data-stu-id="a30fc-125">Playback and recording software must process a multiple of **nBlockAlign** bytes of data at a time.</span></span> <span data-ttu-id="a30fc-126">Os dados gravados e lidos de um dispositivo devem sempre ser iniciados no início de um bloco.</span><span class="sxs-lookup"><span data-stu-id="a30fc-126">Data written and read from a device must always start at the beginning of a block.</span></span> <span data-ttu-id="a30fc-127">Por exemplo, não é possível iniciar corretamente a reprodução de dados PCM no meio de um exemplo (ou seja, em um limite que não seja alinhado em bloco).</span><span class="sxs-lookup"><span data-stu-id="a30fc-127">For example, it is not possible to correctly start playing PCM data in the middle of a sample (that is, on a boundary that is not block aligned).</span></span>

</dd> <dt>

<span data-ttu-id="a30fc-128">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="a30fc-128">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="a30fc-129">Bits por amostra para o tipo de formato **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="a30fc-129">Bits per sample for the **wFormatTag** format type.</span></span>

</dd> <dt>

<span data-ttu-id="a30fc-130">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a30fc-130">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a30fc-131">Este membro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a30fc-131">This member is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a30fc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a30fc-132">Requirements</span></span>



| <span data-ttu-id="a30fc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30fc-133">Requirement</span></span> | <span data-ttu-id="a30fc-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a30fc-134">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a30fc-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a30fc-135">Header</span></span><br/> | <dl> <span data-ttu-id="a30fc-136"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a30fc-136"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a30fc-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a30fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30fc-138">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="a30fc-138">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="a30fc-139">**IMDSPStorage:: CreateStorage**</span><span class="sxs-lookup"><span data-stu-id="a30fc-139">**IMDSPStorage::CreateStorage**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[<span data-ttu-id="a30fc-140">**IMDSPStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="a30fc-140">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="a30fc-141">**IWMDMDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="a30fc-141">**IWMDMDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="a30fc-142">**IWMDMOperation:: getobjectattributes**</span><span class="sxs-lookup"><span data-stu-id="a30fc-142">**IWMDMOperation::GetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[<span data-ttu-id="a30fc-143">**IWMDMOperation:: setobjectattributes**</span><span class="sxs-lookup"><span data-stu-id="a30fc-143">**IWMDMOperation::SetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="a30fc-144">**IWMDMStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="a30fc-144">**IWMDMStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="a30fc-145">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="a30fc-145">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





