---
title: Mensagem de MM_MIXM_LINE_CHANGE (mmsystem. h)
description: A \_ mensagem de alteração de linha MIXM mm \_ \_ é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de uma linha de áudio no dispositivo especificado foi alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para a linha de áudio especificada.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- Multimídia do Windows de mensagem MM_MIXM_LINE_CHANGE
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760413"
---
# <a name="mm_mixm_line_change-message"></a><span data-ttu-id="069af-105">\_Mensagem de \_ alteração de linha MIXM mm \_</span><span class="sxs-lookup"><span data-stu-id="069af-105">MM\_MIXM\_LINE\_CHANGE message</span></span>

<span data-ttu-id="069af-106">A mensagem de **\_ \_ \_ alteração de linha MIXM mm** é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de uma linha de áudio no dispositivo especificado foi alterado.</span><span class="sxs-lookup"><span data-stu-id="069af-106">The **MM\_MIXM\_LINE\_CHANGE** message is sent by a mixer device to notify an application that the state of an audio line on the specified device has changed.</span></span> <span data-ttu-id="069af-107">O aplicativo deve atualizar seus valores de exibição e armazenados em cache para a linha de áudio especificada.</span><span class="sxs-lookup"><span data-stu-id="069af-107">The application should refresh its display and cached values for the specified audio line.</span></span>


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a><span data-ttu-id="069af-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="069af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="069af-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="069af-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="069af-110">Identificador para o dispositivo de mixer que enviou a mensagem de notificação.</span><span class="sxs-lookup"><span data-stu-id="069af-110">Handle to the mixer device that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="069af-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span><span class="sxs-lookup"><span data-stu-id="069af-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span></span>
</dt> <dd>

<span data-ttu-id="069af-112">Identificador de linha para a linha de áudio que tem o estado alterado.</span><span class="sxs-lookup"><span data-stu-id="069af-112">Line identifier for the audio line that has changed state.</span></span> <span data-ttu-id="069af-113">Esse identificador é o mesmo que o membro **dwLineID** da estrutura de **mixer** retornada pela função **mixerGetLineInfo**.</span><span class="sxs-lookup"><span data-stu-id="069af-113">This identifier is the same as the **dwLineID** member of the **MIXERLINE** structure returned by the **mixerGetLineInfo** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="069af-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="069af-114">Remarks</span></span>

<span data-ttu-id="069af-115">Um aplicativo deve abrir um dispositivo de mixer e especificar uma janela de retorno de chamada para receber a mensagem de **\_ \_ \_ alteração de linha MIXM mm** .</span><span class="sxs-lookup"><span data-stu-id="069af-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_LINE\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="069af-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="069af-116">Requirements</span></span>



| <span data-ttu-id="069af-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="069af-117">Requirement</span></span> | <span data-ttu-id="069af-118">Valor</span><span class="sxs-lookup"><span data-stu-id="069af-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="069af-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="069af-119">Minimum supported client</span></span><br/> | <span data-ttu-id="069af-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="069af-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="069af-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="069af-121">Minimum supported server</span></span><br/> | <span data-ttu-id="069af-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="069af-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="069af-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="069af-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="069af-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="069af-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069af-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="069af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069af-126">Mixers de áudio</span><span class="sxs-lookup"><span data-stu-id="069af-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="069af-127">Mensagens do mixer de áudio</span><span class="sxs-lookup"><span data-stu-id="069af-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





