---
title: Mensagem de MCIWNDM_GETSTART (VFW. h)
description: A \_ mensagem GETstart MCIWNDM recupera o local do início do conteúdo de um dispositivo ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETSTART
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454749"
---
# <a name="mciwndm_getstart-message"></a><span data-ttu-id="7b400-105">MCIWNDM \_ getiniciar mensagem</span><span class="sxs-lookup"><span data-stu-id="7b400-105">MCIWNDM\_GETSTART message</span></span>

<span data-ttu-id="7b400-106">A **mensagem \_ GetStart MCIWNDM** recupera o local do início do conteúdo de um dispositivo ou arquivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7b400-106">The **MCIWNDM\_GETSTART** message retrieves the location of the beginning of the content of an MCI device or file.</span></span> <span data-ttu-id="7b400-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .</span><span class="sxs-lookup"><span data-stu-id="7b400-107">You can send this message explicitly or by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) macro.</span></span>


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="7b400-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7b400-108">Return Value</span></span>

<span data-ttu-id="7b400-109">Retorna o local no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="7b400-109">Returns the location in the current time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b400-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b400-110">Remarks</span></span>

<span data-ttu-id="7b400-111">Normalmente, o valor de retorno é zero; Mas alguns dispositivos usam um local de início diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7b400-111">Typically, the return value is zero; but some devices use a nonzero starting location.</span></span> <span data-ttu-id="7b400-112">A busca desse local define o dispositivo para o início da mídia.</span><span class="sxs-lookup"><span data-stu-id="7b400-112">Seeking to this location sets the device to the start of the media.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b400-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b400-113">Requirements</span></span>



| <span data-ttu-id="7b400-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b400-114">Requirement</span></span> | <span data-ttu-id="7b400-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7b400-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7b400-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b400-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7b400-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b400-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7b400-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b400-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7b400-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b400-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b400-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7b400-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b400-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b400-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b400-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b400-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b400-123">**MCIWndGetStart**</span><span class="sxs-lookup"><span data-stu-id="7b400-123">**MCIWndGetStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





