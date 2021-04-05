---
title: obter o comando
description: O comando perceber instrui um dispositivo a selecionar e a perceber sua paleta no contexto de exibição da janela exibida. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- perceba o multimídia do Windows de comando
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919009"
---
# <a name="realize-command"></a><span data-ttu-id="a6f0a-105">obter o comando</span><span class="sxs-lookup"><span data-stu-id="a6f0a-105">realize command</span></span>

<span data-ttu-id="a6f0a-106">O comando perceber instrui um dispositivo a selecionar e a perceber sua paleta no contexto de exibição da janela exibida.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-106">The realize command instructs a device to select and realize its palette into the display context of the displayed window.</span></span> <span data-ttu-id="a6f0a-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="a6f0a-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a6f0a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6f0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f0a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a6f0a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a6f0a-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a6f0a-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a6f0a-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span><span class="sxs-lookup"><span data-stu-id="a6f0a-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span></span>
</dt> <dd>

<span data-ttu-id="a6f0a-114">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-114">One of the following flags.</span></span>



| <span data-ttu-id="a6f0a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a6f0a-115">Value</span></span>      | <span data-ttu-id="a6f0a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a6f0a-116">Meaning</span></span>                                                                   |
|------------|---------------------------------------------------------------------------|
| <span data-ttu-id="a6f0a-117">background</span><span class="sxs-lookup"><span data-stu-id="a6f0a-117">background</span></span> | <span data-ttu-id="a6f0a-118">Percebe a paleta como uma paleta de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-118">Realizes the palette as a background palette.</span></span>                             |
| <span data-ttu-id="a6f0a-119">normal</span><span class="sxs-lookup"><span data-stu-id="a6f0a-119">normal</span></span>     | <span data-ttu-id="a6f0a-120">Percebe a paleta para uma janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-120">Realizes the palette for a top-level window.</span></span> <span data-ttu-id="a6f0a-121">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-121">This is the default setting.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a6f0a-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a6f0a-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a6f0a-123">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-123">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a6f0a-124">Para dispositivos de vídeo digital, "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-124">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="a6f0a-125">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a6f0a-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f0a-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a6f0a-126">Return Value</span></span>

<span data-ttu-id="a6f0a-127">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f0a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6f0a-128">Remarks</span></span>

<span data-ttu-id="a6f0a-129">Use este comando somente se o seu aplicativo usar um identificador de janela e receber uma mensagem do **WM \_ QUERYNEWPALLETTE** ou do **WM da \_ paletachanged** .</span><span class="sxs-lookup"><span data-stu-id="a6f0a-129">Use this command only if your application uses a window handle and receives a **WM\_QUERYNEWPALLETTE** or **WM\_PALETTECHANGED** message.</span></span>

## <a name="examples"></a><span data-ttu-id="a6f0a-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6f0a-130">Examples</span></span>

<span data-ttu-id="a6f0a-131">O comando a seguir informa o dispositivo "MyVideo" para perceber sua paleta.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-131">The following command tells the "myvideo" device to realize its palette.</span></span>

``` syntax
realize myvideo normal
```

## <a name="requirements"></a><span data-ttu-id="a6f0a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6f0a-132">Requirements</span></span>



| <span data-ttu-id="a6f0a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6f0a-133">Requirement</span></span> | <span data-ttu-id="a6f0a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a6f0a-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a6f0a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6f0a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f0a-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a6f0a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a6f0a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6f0a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f0a-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a6f0a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a6f0a-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6f0a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f0a-140">MCI</span><span class="sxs-lookup"><span data-stu-id="a6f0a-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a6f0a-141">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="a6f0a-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

