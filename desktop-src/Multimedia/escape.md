---
title: comando de escape
description: O comando de escape envia informações específicas do dispositivo para um dispositivo. Os dispositivos VIDEODISC reconhecem este comando.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- Multimídia do Windows de comando de escape
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105747515"
---
# <a name="escape-command"></a><span data-ttu-id="f3c63-105">comando de escape</span><span class="sxs-lookup"><span data-stu-id="f3c63-105">escape command</span></span>

<span data-ttu-id="f3c63-106">O comando de escape envia informações específicas do dispositivo para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c63-106">The escape command sends device-specific information to a device.</span></span> <span data-ttu-id="f3c63-107">Os dispositivos VIDEODISC reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f3c63-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="f3c63-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f3c63-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f3c63-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3c63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3c63-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f3c63-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f3c63-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f3c63-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f3c63-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="f3c63-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f3c63-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span><span class="sxs-lookup"><span data-stu-id="f3c63-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span></span>
</dt> <dd>

<span data-ttu-id="f3c63-114">Informações personalizadas a serem enviadas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c63-114">Custom information to send to the device.</span></span>

</dd> <dt>

<span data-ttu-id="f3c63-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f3c63-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f3c63-116">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="f3c63-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f3c63-117">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f3c63-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3c63-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f3c63-118">Return Value</span></span>

<span data-ttu-id="f3c63-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f3c63-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="f3c63-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3c63-120">Examples</span></span>

<span data-ttu-id="f3c63-121">O comando a seguir envia a cadeia de caracteres de escape "SA" para o dispositivo VIDEODISC.</span><span class="sxs-lookup"><span data-stu-id="f3c63-121">The following command sends the escape string "SA" to the videodisc device.</span></span>

``` syntax
escape videodisc SA
```

## <a name="requirements"></a><span data-ttu-id="f3c63-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3c63-122">Requirements</span></span>



| <span data-ttu-id="f3c63-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3c63-123">Requirement</span></span> | <span data-ttu-id="f3c63-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f3c63-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f3c63-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3c63-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c63-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3c63-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f3c63-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3c63-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c63-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3c63-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f3c63-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3c63-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c63-130">MCI</span><span class="sxs-lookup"><span data-stu-id="f3c63-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f3c63-131">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="f3c63-131">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

