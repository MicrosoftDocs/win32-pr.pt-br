---
title: comando de índice
description: O comando index controla a exibição na tela de um videocassete. Os dispositivos VCR reconhecem este comando.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- comando de índice multimídia do Windows
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919217"
---
# <a name="index-command"></a><span data-ttu-id="70877-105">comando de índice</span><span class="sxs-lookup"><span data-stu-id="70877-105">index command</span></span>

<span data-ttu-id="70877-106">O comando index controla a exibição na tela de um videocassete.</span><span class="sxs-lookup"><span data-stu-id="70877-106">The index command controls a VCR's on-screen display.</span></span> <span data-ttu-id="70877-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="70877-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="70877-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="70877-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="70877-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70877-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70877-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="70877-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="70877-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="70877-111">Identifier of an MCI device.</span></span> <span data-ttu-id="70877-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="70877-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="70877-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span><span class="sxs-lookup"><span data-stu-id="70877-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span></span>
</dt> <dd>

<span data-ttu-id="70877-114">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="70877-114">One of the following flags.</span></span>



| <span data-ttu-id="70877-115">Valor</span><span class="sxs-lookup"><span data-stu-id="70877-115">Value</span></span> | <span data-ttu-id="70877-116">Significado</span><span class="sxs-lookup"><span data-stu-id="70877-116">Meaning</span></span>                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70877-117">Desligar</span><span class="sxs-lookup"><span data-stu-id="70877-117">off</span></span>   | <span data-ttu-id="70877-118">Desativa a exibição na tela.</span><span class="sxs-lookup"><span data-stu-id="70877-118">Turns off the on-screen display.</span></span>                                                                                         |
| <span data-ttu-id="70877-119">on</span><span class="sxs-lookup"><span data-stu-id="70877-119">on</span></span>    | <span data-ttu-id="70877-120">Ativa a exibição na tela.</span><span class="sxs-lookup"><span data-stu-id="70877-120">Turns on the on-screen display.</span></span> <span data-ttu-id="70877-121">O item a ser exibido é especificado pelo sinalizador "index" do comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="70877-121">The item to be displayed is specified by the "index" flag of the [set](set.md) command.</span></span> |



 

</dd> <dt>

<span data-ttu-id="70877-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="70877-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="70877-123">Pode ser "Wait", "Notify" ou "Test".</span><span class="sxs-lookup"><span data-stu-id="70877-123">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="70877-124">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="70877-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70877-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="70877-125">Return Value</span></span>

<span data-ttu-id="70877-126">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="70877-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="70877-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70877-127">Requirements</span></span>



| <span data-ttu-id="70877-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="70877-128">Requirement</span></span> | <span data-ttu-id="70877-129">Valor</span><span class="sxs-lookup"><span data-stu-id="70877-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="70877-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70877-130">Minimum supported client</span></span><br/> | <span data-ttu-id="70877-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="70877-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="70877-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70877-132">Minimum supported server</span></span><br/> | <span data-ttu-id="70877-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="70877-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="70877-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="70877-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70877-135">MCI</span><span class="sxs-lookup"><span data-stu-id="70877-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="70877-136">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="70877-136">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="70877-137">set</span><span class="sxs-lookup"><span data-stu-id="70877-137">set</span></span>](set.md)
</dt> </dl>

 

