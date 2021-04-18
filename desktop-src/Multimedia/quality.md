---
title: comando de qualidade
description: O comando de qualidade define um nível de qualidade personalizado para a compactação de dados de áudio, vídeo ou ainda de imagem. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- Multimídia do Windows de comando de qualidade
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753433"
---
# <a name="quality-command"></a><span data-ttu-id="8d234-105">comando de qualidade</span><span class="sxs-lookup"><span data-stu-id="8d234-105">quality command</span></span>

<span data-ttu-id="8d234-106">O comando de qualidade define um nível de qualidade personalizado para a compactação de dados de áudio, vídeo ou ainda de imagem.</span><span class="sxs-lookup"><span data-stu-id="8d234-106">The quality command defines a custom quality level for either audio, video or still image data compression.</span></span> <span data-ttu-id="8d234-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="8d234-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8d234-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8d234-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8d234-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d234-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d234-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8d234-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8d234-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="8d234-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8d234-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="8d234-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8d234-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span><span class="sxs-lookup"><span data-stu-id="8d234-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span></span>
</dt> <dd>

<span data-ttu-id="8d234-114">Um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8d234-114">One or more of the following flags.</span></span> <span data-ttu-id="8d234-115">(Um dos três sinalizadores "áudio", "ainda" e "vídeo" deve estar presente.)</span><span class="sxs-lookup"><span data-stu-id="8d234-115">(One of the three flags "audio", "still", and "video" must be present.)</span></span>



| <span data-ttu-id="8d234-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8d234-116">Value</span></span>                 | <span data-ttu-id="8d234-117">Significado</span><span class="sxs-lookup"><span data-stu-id="8d234-117">Meaning</span></span>                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d234-118">*algoritmo* de algoritmo</span><span class="sxs-lookup"><span data-stu-id="8d234-118">algorithm *algorithm*</span></span> | <span data-ttu-id="8d234-119">Associa o nível de qualidade ao *algoritmo* especificado.</span><span class="sxs-lookup"><span data-stu-id="8d234-119">Associates the quality level with the specified *algorithm*.</span></span> <span data-ttu-id="8d234-120">Esse *algoritmo* deve ser suportado pelo dispositivo e ser compatível com o sinalizador "áudio", "ainda" ou "vídeo" que é usado.</span><span class="sxs-lookup"><span data-stu-id="8d234-120">This *algorithm* must be supported by the device and be compatible with the "audio", "still", or "video" flag that is used.</span></span> <span data-ttu-id="8d234-121">Se omitido, o algoritmo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="8d234-121">If omitted, the current algorithm is used.</span></span> |
| <span data-ttu-id="8d234-122">*nome* do áudio</span><span class="sxs-lookup"><span data-stu-id="8d234-122">audio *name*</span></span>          | <span data-ttu-id="8d234-123">Indica que este comando especifica um nível de qualidade de "áudio" identificado com o *nome*.</span><span class="sxs-lookup"><span data-stu-id="8d234-123">Indicates this command specifies an "audio" quality level identified with *name*.</span></span>                                                                                                                                                   |
| <span data-ttu-id="8d234-124">diálogo</span><span class="sxs-lookup"><span data-stu-id="8d234-124">dialog</span></span>                | <span data-ttu-id="8d234-125">Solicita que o dispositivo exiba uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8d234-125">Requests that the device display a dialog box.</span></span> <span data-ttu-id="8d234-126">Essa caixa de diálogo tem campos específicos de algoritmo que são usados internamente pelo dispositivo para criar a estrutura que descreve um nível de qualidade específico.</span><span class="sxs-lookup"><span data-stu-id="8d234-126">This dialog box has algorithm-specific fields that are used internally by the device to create the structure describing a specific quality level.</span></span>                                    |
| <span data-ttu-id="8d234-127">*identificador* de identificador</span><span class="sxs-lookup"><span data-stu-id="8d234-127">handle *handle*</span></span>       | <span data-ttu-id="8d234-128">Especifica um *identificador* para uma estrutura que contém dados específicos de algoritmos que descrevem um nível de qualidade específico.</span><span class="sxs-lookup"><span data-stu-id="8d234-128">Specifies a *handle* to a structure that contains algorithmic-specific data describing a specific quality level.</span></span> <span data-ttu-id="8d234-129">As estruturas para os dados referenciados por esse identificador são específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d234-129">The structures for the data referenced by this handle are device specific.</span></span>                                         |
| <span data-ttu-id="8d234-130">*nome* ainda</span><span class="sxs-lookup"><span data-stu-id="8d234-130">still *name*</span></span>          | <span data-ttu-id="8d234-131">Indica que o comando especifica um nível de qualidade "ainda" identificado com o *nome.*</span><span class="sxs-lookup"><span data-stu-id="8d234-131">Indicates the command specifies a "still" quality level identified with *name.*</span></span>                                                                                                                                                     |
| <span data-ttu-id="8d234-132">*nome* do vídeo</span><span class="sxs-lookup"><span data-stu-id="8d234-132">video *name*</span></span>          | <span data-ttu-id="8d234-133">Indica que o comando especifica um nível de qualidade de "vídeo" identificado com o *nome*.</span><span class="sxs-lookup"><span data-stu-id="8d234-133">Indicates the command specifies a "video" quality level identified with *name*.</span></span>                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="8d234-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="8d234-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8d234-135">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="8d234-135">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="8d234-136">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8d234-136">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d234-137">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8d234-137">Return Value</span></span>

<span data-ttu-id="8d234-138">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="8d234-138">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d234-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d234-139">Remarks</span></span>

<span data-ttu-id="8d234-140">Este comando define um nome de cadeia de caracteres para o nível de qualidade, que pode ser usado em um comando [setvideo](setvideo.md) "qualidade", setvideo "qualidade [" ou "](setaudio.md) qualidade" para estabelecer o nível de qualidade do vídeo atual, ainda ou de compactação de áudio.</span><span class="sxs-lookup"><span data-stu-id="8d234-140">This command defines a string name for the quality level, which can then be used in a [setvideo](setvideo.md) "quality", setvideo "still quality", or [setaudio](setaudio.md) "quality" command to establish it as the current video, still, or audio-compression quality level.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d234-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d234-141">Requirements</span></span>



| <span data-ttu-id="8d234-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d234-142">Requirement</span></span> | <span data-ttu-id="8d234-143">Valor</span><span class="sxs-lookup"><span data-stu-id="8d234-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8d234-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d234-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8d234-145">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d234-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d234-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d234-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8d234-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d234-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8d234-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d234-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d234-149">MCI</span><span class="sxs-lookup"><span data-stu-id="8d234-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8d234-150">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="8d234-150">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="8d234-151">SetAudio</span><span class="sxs-lookup"><span data-stu-id="8d234-151">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="8d234-152">setvideo</span><span class="sxs-lookup"><span data-stu-id="8d234-152">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

