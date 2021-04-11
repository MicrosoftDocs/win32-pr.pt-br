---
title: Mensagem de MCIWNDM_RETURNSTRING (VFW. h)
description: A \_ mensagem returnstring MCIWNDM recupera a resposta para o comando de cadeia de caracteres MCI mais recente enviado para um dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- Multimídia do Windows de mensagem MCIWNDM_RETURNSTRING
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009340"
---
# <a name="mciwndm_returnstring-message"></a><span data-ttu-id="f47db-104">Mensagem de retorno de MCIWNDM \_</span><span class="sxs-lookup"><span data-stu-id="f47db-104">MCIWNDM\_RETURNSTRING message</span></span>

<span data-ttu-id="f47db-105">A **mensagem \_ returnstring MCIWNDM** recupera a resposta para o comando de cadeia de caracteres MCI mais recente enviado para um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f47db-105">The **MCIWNDM\_RETURNSTRING** message retrieves the reply to the most recent MCI string command sent to an MCI device.</span></span> <span data-ttu-id="f47db-106">As informações na resposta são fornecidas como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f47db-106">Information in the reply is supplied as a null-terminated string.</span></span> <span data-ttu-id="f47db-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="f47db-107">You can send this message explicitly or by using the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="f47db-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f47db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f47db-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="f47db-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="f47db-110">Tamanho, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="f47db-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f47db-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="f47db-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="f47db-112">Ponteiro para um buffer definido pelo aplicativo para conter a cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f47db-112">Pointer to an application-defined buffer to contain the null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f47db-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f47db-113">Return Value</span></span>

<span data-ttu-id="f47db-114">Retorna um inteiro correspondente à cadeia de caracteres MCI.</span><span class="sxs-lookup"><span data-stu-id="f47db-114">Returns an integer corresponding to the MCI string.</span></span>

## <a name="remarks"></a><span data-ttu-id="f47db-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f47db-115">Remarks</span></span>

<span data-ttu-id="f47db-116">Se a cadeia de caracteres terminada em nulo for maior que o buffer, a cadeia de caracteres será truncada.</span><span class="sxs-lookup"><span data-stu-id="f47db-116">If the null-terminated string is longer than the buffer, the string is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47db-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f47db-117">Requirements</span></span>



| <span data-ttu-id="f47db-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f47db-118">Requirement</span></span> | <span data-ttu-id="f47db-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f47db-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f47db-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f47db-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f47db-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f47db-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f47db-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f47db-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f47db-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f47db-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f47db-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f47db-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f47db-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f47db-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47db-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f47db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47db-127">**MCIWndReturnString**</span><span class="sxs-lookup"><span data-stu-id="f47db-127">**MCIWndReturnString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





