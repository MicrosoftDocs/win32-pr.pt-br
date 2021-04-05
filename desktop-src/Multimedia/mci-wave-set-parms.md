---
title: Estrutura de MCI_WAVE_SET_PARMS (Mciapi. h)
description: A \_ estrutura de \_ \_ parâmetros Set parms do MCI contém informações para o \_ comando set do MCI para dispositivos de forma de onda-áudio.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- Multimídia do Windows da estrutura de MCI_WAVE_SET_PARMS
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824735"
---
# <a name="mci_wave_set_parms-structure"></a><span data-ttu-id="301e3-104">\_Estrutura de \_ parâmetros do conjunto de ondas MCI \_</span><span class="sxs-lookup"><span data-stu-id="301e3-104">MCI\_WAVE\_SET\_PARMS structure</span></span>

<span data-ttu-id="301e3-105">A estrutura de **\_ \_ \_ parâmetros Set parms do MCI** contém informações para o comando [**\_ set do MCI**](mci-set.md) para dispositivos de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="301e3-105">The **MCI\_WAVE\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="301e3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="301e3-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="301e3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="301e3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="301e3-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="301e3-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="301e3-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="301e3-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-111">Formato de hora do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="301e3-111">Device's time format.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="301e3-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-113">Número de canal para saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="301e3-113">Channel number for audio output.</span></span> <span data-ttu-id="301e3-114">Normalmente usado ao ativar ou desativar um canal.</span><span class="sxs-lookup"><span data-stu-id="301e3-114">Typically used when turning a channel on or off.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-115">**wInput**</span><span class="sxs-lookup"><span data-stu-id="301e3-115">**wInput**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-116">Canal de entrada de áudio.</span><span class="sxs-lookup"><span data-stu-id="301e3-116">Audio input channel.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-117">**wOutput**</span><span class="sxs-lookup"><span data-stu-id="301e3-117">**wOutput**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-118">Dispositivo de saída a ser usado.</span><span class="sxs-lookup"><span data-stu-id="301e3-118">Output device to use.</span></span> <span data-ttu-id="301e3-119">Por exemplo, esse valor poderia ser 2 se um sistema tiver duas placas de som instaladas.</span><span class="sxs-lookup"><span data-stu-id="301e3-119">For example, this value could be 2 if a system had two installed sound cards.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-120">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="301e3-120">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-121">Formato dos dados de wave-áudio, como PCM de \_ formato Wave \_ .</span><span class="sxs-lookup"><span data-stu-id="301e3-121">Format of the waveform-audio data, such as WAVE\_FORMAT\_PCM.</span></span> <span data-ttu-id="301e3-122">Os valores possíveis são definidos em Mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="301e3-122">Possible values are defined in Mmreg.h.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-123">**wReserved2**</span><span class="sxs-lookup"><span data-stu-id="301e3-123">**wReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="301e3-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-125">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="301e3-125">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-126">Mono (1) ou estéreo (2).</span><span class="sxs-lookup"><span data-stu-id="301e3-126">Mono (1) or stereo (2).</span></span>

</dd> <dt>

<span data-ttu-id="301e3-127">**wReserved3**</span><span class="sxs-lookup"><span data-stu-id="301e3-127">**wReserved3**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="301e3-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-129">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="301e3-129">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-130">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="301e3-130">Samples per second.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-131">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="301e3-131">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-132">Taxa de amostragem em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="301e3-132">Sample rate in bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-133">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="301e3-133">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-134">Bloquear o alinhamento dos dados.</span><span class="sxs-lookup"><span data-stu-id="301e3-134">Block alignment of the data.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-135">**wReserved4**</span><span class="sxs-lookup"><span data-stu-id="301e3-135">**wReserved4**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-136">Reservado.</span><span class="sxs-lookup"><span data-stu-id="301e3-136">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-137">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="301e3-137">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-138">Bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="301e3-138">Bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="301e3-139">**wReserved5**</span><span class="sxs-lookup"><span data-stu-id="301e3-139">**wReserved5**</span></span>
</dt> <dd>

<span data-ttu-id="301e3-140">Reservado.</span><span class="sxs-lookup"><span data-stu-id="301e3-140">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="301e3-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="301e3-141">Remarks</span></span>

<span data-ttu-id="301e3-142">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="301e3-142">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="301e3-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="301e3-143">Requirements</span></span>



| <span data-ttu-id="301e3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="301e3-144">Requirement</span></span> | <span data-ttu-id="301e3-145">Valor</span><span class="sxs-lookup"><span data-stu-id="301e3-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="301e3-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="301e3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="301e3-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="301e3-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="301e3-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="301e3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="301e3-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="301e3-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="301e3-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="301e3-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="301e3-151"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="301e3-151"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="301e3-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="301e3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301e3-153">**MCI**</span><span class="sxs-lookup"><span data-stu-id="301e3-153">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="301e3-154">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="301e3-154">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="301e3-155">**conjunto de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="301e3-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="301e3-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="301e3-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

