---
title: comando Where
description: O comando Where recupera o retângulo especificando a área de origem ou de destino. Esse retângulo foi especificado usando o comando put. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- como multimídia do Windows de comando
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919007"
---
# <a name="where-command"></a><span data-ttu-id="96265-106">comando Where</span><span class="sxs-lookup"><span data-stu-id="96265-106">where command</span></span>

<span data-ttu-id="96265-107">O comando Where recupera o retângulo especificando a área de origem ou de destino.</span><span class="sxs-lookup"><span data-stu-id="96265-107">The where command retrieves the rectangle specifying the source or destination area.</span></span> <span data-ttu-id="96265-108">Esse retângulo foi especificado usando o comando [Put](put.md) .</span><span class="sxs-lookup"><span data-stu-id="96265-108">This rectangle was specified using the [put](put.md) command.</span></span> <span data-ttu-id="96265-109">Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="96265-109">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="96265-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="96265-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="96265-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96265-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96265-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="96265-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="96265-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="96265-113">Identifier of an MCI device.</span></span> <span data-ttu-id="96265-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="96265-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="96265-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span><span class="sxs-lookup"><span data-stu-id="96265-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span></span>
</dt> <dd>

<span data-ttu-id="96265-116">Sinalizador que identifica o retângulo cujas dimensões são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="96265-116">Flag that identifies the rectangle whose dimensions are retrieved.</span></span> <span data-ttu-id="96265-117">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Where** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="96265-117">The following table lists device types that recognize the **where** command and the flags used by each type.</span></span>



| <span data-ttu-id="96265-118">Valor</span><span class="sxs-lookup"><span data-stu-id="96265-118">Value</span></span>        | <span data-ttu-id="96265-119">Significado</span><span class="sxs-lookup"><span data-stu-id="96265-119">Meaning</span></span>                                                       | <span data-ttu-id="96265-120">Significado</span><span class="sxs-lookup"><span data-stu-id="96265-120">Meaning</span></span>                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="96265-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="96265-121">digitalvideo</span></span> | <span data-ttu-id="96265-122">destinationdestination [**Max**](max.md)frameFrame maxsource</span><span class="sxs-lookup"><span data-stu-id="96265-122">destinationdestination [**max**](max.md)frameframe maxsource</span></span> | <span data-ttu-id="96265-123">maxvideovideo de origem maxwindowwindow Max</span><span class="sxs-lookup"><span data-stu-id="96265-123">source maxvideovideo maxwindowwindow max</span></span> |
| <span data-ttu-id="96265-124">overlay</span><span class="sxs-lookup"><span data-stu-id="96265-124">overlay</span></span>      | <span data-ttu-id="96265-125">destinationframe</span><span class="sxs-lookup"><span data-stu-id="96265-125">destinationframe</span></span>                                              | <span data-ttu-id="96265-126">sourcevideo</span><span class="sxs-lookup"><span data-stu-id="96265-126">sourcevideo</span></span>                              |



 

<span data-ttu-id="96265-127">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRequestRect** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="96265-127">The following table lists the flags that can be specified in the **lpszRequestRect** parameter and their meanings.</span></span>



| <span data-ttu-id="96265-128">Valor</span><span class="sxs-lookup"><span data-stu-id="96265-128">Value</span></span>                          | <span data-ttu-id="96265-129">Significado</span><span class="sxs-lookup"><span data-stu-id="96265-129">Meaning</span></span>                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96265-130">destino</span><span class="sxs-lookup"><span data-stu-id="96265-130">destination</span></span>                    | <span data-ttu-id="96265-131">Recupera a extensão e o deslocamento de destino.</span><span class="sxs-lookup"><span data-stu-id="96265-131">Retrieves the destination offset and extent.</span></span> <span data-ttu-id="96265-132">Para dispositivos de sobreposição de vídeo, o retângulo de destino define a área da área do cliente da janela de exibição que exibe os dados da imagem do buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="96265-132">For video-overlay devices, the destination rectangle defines the area of the display window client area that displays the image data from the frame buffer.</span></span>                                                                                             |
| <span data-ttu-id="96265-133">[ **máximo** de destino](max.md)</span><span class="sxs-lookup"><span data-stu-id="96265-133">destination [**max**](max.md)</span></span> | <span data-ttu-id="96265-134">Recupera o tamanho atual do retângulo do cliente.</span><span class="sxs-lookup"><span data-stu-id="96265-134">Retrieves the current size of the client rectangle.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="96265-135">frame</span><span class="sxs-lookup"><span data-stu-id="96265-135">frame</span></span>                          | <span data-ttu-id="96265-136">Recupera o deslocamento e a extensão do retângulo do buffer do quadro.</span><span class="sxs-lookup"><span data-stu-id="96265-136">Retrieves the offset and extent of the frame buffer rectangle.</span></span> <span data-ttu-id="96265-137">O retângulo do buffer de quadro define a área do buffer de quadro que recebe dados de vídeo recebidos.</span><span class="sxs-lookup"><span data-stu-id="96265-137">The frame buffer rectangle defines the area of the frame buffer that receives incoming video data.</span></span> <span data-ttu-id="96265-138">As imagens do retângulo "vídeo" são dimensionadas para essa região.</span><span class="sxs-lookup"><span data-stu-id="96265-138">Images from the "video" rectangle are scaled into this region.</span></span>                                                                     |
| <span data-ttu-id="96265-139">[ **máximo** do quadro](max.md)</span><span class="sxs-lookup"><span data-stu-id="96265-139">frame [**max**](max.md)</span></span>       | <span data-ttu-id="96265-140">Retorna o tamanho máximo do buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="96265-140">Returns the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="96265-141">source</span><span class="sxs-lookup"><span data-stu-id="96265-141">source</span></span>                         | <span data-ttu-id="96265-142">Recupera o deslocamento e a extensão da origem.</span><span class="sxs-lookup"><span data-stu-id="96265-142">Retrieves the source offset and extent.</span></span> <span data-ttu-id="96265-143">Para dispositivos de sobreposição de vídeo, o retângulo de origem define a região do buffer de quadro que é exibido na janela de destino.</span><span class="sxs-lookup"><span data-stu-id="96265-143">For video-overlay devices, the source rectangle defines the region of the frame buffer that is displayed in the destination window.</span></span> <span data-ttu-id="96265-144">O dispositivo usa esse retângulo para cortar a imagem antes que ela seja ampliada para se ajustar ao retângulo de destino na exibição.</span><span class="sxs-lookup"><span data-stu-id="96265-144">The device uses this rectangle to crop the image before it is stretched to fit the destination rectangle on the display.</span></span> |
| <span data-ttu-id="96265-145">fonte [ **máxima**](max.md)</span><span class="sxs-lookup"><span data-stu-id="96265-145">source [**max**](max.md)</span></span>      | <span data-ttu-id="96265-146">Recupera o tamanho máximo do buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="96265-146">Retrieves the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="96265-147">video</span><span class="sxs-lookup"><span data-stu-id="96265-147">video</span></span>                          | <span data-ttu-id="96265-148">Recupera o deslocamento e a extensão do retângulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="96265-148">Retrieves the offset and extent of the video rectangle.</span></span> <span data-ttu-id="96265-149">O retângulo de vídeo define a região dos dados de vídeo de entrada que são transferidos para o buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="96265-149">The video rectangle defines the region of the incoming video data that is transferred to the frame buffer.</span></span>                                                                                                                                   |
| <span data-ttu-id="96265-150">[ **máximo** de vídeo](max.md)</span><span class="sxs-lookup"><span data-stu-id="96265-150">video [**max**](max.md)</span></span>       | <span data-ttu-id="96265-151">Retorna o tamanho máximo da entrada.</span><span class="sxs-lookup"><span data-stu-id="96265-151">Returns the maximum size of the input.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="96265-152">janela</span><span class="sxs-lookup"><span data-stu-id="96265-152">window</span></span>                         | <span data-ttu-id="96265-153">Recupera o tamanho atual e a posição do quadro da janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="96265-153">Retrieves the current size and position of the display-window frame.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="96265-154">janela [ **máxima**](max.md)</span><span class="sxs-lookup"><span data-stu-id="96265-154">window [**max**](max.md)</span></span>      | <span data-ttu-id="96265-155">Recupera o tamanho da tela inteira.</span><span class="sxs-lookup"><span data-stu-id="96265-155">Retrieves the size of the entire display.</span></span>                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="96265-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="96265-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="96265-157">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="96265-157">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="96265-158">Para dispositivos de vídeo digital, "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="96265-158">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="96265-159">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="96265-159">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96265-160">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="96265-160">Return Value</span></span>

<span data-ttu-id="96265-161">Retorna um retângulo no parâmetro *lpszReturnString* da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="96265-161">Returns a rectangle in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="96265-162">O retângulo descreve a área especificada no parâmetro *lpszRequestRect* deste comando.</span><span class="sxs-lookup"><span data-stu-id="96265-162">The rectangle describes the area specified in the *lpszRequestRect* parameter of this command.</span></span> <span data-ttu-id="96265-163">O retângulo é especificado como *X1 Y1 x2 y2*.</span><span class="sxs-lookup"><span data-stu-id="96265-163">The rectangle is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="96265-164">As coordenadas *X1 Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *x2 y2* especificam a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="96265-164">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span>

## <a name="examples"></a><span data-ttu-id="96265-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96265-165">Examples</span></span>

<span data-ttu-id="96265-166">O comando a seguir retorna o retângulo de exibição do dispositivo de "filme".</span><span class="sxs-lookup"><span data-stu-id="96265-166">The following command returns the display rectangle of the "movie" device.</span></span>

``` syntax
where movie destination
```

## <a name="requirements"></a><span data-ttu-id="96265-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96265-167">Requirements</span></span>



| <span data-ttu-id="96265-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="96265-168">Requirement</span></span> | <span data-ttu-id="96265-169">Valor</span><span class="sxs-lookup"><span data-stu-id="96265-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="96265-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96265-170">Minimum supported client</span></span><br/> | <span data-ttu-id="96265-171">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96265-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="96265-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96265-172">Minimum supported server</span></span><br/> | <span data-ttu-id="96265-173">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96265-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="96265-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="96265-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96265-175">MCI</span><span class="sxs-lookup"><span data-stu-id="96265-175">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="96265-176">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="96265-176">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="96265-177">Posicione</span><span class="sxs-lookup"><span data-stu-id="96265-177">put</span></span>](put.md)
</dt> </dl>

 

