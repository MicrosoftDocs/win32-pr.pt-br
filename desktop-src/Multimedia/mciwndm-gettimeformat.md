---
title: Mensagem de MCIWNDM_GETTIMEFORMAT (VFW. h)
description: A \_ mensagem MCIWNDM GETTIMEFORMAT recupera o formato de hora atual de um dispositivo MCI em dois formulários como um valor numérico e como uma cadeia de caracteres. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETTIMEFORMAT
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644334"
---
# <a name="mciwndm_gettimeformat-message"></a><span data-ttu-id="ab977-105">\_Mensagem MCIWNDM GETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="ab977-105">MCIWNDM\_GETTIMEFORMAT message</span></span>

<span data-ttu-id="ab977-106">A mensagem **MCIWNDM \_ GETTIMEFORMAT** recupera o formato de hora atual de um dispositivo MCI em duas formas: como um valor numérico e uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ab977-106">The **MCIWNDM\_GETTIMEFORMAT** message retrieves the current time format of an MCI device in two forms: as a numerical value and as a string.</span></span> <span data-ttu-id="ab977-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ab977-107">You can send this message explicitly or by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="ab977-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab977-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab977-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="ab977-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="ab977-110">Tamanho, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="ab977-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ab977-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="ab977-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="ab977-112">Ponteiro para um buffer para conter a forma de cadeia de caracteres terminada em nulo do formato de hora.</span><span class="sxs-lookup"><span data-stu-id="ab977-112">Pointer to a buffer to contain the null-terminated string form of the time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab977-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ab977-113">Return Value</span></span>

<span data-ttu-id="ab977-114">Retorna um inteiro correspondente à constante MCI que define o formato de hora.</span><span class="sxs-lookup"><span data-stu-id="ab977-114">Returns an integer corresponding to the MCI constant defining the time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab977-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab977-115">Remarks</span></span>

<span data-ttu-id="ab977-116">Se a cadeia de caracteres de formato de hora for maior do que o buffer de retorno, MCIWnd truncará a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ab977-116">If the time format string is longer than the return buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="ab977-117">Um dispositivo MCI pode dar suporte a um ou mais dos seguintes formatos de hora.</span><span class="sxs-lookup"><span data-stu-id="ab977-117">An MCI device can support one or more of the following time formats.</span></span>



| <span data-ttu-id="ab977-118">Formato de hora</span><span class="sxs-lookup"><span data-stu-id="ab977-118">Time format</span></span>                      | <span data-ttu-id="ab977-119">Constante MCI</span><span class="sxs-lookup"><span data-stu-id="ab977-119">MCI constant</span></span>               |
|----------------------------------|----------------------------|
| <span data-ttu-id="ab977-120">Bytes</span><span class="sxs-lookup"><span data-stu-id="ab977-120">Bytes</span></span>                            | <span data-ttu-id="ab977-121">\_bytes de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="ab977-121">MCI\_FORMAT\_BYTES</span></span>         |
| <span data-ttu-id="ab977-122">Intervalos</span><span class="sxs-lookup"><span data-stu-id="ab977-122">Frames</span></span>                           | <span data-ttu-id="ab977-123">\_quadros de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="ab977-123">MCI\_FORMAT\_FRAMES</span></span>        |
| <span data-ttu-id="ab977-124">Horas, minutos, segundos</span><span class="sxs-lookup"><span data-stu-id="ab977-124">Hours, minutes, seconds</span></span>          | <span data-ttu-id="ab977-125">\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="ab977-125">MCI\_FORMAT\_HMS</span></span>           |
| <span data-ttu-id="ab977-126">Milissegundos</span><span class="sxs-lookup"><span data-stu-id="ab977-126">Milliseconds</span></span>                     | <span data-ttu-id="ab977-127">\_milissegundos do formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="ab977-127">MCI\_FORMAT\_MILLISECONDS</span></span>  |
| <span data-ttu-id="ab977-128">Minutos, segundos, quadros</span><span class="sxs-lookup"><span data-stu-id="ab977-128">Minutes, seconds, frames</span></span>         | <span data-ttu-id="ab977-129">\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="ab977-129">MCI\_FORMAT\_MSF</span></span>           |
| <span data-ttu-id="ab977-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab977-130">Samples</span></span>                          | <span data-ttu-id="ab977-131">\_exemplos de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="ab977-131">MCI\_FORMAT\_SAMPLES</span></span>       |
| <span data-ttu-id="ab977-132">SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="ab977-132">SMPTE 24</span></span>                         | <span data-ttu-id="ab977-133">\_Formato MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="ab977-133">MCI\_FORMAT\_SMPTE\_24</span></span>     |
| <span data-ttu-id="ab977-134">SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="ab977-134">SMPTE 25</span></span>                         | <span data-ttu-id="ab977-135">\_Formato MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="ab977-135">MCI\_FORMAT\_SMPTE\_25</span></span>     |
| <span data-ttu-id="ab977-136">Remoção de 30 do SMPTE</span><span class="sxs-lookup"><span data-stu-id="ab977-136">SMPTE 30 drop</span></span>                    | <span data-ttu-id="ab977-137">\_Formato MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="ab977-137">MCI\_FORMAT\_SMPTE\_30DROP</span></span> |
| <span data-ttu-id="ab977-138">SMPTE 30 (não descartar)</span><span class="sxs-lookup"><span data-stu-id="ab977-138">SMPTE 30 (non-drop)</span></span>              | <span data-ttu-id="ab977-139">\_Formato MCI \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="ab977-139">MCI\_FORMAT\_SMPTE\_30</span></span>     |
| <span data-ttu-id="ab977-140">Faixas, minutos, segundos, quadros</span><span class="sxs-lookup"><span data-stu-id="ab977-140">Tracks, minutes, seconds, frames</span></span> | <span data-ttu-id="ab977-141">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="ab977-141">MCI\_FORMAT\_TMSF</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="ab977-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab977-142">Requirements</span></span>



| <span data-ttu-id="ab977-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab977-143">Requirement</span></span> | <span data-ttu-id="ab977-144">Valor</span><span class="sxs-lookup"><span data-stu-id="ab977-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab977-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab977-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ab977-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab977-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab977-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab977-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ab977-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab977-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab977-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ab977-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab977-150"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab977-150"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab977-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab977-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab977-152">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ab977-152">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





