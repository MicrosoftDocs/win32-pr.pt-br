---
title: comando de rotação
description: O comando de rotação começa a girar um disco ou interrompe a rotação do disco. Os dispositivos VIDEODISC reconhecem este comando.
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- Multimídia do Windows de comando de rotação
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812898"
---
# <a name="spin-command"></a><span data-ttu-id="50bfd-105">comando de rotação</span><span class="sxs-lookup"><span data-stu-id="50bfd-105">spin command</span></span>

<span data-ttu-id="50bfd-106">O comando de rotação começa a girar um disco ou interrompe a rotação do disco.</span><span class="sxs-lookup"><span data-stu-id="50bfd-106">The spin command starts spinning a disc or stops the disc from spinning.</span></span> <span data-ttu-id="50bfd-107">Os dispositivos VIDEODISC reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="50bfd-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="50bfd-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="50bfd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="50bfd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50bfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50bfd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="50bfd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="50bfd-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="50bfd-111">Identifier of an MCI device.</span></span> <span data-ttu-id="50bfd-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="50bfd-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="50bfd-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span><span class="sxs-lookup"><span data-stu-id="50bfd-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span></span>
</dt> <dd>

<span data-ttu-id="50bfd-114">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="50bfd-114">One of the following flags.</span></span>



| <span data-ttu-id="50bfd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="50bfd-115">Value</span></span> | <span data-ttu-id="50bfd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="50bfd-116">Meaning</span></span>                       |
|-------|-------------------------------|
| <span data-ttu-id="50bfd-117">ligar</span><span class="sxs-lookup"><span data-stu-id="50bfd-117">down</span></span>  | <span data-ttu-id="50bfd-118">Interrompe a rotação do disco.</span><span class="sxs-lookup"><span data-stu-id="50bfd-118">Stops the disc from spinning.</span></span> |
| <span data-ttu-id="50bfd-119">ativo</span><span class="sxs-lookup"><span data-stu-id="50bfd-119">up</span></span>    | <span data-ttu-id="50bfd-120">Inicia a rotação do disco.</span><span class="sxs-lookup"><span data-stu-id="50bfd-120">Starts spinning the disc.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="50bfd-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="50bfd-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="50bfd-122">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="50bfd-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="50bfd-123">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="50bfd-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50bfd-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="50bfd-124">Return Value</span></span>

<span data-ttu-id="50bfd-125">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="50bfd-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="50bfd-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50bfd-126">Examples</span></span>

<span data-ttu-id="50bfd-127">O comando a seguir inicia a rotação de um dispositivo VIDEODISC.</span><span class="sxs-lookup"><span data-stu-id="50bfd-127">The following command starts spinning a videodisc device.</span></span>

``` syntax
spin videodisc up
```

## <a name="requirements"></a><span data-ttu-id="50bfd-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50bfd-128">Requirements</span></span>



| <span data-ttu-id="50bfd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="50bfd-129">Requirement</span></span> | <span data-ttu-id="50bfd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="50bfd-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="50bfd-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50bfd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="50bfd-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50bfd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="50bfd-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50bfd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="50bfd-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50bfd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="50bfd-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="50bfd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50bfd-136">MCI</span><span class="sxs-lookup"><span data-stu-id="50bfd-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="50bfd-137">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="50bfd-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

