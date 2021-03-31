---
title: comando SetCode
description: O comando SetCode habilita ou desabilita a gravação do código de ponto para um videocassete. Os dispositivos VCR reconhecem este comando.
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- Multimídia do Windows do comando SetCode
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32092e5af7c77cdc274491b20663218d39a1ec1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645250"
---
# <a name="settimecode-command"></a><span data-ttu-id="d1e79-105">comando SetCode</span><span class="sxs-lookup"><span data-stu-id="d1e79-105">settimecode command</span></span>

<span data-ttu-id="d1e79-106">O comando SetCode habilita ou desabilita a gravação do código de ponto para um videocassete.</span><span class="sxs-lookup"><span data-stu-id="d1e79-106">The settimecode command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="d1e79-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="d1e79-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="d1e79-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="d1e79-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d1e79-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1e79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e79-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d1e79-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d1e79-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d1e79-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d1e79-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="d1e79-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d1e79-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span><span class="sxs-lookup"><span data-stu-id="d1e79-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span></span>
</dt> <dd>

<span data-ttu-id="d1e79-114">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1e79-114">One of the following flags.</span></span>



| <span data-ttu-id="d1e79-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d1e79-115">Value</span></span>      | <span data-ttu-id="d1e79-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d1e79-116">Meaning</span></span>                          |
|------------|----------------------------------|
| <span data-ttu-id="d1e79-117">gravar em</span><span class="sxs-lookup"><span data-stu-id="d1e79-117">record on</span></span>  | <span data-ttu-id="d1e79-118">Define o VCR para registrar o código de linhas.</span><span class="sxs-lookup"><span data-stu-id="d1e79-118">Sets the VCR to record timecode.</span></span> |
| <span data-ttu-id="d1e79-119">registro desativado</span><span class="sxs-lookup"><span data-stu-id="d1e79-119">record off</span></span> | <span data-ttu-id="d1e79-120">Desabilita a gravação do código de ponto.</span><span class="sxs-lookup"><span data-stu-id="d1e79-120">Disables timecode recording.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d1e79-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d1e79-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d1e79-122">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="d1e79-122">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="d1e79-123">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d1e79-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e79-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d1e79-124">Return Value</span></span>

<span data-ttu-id="d1e79-125">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="d1e79-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e79-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1e79-126">Requirements</span></span>



| <span data-ttu-id="d1e79-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e79-127">Requirement</span></span> | <span data-ttu-id="d1e79-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d1e79-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d1e79-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1e79-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e79-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1e79-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d1e79-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1e79-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e79-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1e79-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d1e79-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d1e79-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e79-134">MCI</span><span class="sxs-lookup"><span data-stu-id="d1e79-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d1e79-135">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="d1e79-135">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

