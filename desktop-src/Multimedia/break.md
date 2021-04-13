---
title: comando de quebra
description: O comando Break especifica uma chave para anular um comando que foi invocado usando o \ 0034; Wait \ 0034; identificar. Esse comando é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando de quebra de multimídia do Windows
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455885"
---
# <a name="break-command"></a><span data-ttu-id="073b2-105">comando de quebra</span><span class="sxs-lookup"><span data-stu-id="073b2-105">break command</span></span>

<span data-ttu-id="073b2-106">O comando Break especifica uma chave para anular um comando que foi invocado usando o sinalizador "Wait".</span><span class="sxs-lookup"><span data-stu-id="073b2-106">The break command specifies a key to abort a command that was invoked using the "wait" flag.</span></span> <span data-ttu-id="073b2-107">Esse comando é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.</span><span class="sxs-lookup"><span data-stu-id="073b2-107">This command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="073b2-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="073b2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="073b2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="073b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="073b2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="073b2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="073b2-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="073b2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="073b2-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="073b2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="073b2-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span><span class="sxs-lookup"><span data-stu-id="073b2-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span></span>
</dt> <dd>

<span data-ttu-id="073b2-114">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="073b2-114">One of the following flags.</span></span>



| <span data-ttu-id="073b2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="073b2-115">Value</span></span>                 | <span data-ttu-id="073b2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="073b2-116">Meaning</span></span>                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="073b2-117">no *código de chave virtual*</span><span class="sxs-lookup"><span data-stu-id="073b2-117">on *virtual key code*</span></span> | <span data-ttu-id="073b2-118">Especifica a chave que anula um comando que foi iniciado usando o sinalizador "Wait".</span><span class="sxs-lookup"><span data-stu-id="073b2-118">Specifies the key that aborts a command that was started using the "wait" flag.</span></span> |
| <span data-ttu-id="073b2-119">Desligar</span><span class="sxs-lookup"><span data-stu-id="073b2-119">off</span></span>                   | <span data-ttu-id="073b2-120">Desabilita a chave de quebra atual.</span><span class="sxs-lookup"><span data-stu-id="073b2-120">Disables the current break key.</span></span>                                                 |



 

</dd> <dt>

<span data-ttu-id="073b2-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="073b2-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="073b2-122">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="073b2-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="073b2-123">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="073b2-123">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="073b2-124">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="073b2-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="073b2-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="073b2-125">Return Value</span></span>

<span data-ttu-id="073b2-126">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="073b2-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="073b2-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="073b2-127">Remarks</span></span>

<span data-ttu-id="073b2-128">Quando a chave de interrupção é habilitada e o usuário pressiona a chave identificada pelo código de chave virtual especificado no parâmetro *lpszVirtKey* , o dispositivo retorna o controle para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="073b2-128">When the break key is enabled and the user presses the key identified by the virtual-key code specified in the *lpszVirtKey* parameter, the device returns control to the application.</span></span> <span data-ttu-id="073b2-129">Se possível, o comando continua a execução.</span><span class="sxs-lookup"><span data-stu-id="073b2-129">If possible, the command continues execution.</span></span>

## <a name="examples"></a><span data-ttu-id="073b2-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="073b2-130">Examples</span></span>

<span data-ttu-id="073b2-131">O comando a seguir define F2 como a chave de interrupção para o dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="073b2-131">The following command sets F2 as the break key for the "mysound" device.</span></span>

``` syntax
break mysound on 113
```

## <a name="requirements"></a><span data-ttu-id="073b2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="073b2-132">Requirements</span></span>



| <span data-ttu-id="073b2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="073b2-133">Requirement</span></span> | <span data-ttu-id="073b2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="073b2-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="073b2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="073b2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="073b2-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="073b2-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="073b2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="073b2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="073b2-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="073b2-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="073b2-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="073b2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073b2-140">MCI</span><span class="sxs-lookup"><span data-stu-id="073b2-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="073b2-141">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="073b2-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

