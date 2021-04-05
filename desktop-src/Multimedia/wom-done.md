---
title: Mensagem de WOM_DONE (mmsystem. h)
description: A \_ mensagem wom feita é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando o buffer de saída fornecido está sendo retornado para o aplicativo.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- Multimídia do Windows de mensagem WOM_DONE
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085236"
---
# <a name="wom_done-message"></a><span data-ttu-id="d4c92-104">\_Mensagem wom concluída</span><span class="sxs-lookup"><span data-stu-id="d4c92-104">WOM\_DONE message</span></span>

<span data-ttu-id="d4c92-105">A mensagem **wom \_ feita** é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando o buffer de saída fornecido está sendo retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4c92-105">The **WOM\_DONE** message is sent to a waveform-audio output callback function when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="d4c92-106">Os buffers são retornados para o aplicativo quando eles são reproduzidos ou como resultado de uma chamada para a função [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="d4c92-106">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="d4c92-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4c92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c92-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d4c92-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d4c92-109">Ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) identificando o buffer.</span><span class="sxs-lookup"><span data-stu-id="d4c92-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d4c92-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d4c92-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d4c92-111">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d4c92-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c92-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d4c92-112">Return Value</span></span>

<span data-ttu-id="d4c92-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d4c92-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4c92-114">Requirements</span></span>



| <span data-ttu-id="d4c92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c92-115">Requirement</span></span> | <span data-ttu-id="d4c92-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d4c92-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c92-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4c92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c92-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4c92-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d4c92-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4c92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c92-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4c92-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4c92-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d4c92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c92-122"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4c92-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c92-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4c92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c92-124">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="d4c92-124">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="d4c92-125">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="d4c92-125">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

