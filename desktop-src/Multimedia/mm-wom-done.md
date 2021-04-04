---
title: Mensagem de MM_WOM_DONE (mmsystem. h)
description: A \_ mensagem mm wom \_ concluído é enviada para uma janela quando o buffer de saída fornecido está sendo retornado para o aplicativo. Os buffers são retornados para o aplicativo quando eles são reproduzidos ou como resultado de uma chamada para a função waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- Multimídia do Windows de mensagem MM_WOM_DONE
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645253"
---
# <a name="mm_wom_done-message"></a><span data-ttu-id="a39b5-105">MM \_ wom de \_ mensagens concluídas</span><span class="sxs-lookup"><span data-stu-id="a39b5-105">MM\_WOM\_DONE message</span></span>

<span data-ttu-id="a39b5-106">A mensagem **mm \_ wom \_ concluído** é enviada para uma janela quando o buffer de saída fornecido está sendo retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a39b5-106">The **MM\_WOM\_DONE** message is sent to a window when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="a39b5-107">Os buffers são retornados para o aplicativo quando eles são reproduzidos ou como resultado de uma chamada para a função [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="a39b5-107">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="a39b5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a39b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a39b5-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="a39b5-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="a39b5-110">Identificador para o dispositivo de saída de wave-áudio que reproduziu o buffer.</span><span class="sxs-lookup"><span data-stu-id="a39b5-110">Handle to the waveform-audio output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a39b5-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="a39b5-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="a39b5-112">Ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) identificando o buffer.</span><span class="sxs-lookup"><span data-stu-id="a39b5-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a39b5-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a39b5-113">Return Value</span></span>

<span data-ttu-id="a39b5-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a39b5-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a39b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a39b5-115">Requirements</span></span>



| <span data-ttu-id="a39b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a39b5-116">Requirement</span></span> | <span data-ttu-id="a39b5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a39b5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39b5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a39b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a39b5-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a39b5-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a39b5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a39b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a39b5-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a39b5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a39b5-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a39b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a39b5-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a39b5-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a39b5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a39b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39b5-125">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="a39b5-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="a39b5-126">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="a39b5-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

