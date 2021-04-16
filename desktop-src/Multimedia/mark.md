---
title: comando de marca
description: O comando Mark controla a gravação e o apagamento de marcas na fita de vídeo. Os dispositivos VCR reconhecem este comando.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- comando marcar multimídia do Windows
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758749"
---
# <a name="mark-command"></a><span data-ttu-id="199d3-105">comando de marca</span><span class="sxs-lookup"><span data-stu-id="199d3-105">mark command</span></span>

<span data-ttu-id="199d3-106">O comando Mark controla a gravação e o apagamento de marcas na fita de vídeo.</span><span class="sxs-lookup"><span data-stu-id="199d3-106">The mark command controls recording and erasing of marks on the videotape.</span></span> <span data-ttu-id="199d3-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="199d3-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="199d3-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="199d3-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="199d3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="199d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="199d3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="199d3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="199d3-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="199d3-111">Identifier of an MCI device.</span></span> <span data-ttu-id="199d3-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="199d3-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="199d3-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span><span class="sxs-lookup"><span data-stu-id="199d3-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span></span>
</dt> <dd>

<span data-ttu-id="199d3-114">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="199d3-114">One of the following flags.</span></span>



| <span data-ttu-id="199d3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="199d3-115">Value</span></span> | <span data-ttu-id="199d3-116">Significado</span><span class="sxs-lookup"><span data-stu-id="199d3-116">Meaning</span></span>                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="199d3-117">erase</span><span class="sxs-lookup"><span data-stu-id="199d3-117">erase</span></span> | <span data-ttu-id="199d3-118">Apaga uma marca na posição atual, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="199d3-118">Erases a mark at the current position, if one exists.</span></span> <span data-ttu-id="199d3-119">Para apagar uma marca, primeiro busque para a marca e, em seguida, emite o comando marcar "apagar".</span><span class="sxs-lookup"><span data-stu-id="199d3-119">To erase a mark, first seek to the mark and then issue the mark "erase" command.</span></span> |
| <span data-ttu-id="199d3-120">gravação</span><span class="sxs-lookup"><span data-stu-id="199d3-120">write</span></span> | <span data-ttu-id="199d3-121">Grava uma marca na posição atual.</span><span class="sxs-lookup"><span data-stu-id="199d3-121">Writes a mark at the current position.</span></span> <span data-ttu-id="199d3-122">O VCR pode precisar estar no modo de gravação ou de registro para que esse comando seja executado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="199d3-122">The VCR might need to be in play or record mode for this command to succeed.</span></span>                    |



 

</dd> <dt>

<span data-ttu-id="199d3-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="199d3-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="199d3-124">Pode ser "Wait", "Notify" ou "Test".</span><span class="sxs-lookup"><span data-stu-id="199d3-124">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="199d3-125">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="199d3-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="199d3-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="199d3-126">Return Value</span></span>

<span data-ttu-id="199d3-127">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="199d3-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="199d3-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="199d3-128">Remarks</span></span>

<span data-ttu-id="199d3-129">As marcas são sinais especiais gravados no conteúdo que podem ser detectados pelo VCR durante pesquisas de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="199d3-129">Marks are special signals written to the content that can be detected by the VCR during high-speed searches.</span></span> <span data-ttu-id="199d3-130">As marcas são específicas do VCR.</span><span class="sxs-lookup"><span data-stu-id="199d3-130">Marks are VCR specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="199d3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="199d3-131">Requirements</span></span>



| <span data-ttu-id="199d3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="199d3-132">Requirement</span></span> | <span data-ttu-id="199d3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="199d3-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="199d3-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="199d3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="199d3-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="199d3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="199d3-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="199d3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="199d3-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="199d3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="199d3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="199d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199d3-139">MCI</span><span class="sxs-lookup"><span data-stu-id="199d3-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="199d3-140">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="199d3-140">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

