---
title: Mensagem de WIM_DATA (mmsystem. h)
description: A \_ mensagem de dados WIM é enviada para a função de retorno de chamada de entrada de wave-áudio fornecida quando a forma de onda – dados de áudio estão presentes no buffer de entrada e o buffer está sendo retornado para o aplicativo.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- Multimídia do Windows de mensagem WIM_DATA
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770155"
---
# <a name="wim_data-message"></a><span data-ttu-id="76510-104">\_Mensagem de dados wim</span><span class="sxs-lookup"><span data-stu-id="76510-104">WIM\_DATA message</span></span>

<span data-ttu-id="76510-105">A mensagem de **\_ dados wim** é enviada para a função de retorno de chamada de entrada de wave-áudio fornecida quando a forma de onda – dados de áudio estão presentes no buffer de entrada e o buffer está sendo retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="76510-105">The **WIM\_DATA** message is sent to the given waveform-audio input callback function when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="76510-106">A mensagem pode ser enviada quando o buffer está cheio ou depois que a função [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) é chamada.</span><span class="sxs-lookup"><span data-stu-id="76510-106">The message can be sent when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="76510-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76510-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76510-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="76510-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="76510-109">Ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o buffer que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="76510-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="76510-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="76510-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="76510-111">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="76510-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76510-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="76510-112">Return Value</span></span>

<span data-ttu-id="76510-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="76510-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76510-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="76510-114">Remarks</span></span>

<span data-ttu-id="76510-115">O buffer retornado pode não estar cheio.</span><span class="sxs-lookup"><span data-stu-id="76510-115">The returned buffer might not be full.</span></span> <span data-ttu-id="76510-116">Use o membro **dwBytesRecorded** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lpwvhdr* para determinar o número de bytes registrados no buffer retornado.</span><span class="sxs-lookup"><span data-stu-id="76510-116">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lpwvhdr* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="76510-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76510-117">Requirements</span></span>



| <span data-ttu-id="76510-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76510-118">Requirement</span></span> | <span data-ttu-id="76510-119">Valor</span><span class="sxs-lookup"><span data-stu-id="76510-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76510-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76510-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76510-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76510-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="76510-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76510-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76510-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76510-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="76510-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="76510-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76510-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76510-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76510-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="76510-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76510-127">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="76510-127">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="76510-128">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="76510-128">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

