---
title: Configurar comando
description: O comando configurar exibe uma caixa de diálogo usada para configurar o dispositivo. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 17d99992-f432-4b8a-ae98-2a70637c29c3
keywords:
- configurar o comando multimídia do Windows
topic_type:
- apiref
api_name:
- configure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f131159d389577e3c717e5630633bb46558d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644234"
---
# <a name="configure-command"></a><span data-ttu-id="3bd69-105">Configurar comando</span><span class="sxs-lookup"><span data-stu-id="3bd69-105">configure command</span></span>

<span data-ttu-id="3bd69-106">O comando configurar exibe uma caixa de diálogo usada para configurar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3bd69-106">The configure command displays a dialog box used to configure the device.</span></span> <span data-ttu-id="3bd69-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="3bd69-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="3bd69-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="3bd69-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("configure %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3bd69-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bd69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd69-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3bd69-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3bd69-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3bd69-111">Identifier of an MCI device.</span></span> <span data-ttu-id="3bd69-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="3bd69-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3bd69-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3bd69-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3bd69-114">Pode ser "Wait", "Notify" ou "Test".</span><span class="sxs-lookup"><span data-stu-id="3bd69-114">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="3bd69-115">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3bd69-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd69-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3bd69-116">Return Value</span></span>

<span data-ttu-id="3bd69-117">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3bd69-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd69-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bd69-118">Requirements</span></span>



| <span data-ttu-id="3bd69-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bd69-119">Requirement</span></span> | <span data-ttu-id="3bd69-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3bd69-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3bd69-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bd69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3bd69-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3bd69-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3bd69-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bd69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3bd69-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3bd69-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3bd69-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bd69-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd69-126">MCI</span><span class="sxs-lookup"><span data-stu-id="3bd69-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3bd69-127">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="3bd69-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

