---
title: carregar comando
description: O comando carregar carrega um arquivo em um formato específico do dispositivo. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- carregar multimídia do Windows de comando
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644898"
---
# <a name="load-command"></a><span data-ttu-id="c96d8-105">carregar comando</span><span class="sxs-lookup"><span data-stu-id="c96d8-105">load command</span></span>

<span data-ttu-id="c96d8-106">O comando carregar carrega um arquivo em um formato específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c96d8-106">The load command loads a file in a device-specific format.</span></span> <span data-ttu-id="c96d8-107">Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="c96d8-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="c96d8-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c96d8-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c96d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c96d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c96d8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c96d8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c96d8-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c96d8-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c96d8-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="c96d8-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c96d8-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span><span class="sxs-lookup"><span data-stu-id="c96d8-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="c96d8-114">Caminho e nome de arquivo a serem carregados.</span><span class="sxs-lookup"><span data-stu-id="c96d8-114">Path and filename to load.</span></span> <span data-ttu-id="c96d8-115">Para dispositivos de sobreposição de vídeo, isso também pode incluir um retângulo de destino para os dados.</span><span class="sxs-lookup"><span data-stu-id="c96d8-115">For video-overlay devices, this can also include a target rectangle for the data.</span></span> <span data-ttu-id="c96d8-116">Para especificar um retângulo de destino, especifique "at" seguido por **X1 Y1 x2 y2**, em que **X1 Y1** especifica o canto superior esquerdo do retângulo e **x2 y2** especifique a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="c96d8-116">To specify a target rectangle, specify "at" followed by **X1 Y1 X2 Y2**, where **X1 Y1** specify the upper left corner of the rectangle, and **X2 Y2** specify the width and height.</span></span> <span data-ttu-id="c96d8-117">O retângulo é relativo à origem do buffer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c96d8-117">The rectangle is relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="c96d8-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c96d8-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c96d8-119">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="c96d8-119">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c96d8-120">Para dispositivos de vídeo digital, "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c96d8-120">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="c96d8-121">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c96d8-121">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c96d8-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c96d8-122">Return Value</span></span>

<span data-ttu-id="c96d8-123">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c96d8-123">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c96d8-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c96d8-124">Remarks</span></span>

<span data-ttu-id="c96d8-125">O dispositivo "vidboard" envia uma mensagem de notificação quando o carregamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="c96d8-125">The "vidboard" device sends a notification message when the loading is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="c96d8-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c96d8-126">Examples</span></span>

<span data-ttu-id="c96d8-127">O comando a seguir carrega um arquivo no dispositivo "vidboard".</span><span class="sxs-lookup"><span data-stu-id="c96d8-127">The following command loads a file into the "vidboard" device.</span></span>

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a><span data-ttu-id="c96d8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c96d8-128">Requirements</span></span>



| <span data-ttu-id="c96d8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c96d8-129">Requirement</span></span> | <span data-ttu-id="c96d8-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c96d8-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c96d8-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c96d8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c96d8-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c96d8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c96d8-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c96d8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c96d8-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c96d8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c96d8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c96d8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96d8-136">MCI</span><span class="sxs-lookup"><span data-stu-id="c96d8-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c96d8-137">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="c96d8-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

