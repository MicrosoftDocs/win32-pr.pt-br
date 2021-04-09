---
title: comando desfazer
description: O comando desfazer reverte a ação realizada pelo comando copiar, recortar, excluir, desfazer ou colar bem-sucedido mais recente. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- comando desfazer multimídia do Windows
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009733"
---
# <a name="undo-command"></a><span data-ttu-id="41b2f-105">comando desfazer</span><span class="sxs-lookup"><span data-stu-id="41b2f-105">undo command</span></span>

<span data-ttu-id="41b2f-106">O comando desfazer reverte a ação realizada pelo comando [copiar](copy.md), [recortar](cut.md), [excluir](delete.md), desfazer ou [colar](paste.md) bem-sucedido mais recente.</span><span class="sxs-lookup"><span data-stu-id="41b2f-106">The undo command reverses the action taken by the most recent successful [copy](copy.md), [cut](cut.md), [delete](delete.md), undo, or [paste](paste.md) command.</span></span> <span data-ttu-id="41b2f-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="41b2f-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="41b2f-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="41b2f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="41b2f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41b2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b2f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="41b2f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="41b2f-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="41b2f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="41b2f-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="41b2f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="41b2f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="41b2f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="41b2f-114">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="41b2f-114">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="41b2f-115">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="41b2f-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b2f-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="41b2f-116">Return Value</span></span>

<span data-ttu-id="41b2f-117">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="41b2f-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b2f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41b2f-118">Requirements</span></span>



| <span data-ttu-id="41b2f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="41b2f-119">Requirement</span></span> | <span data-ttu-id="41b2f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="41b2f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="41b2f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41b2f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41b2f-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41b2f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="41b2f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41b2f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41b2f-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41b2f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="41b2f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="41b2f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b2f-126">MCI</span><span class="sxs-lookup"><span data-stu-id="41b2f-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="41b2f-127">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="41b2f-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="41b2f-128">copy</span><span class="sxs-lookup"><span data-stu-id="41b2f-128">copy</span></span>](copy.md)
</dt> <dt>

[<span data-ttu-id="41b2f-129">migração</span><span class="sxs-lookup"><span data-stu-id="41b2f-129">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="41b2f-130">delete</span><span class="sxs-lookup"><span data-stu-id="41b2f-130">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="41b2f-131">Olar</span><span class="sxs-lookup"><span data-stu-id="41b2f-131">paste</span></span>](paste.md)
</dt> </dl>

 

