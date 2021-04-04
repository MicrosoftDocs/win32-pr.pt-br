---
title: comando fechar (Corecrt \_ Io. h)
description: O comando fechar fecha o dispositivo ou arquivo e todos os recursos associados. O MCI descarrega um dispositivo quando todas as instâncias do dispositivo ou todos os arquivos são fechados. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- fechar o comando multimídia do Windows
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918329"
---
# <a name="close-command"></a><span data-ttu-id="297a0-106">comando fechar</span><span class="sxs-lookup"><span data-stu-id="297a0-106">close command</span></span>

<span data-ttu-id="297a0-107">O comando fechar fecha o dispositivo ou arquivo e todos os recursos associados.</span><span class="sxs-lookup"><span data-stu-id="297a0-107">The close command closes the device or file and any associated resources.</span></span> <span data-ttu-id="297a0-108">O MCI descarrega um dispositivo quando todas as instâncias do dispositivo ou todos os arquivos são fechados.</span><span class="sxs-lookup"><span data-stu-id="297a0-108">MCI unloads a device when all instances of the device or all files are closed.</span></span> <span data-ttu-id="297a0-109">Todos os dispositivos MCI reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="297a0-109">All MCI devices recognize this command.</span></span>

<span data-ttu-id="297a0-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="297a0-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="297a0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="297a0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="297a0-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="297a0-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="297a0-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="297a0-113">Identifier of an MCI device.</span></span> <span data-ttu-id="297a0-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="297a0-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="297a0-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="297a0-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="297a0-116">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="297a0-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="297a0-117">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="297a0-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="297a0-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="297a0-118">Return Value</span></span>

<span data-ttu-id="297a0-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="297a0-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="297a0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="297a0-120">Remarks</span></span>

<span data-ttu-id="297a0-121">Para fechar todos os dispositivos abertos pelo seu aplicativo, especifique o identificador de dispositivo "todos" para o parâmetro *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="297a0-121">To close all devices opened by your application, specify the "all" device identifier for the *lpszDeviceID* parameter.</span></span>

<span data-ttu-id="297a0-122">Fechar o dispositivo **cdaudio** para a reprodução de áudio.</span><span class="sxs-lookup"><span data-stu-id="297a0-122">Closing the **cdaudio** device stops audio playback.</span></span>

<span data-ttu-id="297a0-123">**Windows 2000/XP:** Se o dispositivo **cdaudio** estiver em execução, fechar o dispositivo **cdaudio** não fará com que o áudio pare de ser executado.</span><span class="sxs-lookup"><span data-stu-id="297a0-123">**Windows 2000/XP:** If the **cdaudio** device is playing, closing the **cdaudio** device does not cause the audio to stop playing.</span></span> <span data-ttu-id="297a0-124">Envie o comando [Stop](stop.md) primeiro.</span><span class="sxs-lookup"><span data-stu-id="297a0-124">Send the [stop](stop.md) command first.</span></span>

## <a name="examples"></a><span data-ttu-id="297a0-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="297a0-125">Examples</span></span>

<span data-ttu-id="297a0-126">O comando a seguir fecha o dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="297a0-126">The following command closes the "mysound" device.</span></span>

``` syntax
close mysound
```

## <a name="requirements"></a><span data-ttu-id="297a0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="297a0-127">Requirements</span></span>



| <span data-ttu-id="297a0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="297a0-128">Requirement</span></span> | <span data-ttu-id="297a0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="297a0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="297a0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="297a0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="297a0-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="297a0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="297a0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="297a0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="297a0-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="297a0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="297a0-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="297a0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="297a0-135"><dt>Corecrt \_ Io. h</dt></span><span class="sxs-lookup"><span data-stu-id="297a0-135"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="297a0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="297a0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297a0-137">MCI</span><span class="sxs-lookup"><span data-stu-id="297a0-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="297a0-138">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="297a0-138">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

