---
title: comando setajuster
description: O comando setajustarr altera o sintonizador atual ou a configuração de canal do sintonizador atual. Os dispositivos VCR reconhecem este comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- Multimídia do Windows do comando setajuster
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456030"
---
# <a name="settuner-command"></a><span data-ttu-id="1142b-105">comando setajuster</span><span class="sxs-lookup"><span data-stu-id="1142b-105">settuner command</span></span>

<span data-ttu-id="1142b-106">O comando setajustarr altera o sintonizador atual ou a configuração de canal do sintonizador atual.</span><span class="sxs-lookup"><span data-stu-id="1142b-106">The settuner command changes the current tuner or the channel setting of the current tuner.</span></span> <span data-ttu-id="1142b-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="1142b-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="1142b-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="1142b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="1142b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1142b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1142b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1142b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1142b-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="1142b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="1142b-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="1142b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="1142b-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span><span class="sxs-lookup"><span data-stu-id="1142b-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span></span>
</dt> <dd>

<span data-ttu-id="1142b-114">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1142b-114">One of the following flags.</span></span>



| <span data-ttu-id="1142b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1142b-115">Value</span></span>                            | <span data-ttu-id="1142b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1142b-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1142b-117">*canal* de canal</span><span class="sxs-lookup"><span data-stu-id="1142b-117">channel *channel*</span></span>                | <span data-ttu-id="1142b-118">Define o sintonizador como *canal*.</span><span class="sxs-lookup"><span data-stu-id="1142b-118">Sets the tuner to *channel*.</span></span> <span data-ttu-id="1142b-119">Talvez você não consiga alterar o canal durante a gravação, dependendo do VCR.</span><span class="sxs-lookup"><span data-stu-id="1142b-119">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="1142b-120">Um canal maior do que o máximo define o sintonizador para o canal máximo.</span><span class="sxs-lookup"><span data-stu-id="1142b-120">A channel larger than the maximum sets the tuner to the maximum channel.</span></span>                                                                                                                    |
| <span data-ttu-id="1142b-121">busca de upchannel de busca de canal</span><span class="sxs-lookup"><span data-stu-id="1142b-121">channel seek upchannel seek down</span></span> | <span data-ttu-id="1142b-122">Procura o próximo canal com um sinal válido.</span><span class="sxs-lookup"><span data-stu-id="1142b-122">Seeks the next channel with a valid signal.</span></span> <span data-ttu-id="1142b-123">"Procurar" incrementa o número de canal em sua pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1142b-123">"Seek up" increments the channel number in its search.</span></span> <span data-ttu-id="1142b-124">"Busca inativa" Decrementa o número do canal em sua pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1142b-124">"Seek down" decrements the channel number in its search.</span></span> <span data-ttu-id="1142b-125">O sintonizador encapsula para o canal 1 quando o número máximo do canal é excedido.</span><span class="sxs-lookup"><span data-stu-id="1142b-125">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="1142b-126">Da mesma forma, ao procurar, o sintonizador é ajustado para o canal máximo.</span><span class="sxs-lookup"><span data-stu-id="1142b-126">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span> |
| <span data-ttu-id="1142b-127">upchannel do canal inativo</span><span class="sxs-lookup"><span data-stu-id="1142b-127">channel upchannel down</span></span>           | <span data-ttu-id="1142b-128">Incrementa ou Decrementa o canal do sintonizador.</span><span class="sxs-lookup"><span data-stu-id="1142b-128">Increments or decrements the tuner channel.</span></span> <span data-ttu-id="1142b-129">Talvez você não consiga alterar o canal durante a gravação, dependendo do VCR.</span><span class="sxs-lookup"><span data-stu-id="1142b-129">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="1142b-130">O sintonizador encapsula para o canal 1 quando o número máximo do canal é excedido.</span><span class="sxs-lookup"><span data-stu-id="1142b-130">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="1142b-131">Da mesma forma, ao procurar, o sintonizador é ajustado para o canal máximo.</span><span class="sxs-lookup"><span data-stu-id="1142b-131">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span>                              |
| <span data-ttu-id="1142b-132">*número* de número</span><span class="sxs-lookup"><span data-stu-id="1142b-132">number *number*</span></span>                  | <span data-ttu-id="1142b-133">Especifica o sintonizador a ser afetado pelo comando setajuster.</span><span class="sxs-lookup"><span data-stu-id="1142b-133">Specifies the tuner to be affected by the settuner command.</span></span> <span data-ttu-id="1142b-134">Se *núm* não for fornecido, o valor padrão de 1 será assumido.</span><span class="sxs-lookup"><span data-stu-id="1142b-134">If *number* is not given, the default value of 1 is assumed.</span></span>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="1142b-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="1142b-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1142b-136">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="1142b-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="1142b-137">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1142b-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1142b-138">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1142b-138">Return Value</span></span>

<span data-ttu-id="1142b-139">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="1142b-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1142b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1142b-140">Requirements</span></span>



| <span data-ttu-id="1142b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1142b-141">Requirement</span></span> | <span data-ttu-id="1142b-142">Valor</span><span class="sxs-lookup"><span data-stu-id="1142b-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1142b-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1142b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1142b-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1142b-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1142b-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1142b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1142b-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1142b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1142b-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="1142b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1142b-148">MCI</span><span class="sxs-lookup"><span data-stu-id="1142b-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1142b-149">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="1142b-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

