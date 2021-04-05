---
title: comando put
description: O comando put define a área da imagem de origem e a janela de destino usadas para exibição. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- comando put multimídia do Windows
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086231"
---
# <a name="put-command"></a><span data-ttu-id="c2305-105">comando put</span><span class="sxs-lookup"><span data-stu-id="c2305-105">put command</span></span>

<span data-ttu-id="c2305-106">O comando put define a área da imagem de origem e a janela de destino usadas para exibição.</span><span class="sxs-lookup"><span data-stu-id="c2305-106">The put command defines the area of the source image and destination window used for display.</span></span> <span data-ttu-id="c2305-107">Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="c2305-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="c2305-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c2305-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c2305-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2305-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2305-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c2305-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c2305-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c2305-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c2305-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="c2305-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c2305-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span><span class="sxs-lookup"><span data-stu-id="c2305-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span></span>
</dt> <dd>

<span data-ttu-id="c2305-114">Sinalizador para definir a área.</span><span class="sxs-lookup"><span data-stu-id="c2305-114">Flag for defining the area.</span></span> <span data-ttu-id="c2305-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando put e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="c2305-115">The following table lists device types that recognize the put command and the flags used by each type.</span></span>



| <span data-ttu-id="c2305-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c2305-116">Value</span></span>        | <span data-ttu-id="c2305-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c2305-117">Meaning</span></span>                                                                                      | <span data-ttu-id="c2305-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c2305-118">Meaning</span></span>                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2305-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c2305-119">digitalvideo</span></span> | <span data-ttu-id="c2305-120">destino de destino no quadro de quadro do *retângulo* na fonte de origem do *retângulo* no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-120">destination destination at *rectangle* frame frame at *rectangle* source source at *rectangle*</span></span> | <span data-ttu-id="c2305-121">vídeo em vídeo na janela de janela do *retângulo* na janela do *retângulo* cliente da janela do cliente no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-121">video video at *rectangle* window window at *rectangle* window client window client at *rectangle*</span></span> |
| <span data-ttu-id="c2305-122">overlay</span><span class="sxs-lookup"><span data-stu-id="c2305-122">overlay</span></span>      | <span data-ttu-id="c2305-123">destino de destino no quadro de quadro do *retângulo* no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-123">destination destination at *rectangle* frame frame at *rectangle*</span></span>                             | <span data-ttu-id="c2305-124">fonte de origem no vídeo de vídeo de *retângulo* no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-124">source source at *rectangle* video video at *rectangle*</span></span>                                           |



 

<span data-ttu-id="c2305-125">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRegions** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="c2305-125">The following table lists the flags that can be specified in the **lpszRegions** parameter and their meanings.</span></span>



| <span data-ttu-id="c2305-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c2305-126">Value</span></span>                        | <span data-ttu-id="c2305-127">Significado</span><span class="sxs-lookup"><span data-stu-id="c2305-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2305-128">destino</span><span class="sxs-lookup"><span data-stu-id="c2305-128">destination</span></span>                  | <span data-ttu-id="c2305-129">Seleciona toda a área do cliente da janela de destino para exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="c2305-129">Selects the entire client area of the destination window to display the data.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c2305-130">destino no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-130">destination at *rectangle*</span></span>   | <span data-ttu-id="c2305-131">Seleciona uma parte da área do cliente da janela de destino usada para exibir a imagem.</span><span class="sxs-lookup"><span data-stu-id="c2305-131">Selects a portion of the client area of the destination window used to display the image.</span></span> <span data-ttu-id="c2305-132">Quando uma área da janela de exibição é especificada e o dispositivo dá suporte à ampliação, a imagem de origem é esticada para o deslocamento e a extensão de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-132">When an area of the display window is specified and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                     |
| <span data-ttu-id="c2305-133">frame</span><span class="sxs-lookup"><span data-stu-id="c2305-133">frame</span></span>                        | <span data-ttu-id="c2305-134">Seleciona o buffer de quadro inteiro para receber as imagens de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2305-134">Selects the entire frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c2305-135">quadro no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-135">frame at *rectangle*</span></span>         | <span data-ttu-id="c2305-136">Seleciona uma parte do buffer de quadro para receber as imagens de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2305-136">Selects a portion of the frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c2305-137">source</span><span class="sxs-lookup"><span data-stu-id="c2305-137">source</span></span>                       | <span data-ttu-id="c2305-138">Seleciona a imagem inteira para exibição na janela de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-138">Selects the entire image for display in the destination window.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c2305-139">fonte no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-139">source at *rectangle*</span></span>        | <span data-ttu-id="c2305-140">Seleciona uma parte da imagem a ser exibida na janela de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-140">Selects a portion of the image to display in the destination window.</span></span> <span data-ttu-id="c2305-141">Quando uma área da imagem de origem é especificada e o dispositivo dá suporte à ampliação, a imagem de origem é esticada para o deslocamento e a extensão de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-141">When an area of the source image is specified, and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                                           |
| <span data-ttu-id="c2305-142">video</span><span class="sxs-lookup"><span data-stu-id="c2305-142">video</span></span>                        | <span data-ttu-id="c2305-143">Seleciona a imagem de vídeo de entrada inteira a ser capturada no buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="c2305-143">Selects the entire incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c2305-144">vídeo no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-144">video at *rectangle*</span></span>         | <span data-ttu-id="c2305-145">Seleciona uma parte da imagem de vídeo de entrada a ser capturada no buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="c2305-145">Selects a portion of the incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c2305-146">janela</span><span class="sxs-lookup"><span data-stu-id="c2305-146">window</span></span>                       | <span data-ttu-id="c2305-147">Restaura o tamanho inicial da janela na exibição.</span><span class="sxs-lookup"><span data-stu-id="c2305-147">Restores the initial window size on the display.</span></span> <span data-ttu-id="c2305-148">Esse comando também exibe a janela.</span><span class="sxs-lookup"><span data-stu-id="c2305-148">This command also displays the window.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c2305-149">janela no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-149">window at *rectangle*</span></span>        | <span data-ttu-id="c2305-150">Altera o tamanho e o local da janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2305-150">Changes the size and location of the display window.</span></span> <span data-ttu-id="c2305-151">O retângulo especificado é relativo à janela pai da janela de exibição (normalmente a área de trabalho) se o sinalizador "estilo filho" tiver sido usado para o comando [abrir](open.md) .</span><span class="sxs-lookup"><span data-stu-id="c2305-151">The specified rectangle is relative to the parent window of the display window (usually the desktop) if the "style child" flag has been used for the [open](open.md) command.</span></span> <span data-ttu-id="c2305-152">Para alterar o local da janela sem alterar sua altura ou largura, especifique zero para a altura e a largura.</span><span class="sxs-lookup"><span data-stu-id="c2305-152">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span> |
| <span data-ttu-id="c2305-153">cliente do Windows</span><span class="sxs-lookup"><span data-stu-id="c2305-153">window client</span></span>                | <span data-ttu-id="c2305-154">Restaura a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="c2305-154">Restores the client area of the window.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c2305-155">cliente de janela no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="c2305-155">window client at *rectangle*</span></span> | <span data-ttu-id="c2305-156">Altera o tamanho e o local da área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="c2305-156">Changes the size and location of the client area of the window.</span></span> <span data-ttu-id="c2305-157">O retângulo especificado é relativo à janela pai da janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="c2305-157">The specified rectangle is relative to the parent window of the client window.</span></span> <span data-ttu-id="c2305-158">Para alterar o local da janela sem alterar sua altura ou largura, especifique zero para a altura e a largura.</span><span class="sxs-lookup"><span data-stu-id="c2305-158">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span>                                                                                      |



 

<span data-ttu-id="c2305-159">Quando um sinalizador inclui um retângulo, as coordenadas do retângulo são relativas à origem da janela ou à origem da imagem, conforme apropriado, e são especificadas como **X1 Y1 x2 y2**.</span><span class="sxs-lookup"><span data-stu-id="c2305-159">When a flag includes a rectangle, the rectangle coordinates are relative to the window origin or the image origin, as appropriate, and are specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="c2305-160">As coordenadas **X1Y1** especificam o canto superior esquerdo e as coordenadas **X2Y2** especificam a largura e a altura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="c2305-160">The coordinates **X1Y1** specify the upper left corner, and the coordinates **X2Y2** specify the width and height of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="c2305-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c2305-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c2305-162">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="c2305-162">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c2305-163">Para dispositivos de vídeo digital, "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c2305-163">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="c2305-164">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c2305-164">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2305-165">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c2305-165">Return Value</span></span>

<span data-ttu-id="c2305-166">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c2305-166">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2305-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2305-167">Remarks</span></span>

<span data-ttu-id="c2305-168">O comando put define um ou mais dos seguintes retângulos ao trabalhar com dispositivos de sobreposição de vídeo:</span><span class="sxs-lookup"><span data-stu-id="c2305-168">The put command defines one or more of the following rectangles when working with video-overlay devices:</span></span>

-   <span data-ttu-id="c2305-169">O retângulo de vídeo define a região da imagem de vídeo de entrada a ser capturada.</span><span class="sxs-lookup"><span data-stu-id="c2305-169">The video rectangle defines the region of the incoming video image to capture.</span></span>
-   <span data-ttu-id="c2305-170">O retângulo do quadro define a região do buffer de quadro que recebe a imagem de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2305-170">The frame rectangle defines the region of the frame buffer that receives the incoming video image.</span></span>
-   <span data-ttu-id="c2305-171">O retângulo de origem define qual região do buffer de quadro é copiada para o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-171">The source rectangle defines which region of the frame buffer is copied to the destination rectangle.</span></span>
-   <span data-ttu-id="c2305-172">O retângulo de destino define a região da área do cliente da janela de exibição que recebe a imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2305-172">The destination rectangle defines the region of the display window client area that receives the video image.</span></span>

<span data-ttu-id="c2305-173">O retângulo de vídeo está relacionado ao retângulo do quadro da mesma maneira que o retângulo de origem está relacionado ao retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-173">The video rectangle is related to the frame rectangle in the same way the source rectangle is related to the destination rectangle.</span></span> <span data-ttu-id="c2305-174">O alongamento pode ocorrer do retângulo de vídeo para o retângulo de quadro e do retângulo de origem para o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-174">Stretching can occur from the video rectangle to the frame rectangle and from the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="c2305-175">Nem todos os dispositivos dão suporte ao alongamento, e o alongamento deve ser habilitado (usando o comando [set](set.md) ).</span><span class="sxs-lookup"><span data-stu-id="c2305-175">Not all devices support stretching, and stretching must be enabled (by using the [set](set.md) command).</span></span>

<span data-ttu-id="c2305-176">O comando a seguir define três regiões para o vídeo, o quadro e a fonte.</span><span class="sxs-lookup"><span data-stu-id="c2305-176">The following command defines three regions for the video, frame, and source.</span></span>

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

<span data-ttu-id="c2305-177">As regiões neste exemplo são definidas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c2305-177">The regions in this example are defined as follows:</span></span>

-   <span data-ttu-id="c2305-178">Uma região de 200 a 200 pixels dos dados de vídeo de entrada, começando com uma origem 120 pixels no canto superior esquerdo, será capturada para o buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="c2305-178">A 200- by 200-pixel region of the incoming video data, starting at an origin 120 pixels from the upper left corner, will be captured to the frame buffer.</span></span>
-   <span data-ttu-id="c2305-179">Os dados de vídeo serão colocados em uma região de 200 por 200 pixels no canto superior esquerdo do buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="c2305-179">The video data will be placed in a 200- by 200-pixel region at the upper left corner of the frame buffer.</span></span>
-   <span data-ttu-id="c2305-180">São feitas transferências da região 200-por 200 pixels no canto superior esquerdo do buffer de quadro para a janela de destino.</span><span class="sxs-lookup"><span data-stu-id="c2305-180">Transfers are made from the 200- by 200-pixel region at the upper left corner of the frame buffer to the destination window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2305-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2305-181">Requirements</span></span>



| <span data-ttu-id="c2305-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2305-182">Requirement</span></span> | <span data-ttu-id="c2305-183">Valor</span><span class="sxs-lookup"><span data-stu-id="c2305-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c2305-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2305-184">Minimum supported client</span></span><br/> | <span data-ttu-id="c2305-185">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2305-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2305-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2305-186">Minimum supported server</span></span><br/> | <span data-ttu-id="c2305-187">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2305-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c2305-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2305-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2305-189">MCI</span><span class="sxs-lookup"><span data-stu-id="c2305-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c2305-190">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="c2305-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c2305-191">open</span><span class="sxs-lookup"><span data-stu-id="c2305-191">open</span></span>](open.md)
</dt> <dt>

[<span data-ttu-id="c2305-192">set</span><span class="sxs-lookup"><span data-stu-id="c2305-192">set</span></span>](set.md)
</dt> </dl>

 

