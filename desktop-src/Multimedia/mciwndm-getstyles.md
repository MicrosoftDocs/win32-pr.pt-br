---
title: Mensagem de MCIWNDM_GETSTYLES (VFW. h)
description: A \_ mensagem GETestilos MCIWNDM recupera os sinalizadores que especificam os estilos de janela MCIWnd atuais usados por uma janela. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETSTYLES
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768707"
---
# <a name="mciwndm_getstyles-message"></a><span data-ttu-id="5be75-105">\_Mensagem de GETestilizas MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="5be75-105">MCIWNDM\_GETSTYLES message</span></span>

<span data-ttu-id="5be75-106">A **mensagem \_ getestilos MCIWNDM** recupera os sinalizadores que especificam os estilos de janela MCIWnd atuais usados por uma janela.</span><span class="sxs-lookup"><span data-stu-id="5be75-106">The **MCIWNDM\_GETSTYLES** message retrieves the flags specifying the current MCIWnd window styles used by a window.</span></span> <span data-ttu-id="5be75-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="5be75-107">You can send this message explicitly or by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5be75-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5be75-108">Return Value</span></span>

<span data-ttu-id="5be75-109">Retorna um valor que representa os estilos atuais da janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5be75-109">Returns a value representing the current styles of the MCIWnd window.</span></span> <span data-ttu-id="5be75-110">O valor de retorno é o operador de bits OR de MCIWnd de estilos de janela (sinalizadores MCIWNDF).</span><span class="sxs-lookup"><span data-stu-id="5be75-110">The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).</span></span>

## <a name="requirements"></a><span data-ttu-id="5be75-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5be75-111">Requirements</span></span>



| <span data-ttu-id="5be75-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5be75-112">Requirement</span></span> | <span data-ttu-id="5be75-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5be75-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5be75-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5be75-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5be75-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5be75-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5be75-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5be75-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5be75-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5be75-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5be75-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5be75-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5be75-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5be75-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5be75-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5be75-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be75-121">**MCIWndGetStyles**</span><span class="sxs-lookup"><span data-stu-id="5be75-121">**MCIWndGetStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





