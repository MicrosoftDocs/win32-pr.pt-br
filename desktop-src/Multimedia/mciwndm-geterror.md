---
title: Mensagem de MCIWNDM_GETERROR (VFW. h)
description: A \_ mensagem GETerror MCIWNDM recupera o último erro MCI encontrado. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETERROR
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824219"
---
# <a name="mciwndm_geterror-message"></a><span data-ttu-id="8e971-105">\_Mensagem GETerror MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="8e971-105">MCIWNDM\_GETERROR message</span></span>

<span data-ttu-id="8e971-106">A **mensagem \_ GetError MCIWNDM** recupera o último erro MCI encontrado.</span><span class="sxs-lookup"><span data-stu-id="8e971-106">The **MCIWNDM\_GETERROR** message retrieves the last MCI error encountered.</span></span> <span data-ttu-id="8e971-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="8e971-107">You can send this message explicitly or by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span>


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="8e971-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e971-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e971-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="8e971-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="8e971-110">Tamanho, em bytes, do buffer de erro.</span><span class="sxs-lookup"><span data-stu-id="8e971-110">Size, in bytes, of the error buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8e971-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="8e971-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="8e971-112">Ponteiro para um buffer definido pelo aplicativo usado para retornar a cadeia de caracteres de erro.</span><span class="sxs-lookup"><span data-stu-id="8e971-112">Pointer to an application-defined buffer used to return the error string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e971-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8e971-113">Return Value</span></span>

<span data-ttu-id="8e971-114">Retorna o valor de erro de inteiro se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8e971-114">Returns the integer error value if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e971-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e971-115">Remarks</span></span>

<span data-ttu-id="8e971-116">Se *LP* for um ponteiro válido, uma cadeia de caracteres terminada em nulo correspondente ao erro será retornada em seu buffer.</span><span class="sxs-lookup"><span data-stu-id="8e971-116">If *lp* is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer.</span></span> <span data-ttu-id="8e971-117">Se a cadeia de caracteres de erro for maior do que o buffer, MCIWnd o truncará.</span><span class="sxs-lookup"><span data-stu-id="8e971-117">If the error string is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e971-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e971-118">Requirements</span></span>



| <span data-ttu-id="8e971-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e971-119">Requirement</span></span> | <span data-ttu-id="8e971-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8e971-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e971-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e971-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e971-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8e971-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8e971-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e971-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e971-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8e971-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8e971-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e971-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e971-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e971-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e971-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e971-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e971-128">**MCIWndGetError**</span><span class="sxs-lookup"><span data-stu-id="8e971-128">**MCIWndGetError**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





