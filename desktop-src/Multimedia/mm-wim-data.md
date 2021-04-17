---
title: Mensagem de MM_WIM_DATA (mmsystem. h)
description: A \_ mensagem de \_ dados wim mm é enviada para uma janela quando a onda de dados de áudio está presente no buffer de entrada e o buffer está sendo retornado para o aplicativo. A mensagem pode ser enviada quando o buffer está cheio ou depois que a função waveInReset é chamada.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- Multimídia do Windows de mensagem MM_WIM_DATA
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779395"
---
# <a name="mm_wim_data-message"></a><span data-ttu-id="14a16-105">MM \_ \_ mensagem de dados wim</span><span class="sxs-lookup"><span data-stu-id="14a16-105">MM\_WIM\_DATA message</span></span>

<span data-ttu-id="14a16-106">A mensagem de **\_ \_ dados wim mm** é enviada para uma janela quando a onda de dados de áudio está presente no buffer de entrada e o buffer está sendo retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14a16-106">The **MM\_WIM\_DATA** message is sent to a window when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="14a16-107">A mensagem pode ser enviada quando o buffer está cheio ou depois que a função [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) é chamada.</span><span class="sxs-lookup"><span data-stu-id="14a16-107">The message can be sent either when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="14a16-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14a16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a16-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="14a16-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="14a16-110">Identificador para o dispositivo de entrada de wave-áudio que recebeu os dados.</span><span class="sxs-lookup"><span data-stu-id="14a16-110">Handle to the waveform-audio input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="14a16-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="14a16-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="14a16-112">Ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o buffer que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="14a16-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a16-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="14a16-113">Return Value</span></span>

<span data-ttu-id="14a16-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="14a16-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14a16-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="14a16-115">Remarks</span></span>

<span data-ttu-id="14a16-116">O buffer retornado pode não estar cheio.</span><span class="sxs-lookup"><span data-stu-id="14a16-116">The returned buffer might not be full.</span></span> <span data-ttu-id="14a16-117">Use o membro **dwBytesRecorded** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lParam* para determinar o número de bytes gravados no buffer retornado.</span><span class="sxs-lookup"><span data-stu-id="14a16-117">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lParam* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a16-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a16-118">Requirements</span></span>



| <span data-ttu-id="14a16-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a16-119">Requirement</span></span> | <span data-ttu-id="14a16-120">Valor</span><span class="sxs-lookup"><span data-stu-id="14a16-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a16-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14a16-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14a16-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14a16-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="14a16-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14a16-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14a16-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14a16-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="14a16-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="14a16-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14a16-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14a16-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a16-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="14a16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a16-128">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="14a16-128">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="14a16-129">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="14a16-129">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

