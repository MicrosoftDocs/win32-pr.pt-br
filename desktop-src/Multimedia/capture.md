---
title: comando de captura
description: O comando Capture copia o conteúdo do buffer de quadro e o armazena no arquivo especificado. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- Multimídia do Windows de comando de captura
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086302"
---
# <a name="capture-command"></a><span data-ttu-id="1c6d7-105">comando de captura</span><span class="sxs-lookup"><span data-stu-id="1c6d7-105">capture command</span></span>

<span data-ttu-id="1c6d7-106">O comando Capture copia o conteúdo do buffer de quadro e o armazena no arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-106">The capture command copies the contents of the frame buffer and stores it in the specified file.</span></span> <span data-ttu-id="1c6d7-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="1c6d7-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="1c6d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c6d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c6d7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1c6d7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1c6d7-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-111">Identifier of an MCI device.</span></span> <span data-ttu-id="1c6d7-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="1c6d7-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span><span class="sxs-lookup"><span data-stu-id="1c6d7-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span></span>
</dt> <dd>

<span data-ttu-id="1c6d7-114">Um ou mais dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="1c6d7-114">One or more of the following flags:</span></span>



| <span data-ttu-id="1c6d7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1c6d7-115">Value</span></span>          | <span data-ttu-id="1c6d7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1c6d7-116">Meaning</span></span>                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6d7-117">como *nome do caminho*</span><span class="sxs-lookup"><span data-stu-id="1c6d7-117">as *pathname*</span></span>  | <span data-ttu-id="1c6d7-118">Especifica o caminho de destino e o nome do arquivo para a imagem capturada.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-118">Specifies the destination path and filename for the captured image.</span></span> <span data-ttu-id="1c6d7-119">Esse sinalizador é necessário.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-119">This flag is required.</span></span>                                                                                                                                                                |
| <span data-ttu-id="1c6d7-120">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="1c6d7-120">at *rectangle*</span></span> | <span data-ttu-id="1c6d7-121">Especifica a região retangular dentro do buffer de quadro que o dispositivo corta e salva em disco.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-121">Specifies the rectangular region within the frame buffer that the device crops and saves to disk.</span></span> <span data-ttu-id="1c6d7-122">Se omitido, a região cortada usa como padrão o retângulo especificado ou padronizado em um comando "Source" de [Put](put.md) anterior para essa instância de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-122">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [put](put.md) "source" command for this device instance.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1c6d7-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="1c6d7-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1c6d7-124">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-124">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="1c6d7-125">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1c6d7-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c6d7-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1c6d7-126">Return Value</span></span>

<span data-ttu-id="1c6d7-127">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c6d7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c6d7-128">Remarks</span></span>

<span data-ttu-id="1c6d7-129">Esse comando poderá falhar se o dispositivo estiver executando o vídeo de movimento no momento ou executando alguma outra operação de uso intensivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-129">This command might fail if the device is currently playing motion video or executing some other resource-intensive operation.</span></span> <span data-ttu-id="1c6d7-130">Se o buffer de quadros estiver sendo atualizado em tempo real, a atualização pausará momentaneamente para que uma imagem completa seja capturada.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-130">If the frame buffer is being updated in real time, the updating momentarily pauses so that a complete image is captured.</span></span> <span data-ttu-id="1c6d7-131">Se o dispositivo pausar a atualização, poderá haver um efeito visual ou audível.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-131">If the device pauses the updating, there might be a visual or audible effect.</span></span> <span data-ttu-id="1c6d7-132">Se o formato de arquivo, o algoritmo de compactação e os níveis de qualidade não tiverem sido definidos, seus padrões serão usados.</span><span class="sxs-lookup"><span data-stu-id="1c6d7-132">If the file format, compression algorithm, and quality levels have not been set, their defaults are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6d7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c6d7-133">Requirements</span></span>



| <span data-ttu-id="1c6d7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c6d7-134">Requirement</span></span> | <span data-ttu-id="1c6d7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1c6d7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c6d7-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c6d7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6d7-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1c6d7-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c6d7-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c6d7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6d7-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1c6d7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1c6d7-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c6d7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6d7-141">MCI</span><span class="sxs-lookup"><span data-stu-id="1c6d7-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1c6d7-142">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="1c6d7-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="1c6d7-143">Posicione</span><span class="sxs-lookup"><span data-stu-id="1c6d7-143">put</span></span>](put.md)
</dt> </dl>

 

