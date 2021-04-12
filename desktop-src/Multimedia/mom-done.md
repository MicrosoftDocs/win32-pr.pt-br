---
title: Mensagem de MOM_DONE (Mciapi. h)
description: A \_ mensagem Mom Done é enviada para uma função de retorno de chamada de saída de Midi quando o buffer especificado exclusivo pelo sistema ou fluxo foi reproduzido e está sendo retornado para o aplicativo.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- Multimídia do Windows de mensagem MOM_DONE
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369484"
---
# <a name="mom_done-message"></a><span data-ttu-id="c8af4-104">Mensagem do MOM \_ concluída</span><span class="sxs-lookup"><span data-stu-id="c8af4-104">MOM\_DONE message</span></span>

<span data-ttu-id="c8af4-105">A mensagem **Mom \_ Done** é enviada para uma função de retorno de chamada de saída de Midi quando o buffer especificado exclusivo pelo sistema ou fluxo foi reproduzido e está sendo retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8af4-105">The **MOM\_DONE** message is sent to a MIDI output callback function when the specified system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="c8af4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8af4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8af4-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="c8af4-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="c8af4-108">Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o buffer.</span><span class="sxs-lookup"><span data-stu-id="c8af4-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c8af4-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c8af4-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c8af4-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="c8af4-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8af4-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c8af4-111">Return Value</span></span>

<span data-ttu-id="c8af4-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c8af4-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8af4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8af4-113">Requirements</span></span>



| <span data-ttu-id="c8af4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8af4-114">Requirement</span></span> | <span data-ttu-id="c8af4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c8af4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c8af4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8af4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8af4-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8af4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c8af4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8af4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8af4-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8af4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c8af4-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c8af4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8af4-121"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8af4-121"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8af4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8af4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8af4-123">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="c8af4-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

