---
title: Mensagem de MCIWNDM_SETREPEAT (VFW. h)
description: A \_ mensagem MCIWNDM setrepetir define o sinalizador de repetição associado à reprodução contínua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETREPEAT
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824578"
---
# <a name="mciwndm_setrepeat-message"></a><span data-ttu-id="9dbd0-104">MCIWNDM \_ AutoRepetir mensagem</span><span class="sxs-lookup"><span data-stu-id="9dbd0-104">MCIWNDM\_SETREPEAT message</span></span>

<span data-ttu-id="9dbd0-105">A mensagem **MCIWNDM \_ setrepetir** define o sinalizador de repetição associado à reprodução contínua.</span><span class="sxs-lookup"><span data-stu-id="9dbd0-105">The **MCIWNDM\_SETREPEAT** message sets the repeat flag associated with continuous playback.</span></span> <span data-ttu-id="9dbd0-106">A mensagem **MCIWNDM \_ setrepetir** funciona em conjunto com o comando [MCI \_ Play](mci-play.md) para fornecer um loop de reprodução contínua.</span><span class="sxs-lookup"><span data-stu-id="9dbd0-106">The **MCIWNDM\_SETREPEAT** message works in conjunction with the [MCI\_PLAY](mci-play.md) command to provide a continuous playback loop.</span></span> <span data-ttu-id="9dbd0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="9dbd0-107">You can send this message explicitly or by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro.</span></span>


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a><span data-ttu-id="9dbd0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9dbd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dbd0-109"><span id="f"></span><span id="F"></span>*fixo*</span><span class="sxs-lookup"><span data-stu-id="9dbd0-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="9dbd0-110">Novo estado do sinalizador de repetição.</span><span class="sxs-lookup"><span data-stu-id="9dbd0-110">New state of the repeat flag.</span></span> <span data-ttu-id="9dbd0-111">Especifique **true** para ativar a reprodução contínua.</span><span class="sxs-lookup"><span data-stu-id="9dbd0-111">Specify **TRUE** to turn on continuous playback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dbd0-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9dbd0-112">Return Value</span></span>

<span data-ttu-id="9dbd0-113">Retorna zero.</span><span class="sxs-lookup"><span data-stu-id="9dbd0-113">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dbd0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dbd0-114">Remarks</span></span>

<span data-ttu-id="9dbd0-115">Atualmente, MCIAVI é o único dispositivo que dá suporte à reprodução contínua.</span><span class="sxs-lookup"><span data-stu-id="9dbd0-115">Currently, MCIAVI is the only device that supports continuous playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dbd0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dbd0-116">Requirements</span></span>



| <span data-ttu-id="9dbd0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dbd0-117">Requirement</span></span> | <span data-ttu-id="9dbd0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9dbd0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9dbd0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dbd0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9dbd0-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9dbd0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9dbd0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dbd0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9dbd0-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9dbd0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9dbd0-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9dbd0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dbd0-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dbd0-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dbd0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dbd0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dbd0-126">\_reprodução MCI</span><span class="sxs-lookup"><span data-stu-id="9dbd0-126">MCI\_PLAY</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="9dbd0-127">**MCIWndSetRepeat**</span><span class="sxs-lookup"><span data-stu-id="9dbd0-127">**MCIWndSetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





