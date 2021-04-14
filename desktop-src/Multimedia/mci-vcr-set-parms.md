---
title: Estrutura de MCI_VCR_SET_PARMS (VCR. h)
description: A \_ estrutura do VCR do conjunto de videocassetes do MCI \_ \_ contém parâmetros para o \_ comando set do MCI para gravadores de vídeo-fita.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SET_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369856"
---
# <a name="mci_vcr_set_parms-structure"></a><span data-ttu-id="9a4bc-104">\_Estrutura de \_ parâmetros de conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="9a4bc-104">MCI\_VCR\_SET\_PARMS structure</span></span>

<span data-ttu-id="9a4bc-105">A estrutura do **\_ VCR do \_ conjunto \_ de videocassetes do MCI** contém parâmetros para o comando [**\_ set do MCI**](mci-set.md) para gravadores de vídeo-fita.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-105">The **MCI\_VCR\_SET\_PARMS** structure contains parameters for the [**MCI\_SET**](mci-set.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a4bc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a4bc-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="9a4bc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9a4bc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a4bc-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-111">Formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-111">Current time format.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-114">**dwTimeMode**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-114">**dwTimeMode**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-115">Constante que especifica a fonte de tempo usada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-115">Constant that specifies the timing source used by the device.</span></span> <span data-ttu-id="9a4bc-116">A origem de temporização é um código de tempo registrado em fita de vídeo ou os contadores no dispositivo que detectam a movimentação da fita.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-116">The timing source is either a timecode recorded on videotape, or the counters in the device that sense videotape movement.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-117">**dwRecordFormat**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-117">**dwRecordFormat**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-118">Taxa de gravação.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-118">Recording rate.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-119">**dwCounterFormat**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-119">**dwCounterFormat**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-120">Formato de um novo valor de hora do contador.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-120">Format of a new counter time value.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-121">**dwIndex**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-121">**dwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-122">Conteúdo da exibição na tela.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-122">Contents of on-screen display.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-123">**dwTracking**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-123">**dwTracking**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-124">Ajuste de velocidade usado ao acompanhar a taxa de reprodução de VCR.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-124">Speed adjustment used when tracking the VCR playback rate.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-125">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-125">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-126">Velocidade de reprodução usada pelo dispositivo como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-126">Playback speed used by the device as an integer.</span></span> <span data-ttu-id="9a4bc-127">A velocidade de reprodução normal é 1000, a velocidade dupla é 2000 e a meia velocidade é 500.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-127">Normal playback speed is 1000, double speed is 2000, and half speed is 500.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-128">**dwLength**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-128">**dwLength**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-129">Tamanho da fita quando o comprimento não puder ser detectado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-129">Videotape length when the length is undetectable by the device.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-130">**dwCounter**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-130">**dwCounter**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-131">Novo valor do contador.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-131">New counter value.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-132">**dwClock**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-132">**dwClock**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-133">Nova hora do relógio.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-133">New clock time.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-134">**dwPauseTimeout**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-134">**dwPauseTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-135">Novo valor de tempo limite para o comando de pausa.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-135">New timeout value for pause command.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-136">**dwPrerollDuration**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-136">**dwPrerollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-137">Tamanho da fita de vídeo necessário para estabilizar a saída do VCR.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-137">Videotape length needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="9a4bc-138">**dwPostrollDuration**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-138">**dwPostrollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="9a4bc-139">Tamanho da fita de vídeo necessário para [**\_ finalizar**](mci-stop.md) o transporte de videocassete quando um comando Stop MCI ou [**MCI \_ Pause**](mci-pause.md) é emitido.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-139">Videotape length needed to brake the VCR transport when a [**MCI\_STOP**](mci-stop.md) or [**MCI\_PAUSE**](mci-pause.md) command is issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a4bc-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a4bc-140">Remarks</span></span>

<span data-ttu-id="9a4bc-141">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="9a4bc-141">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a4bc-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a4bc-142">Requirements</span></span>



| <span data-ttu-id="9a4bc-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a4bc-143">Requirement</span></span> | <span data-ttu-id="9a4bc-144">Valor</span><span class="sxs-lookup"><span data-stu-id="9a4bc-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9a4bc-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a4bc-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9a4bc-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a4bc-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9a4bc-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a4bc-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9a4bc-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a4bc-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9a4bc-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9a4bc-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a4bc-150"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a4bc-150"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a4bc-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a4bc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a4bc-152">**MCI**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-152">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9a4bc-153">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-153">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="9a4bc-154">**pausa de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-154">**MCI\_PAUSE**</span></span>](mci-pause.md)
</dt> <dt>

[<span data-ttu-id="9a4bc-155">**conjunto de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="9a4bc-156">**parada do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="9a4bc-156">**MCI\_STOP**</span></span>](mci-stop.md)
</dt> <dt>

<span data-ttu-id="9a4bc-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a4bc-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

