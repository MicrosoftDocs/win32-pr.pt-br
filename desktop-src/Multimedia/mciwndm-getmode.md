---
title: Mensagem de MCIWNDM_GETMODE (VFW. h)
description: A \_ mensagem MCIWNDM GetMode recupera o modo de operação atual de um dispositivo MCI. Os dispositivos MCI têm vários modos de operação, que são designados por constantes. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETMODE
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085144"
---
# <a name="mciwndm_getmode-message"></a><span data-ttu-id="716a3-106">\_Mensagem MCIWNDM GETmode</span><span class="sxs-lookup"><span data-stu-id="716a3-106">MCIWNDM\_GETMODE message</span></span>

<span data-ttu-id="716a3-107">A mensagem **MCIWNDM \_ GetMode** recupera o modo de operação atual de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="716a3-107">The **MCIWNDM\_GETMODE** message retrieves the current operating mode of an MCI device.</span></span> <span data-ttu-id="716a3-108">Os dispositivos MCI têm vários modos de operação, que são designados por constantes.</span><span class="sxs-lookup"><span data-stu-id="716a3-108">MCI devices have several operating modes, which are designated by constants.</span></span> <span data-ttu-id="716a3-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .</span><span class="sxs-lookup"><span data-stu-id="716a3-109">You can send this message explicitly or by using the [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) macro.</span></span>


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="716a3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="716a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716a3-111"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="716a3-111"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="716a3-112">Tamanho, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="716a3-112">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="716a3-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="716a3-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="716a3-114">Ponteiro para o buffer definido pelo aplicativo usado para retornar o modo.</span><span class="sxs-lookup"><span data-stu-id="716a3-114">Pointer to the application-defined buffer used to return the mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="716a3-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="716a3-115">Return Value</span></span>

<span data-ttu-id="716a3-116">Retorna um inteiro correspondente à constante MCI que define o modo.</span><span class="sxs-lookup"><span data-stu-id="716a3-116">Returns an integer corresponding to the MCI constant defining the mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="716a3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="716a3-117">Remarks</span></span>

<span data-ttu-id="716a3-118">Se a cadeia de caracteres terminada em nulo que descreve o modo for maior que o buffer, ela será truncada.</span><span class="sxs-lookup"><span data-stu-id="716a3-118">If the null-terminated string describing the mode is longer than the buffer, it is truncated.</span></span>

<span data-ttu-id="716a3-119">Nem todos os dispositivos podem operar em todos os modos.</span><span class="sxs-lookup"><span data-stu-id="716a3-119">Not all devices can operate in every mode.</span></span> <span data-ttu-id="716a3-120">Por exemplo, o dispositivo MCIAVI é um dispositivo de reprodução; Ele não dá suporte ao modo de gravação.</span><span class="sxs-lookup"><span data-stu-id="716a3-120">For example, the MCIAVI device is a playback device; it doesn't support the recording mode.</span></span> <span data-ttu-id="716a3-121">Os modos a seguir podem ser recuperados usando **MCIWNDM \_ GetMode**.</span><span class="sxs-lookup"><span data-stu-id="716a3-121">The following modes can be retrieved by using **MCIWNDM\_GETMODE**.</span></span>



| <span data-ttu-id="716a3-122">Modo de operação</span><span class="sxs-lookup"><span data-stu-id="716a3-122">Operating mode</span></span> | <span data-ttu-id="716a3-123">Constante MCI</span><span class="sxs-lookup"><span data-stu-id="716a3-123">MCI constant</span></span>          |
|----------------|-----------------------|
| <span data-ttu-id="716a3-124">Não está pronto</span><span class="sxs-lookup"><span data-stu-id="716a3-124">not ready</span></span>      | <span data-ttu-id="716a3-125">\_modo MCI \_ não \_ está pronto</span><span class="sxs-lookup"><span data-stu-id="716a3-125">MCI\_MODE\_NOT\_READY</span></span> |
| <span data-ttu-id="716a3-126">Abrir</span><span class="sxs-lookup"><span data-stu-id="716a3-126">open</span></span>           | <span data-ttu-id="716a3-127">\_modo MCI \_ aberto</span><span class="sxs-lookup"><span data-stu-id="716a3-127">MCI\_MODE\_OPEN</span></span>       |
| <span data-ttu-id="716a3-128">pausado</span><span class="sxs-lookup"><span data-stu-id="716a3-128">paused</span></span>         | <span data-ttu-id="716a3-129">\_pausa no modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="716a3-129">MCI\_MODE\_PAUSE</span></span>      |
| <span data-ttu-id="716a3-130">reproduzindo</span><span class="sxs-lookup"><span data-stu-id="716a3-130">playing</span></span>        | <span data-ttu-id="716a3-131">\_reprodução do modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="716a3-131">MCI\_MODE\_PLAY</span></span>       |
| <span data-ttu-id="716a3-132">gravação</span><span class="sxs-lookup"><span data-stu-id="716a3-132">recording</span></span>      | <span data-ttu-id="716a3-133">\_registro do modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="716a3-133">MCI\_MODE\_RECORD</span></span>     |
| <span data-ttu-id="716a3-134">buscando</span><span class="sxs-lookup"><span data-stu-id="716a3-134">seeking</span></span>        | <span data-ttu-id="716a3-135">\_modo MCI \_ Seek</span><span class="sxs-lookup"><span data-stu-id="716a3-135">MCI\_MODE\_SEEK</span></span>       |
| <span data-ttu-id="716a3-136">interrompido</span><span class="sxs-lookup"><span data-stu-id="716a3-136">stopped</span></span>        | <span data-ttu-id="716a3-137">\_parada do modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="716a3-137">MCI\_MODE\_STOP</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="716a3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="716a3-138">Requirements</span></span>



| <span data-ttu-id="716a3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="716a3-139">Requirement</span></span> | <span data-ttu-id="716a3-140">Valor</span><span class="sxs-lookup"><span data-stu-id="716a3-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="716a3-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="716a3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="716a3-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="716a3-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="716a3-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="716a3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="716a3-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="716a3-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="716a3-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="716a3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="716a3-146"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="716a3-146"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="716a3-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="716a3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716a3-148">**MCIWndGetMode**</span><span class="sxs-lookup"><span data-stu-id="716a3-148">**MCIWndGetMode**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





