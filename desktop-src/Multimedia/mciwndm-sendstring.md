---
title: Mensagem de MCIWNDM_SENDSTRING (VFW. h)
description: A \_ mensagem SendString MCIWNDM envia um comando MCI no formato de cadeia de caracteres para o dispositivo associado à janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SENDSTRING
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644896"
---
# <a name="mciwndm_sendstring-message"></a><span data-ttu-id="fc0c3-105">\_Mensagem MCIWNDM SendString</span><span class="sxs-lookup"><span data-stu-id="fc0c3-105">MCIWNDM\_SENDSTRING message</span></span>

<span data-ttu-id="fc0c3-106">A **mensagem \_ SendString MCIWNDM** envia um comando MCI no formato de cadeia de caracteres para o dispositivo associado à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="fc0c3-106">The **MCIWNDM\_SENDSTRING** message sends an MCI command in string form to the device associated with the MCIWnd window.</span></span> <span data-ttu-id="fc0c3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .</span><span class="sxs-lookup"><span data-stu-id="fc0c3-107">You can send this message explicitly or by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro.</span></span>


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a><span data-ttu-id="fc0c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc0c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc0c3-109"><span id="sz"></span><span id="SZ"></span>*sz*</span><span class="sxs-lookup"><span data-stu-id="fc0c3-109"><span id="sz"></span><span id="SZ"></span>*sz*</span></span>
</dt> <dd>

<span data-ttu-id="fc0c3-110">Comando de cadeia de caracteres para enviar para o dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="fc0c3-110">String command to send to the MCI device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc0c3-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fc0c3-111">Return Value</span></span>

<span data-ttu-id="fc0c3-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="fc0c3-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc0c3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc0c3-113">Remarks</span></span>

<span data-ttu-id="fc0c3-114">O manipulador de mensagens **para \_ SendString MCIWNDM** anexa um alias de dispositivo ao comando MCI que você envia para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc0c3-114">The message handler for **MCIWNDM\_SENDSTRING** appends a device alias to the MCI command you send to the device.</span></span> <span data-ttu-id="fc0c3-115">Portanto, você não deve usar nenhum alias em um comando MCI que você emite com **MCIWNDM \_ SendString**.</span><span class="sxs-lookup"><span data-stu-id="fc0c3-115">Therefore, you should not use any alias in an MCI command that you issue with **MCIWNDM\_SENDSTRING**.</span></span>

<span data-ttu-id="fc0c3-116">Para obter a cadeia de caracteres de retorno, que contém o resultado do comando, envie a mensagem de [**\_ retorno de MCIWNDM**](mciwndm-returnstring.md) .</span><span class="sxs-lookup"><span data-stu-id="fc0c3-116">To get the return string, which contains the result of the command, send the [**MCIWNDM\_RETURNSTRING**](mciwndm-returnstring.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc0c3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc0c3-117">Requirements</span></span>



| <span data-ttu-id="fc0c3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc0c3-118">Requirement</span></span> | <span data-ttu-id="fc0c3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fc0c3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fc0c3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc0c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fc0c3-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc0c3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fc0c3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc0c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fc0c3-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc0c3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fc0c3-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fc0c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc0c3-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c3-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc0c3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc0c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0c3-127">**MCIWndSendString**</span><span class="sxs-lookup"><span data-stu-id="fc0c3-127">**MCIWndSendString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[<span data-ttu-id="fc0c3-128">Cadeias de caracteres de comando multimídia</span><span class="sxs-lookup"><span data-stu-id="fc0c3-128">Multimedia Command Strings</span></span>](multimedia-command-strings.md)
</dt> </dl>

 

 





