---
title: Mensagem de MM_MOM_DONE (mmsystem. h)
description: A \_ mensagem mm Mom \_ Done é enviada para uma janela quando o buffer especificado de fluxo de sistema/exclusivo do Midi foi reproduzido e está sendo retornado para o aplicativo.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- Multimídia do Windows de mensagem MM_MOM_DONE
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008972"
---
# <a name="mm_mom_done-message"></a><span data-ttu-id="31f43-104">\_Mensagem mm Mom \_ concluído</span><span class="sxs-lookup"><span data-stu-id="31f43-104">MM\_MOM\_DONE message</span></span>

<span data-ttu-id="31f43-105">A mensagem **mm \_ Mom \_ Done** é enviada para uma janela quando o buffer especificado de fluxo de sistema/exclusivo do Midi foi reproduzido e está sendo retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31f43-105">The **MM\_MOM\_DONE** message is sent to a window when the specified MIDI system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="31f43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31f43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31f43-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="31f43-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="31f43-108">Identificador para o dispositivo de saída de MIDI que reproduziu o buffer.</span><span class="sxs-lookup"><span data-stu-id="31f43-108">Handle to the MIDI output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31f43-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="31f43-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="31f43-110">Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o buffer.</span><span class="sxs-lookup"><span data-stu-id="31f43-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31f43-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="31f43-111">Return Value</span></span>

<span data-ttu-id="31f43-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="31f43-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="31f43-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f43-113">Requirements</span></span>



| <span data-ttu-id="31f43-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f43-114">Requirement</span></span> | <span data-ttu-id="31f43-115">Valor</span><span class="sxs-lookup"><span data-stu-id="31f43-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f43-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31f43-116">Minimum supported client</span></span><br/> | <span data-ttu-id="31f43-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31f43-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="31f43-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31f43-118">Minimum supported server</span></span><br/> | <span data-ttu-id="31f43-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31f43-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="31f43-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31f43-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="31f43-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31f43-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f43-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="31f43-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f43-123">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="31f43-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

