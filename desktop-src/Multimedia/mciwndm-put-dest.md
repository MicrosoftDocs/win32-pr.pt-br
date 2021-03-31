---
title: Mensagem de MCIWNDM_PUT_DEST (VFW. h)
description: O MCIWNDM \_ colocar \_ mensagem de destino redefine as coordenadas do retângulo de destino usado para ampliar ou alongar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PUT_DEST
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645012"
---
# <a name="mciwndm_put_dest-message"></a><span data-ttu-id="5e9d1-105">MCIWNDM \_ colocar \_ mensagem de dest</span><span class="sxs-lookup"><span data-stu-id="5e9d1-105">MCIWNDM\_PUT\_DEST message</span></span>

<span data-ttu-id="5e9d1-106">O **MCIWNDM \_ colocar \_** mensagem de destino redefine as coordenadas do retângulo de destino usado para ampliar ou alongar as imagens de um arquivo AVI durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="5e9d1-106">The **MCIWNDM\_PUT\_DEST** message redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="5e9d1-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .</span><span class="sxs-lookup"><span data-stu-id="5e9d1-107">You can send this message explicitly or by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span>


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="5e9d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e9d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e9d1-109"><span id="prc"></span><span id="PRC"></span>*popular*</span><span class="sxs-lookup"><span data-stu-id="5e9d1-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="5e9d1-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="5e9d1-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e9d1-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5e9d1-111">Return Value</span></span>

<span data-ttu-id="5e9d1-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="5e9d1-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e9d1-113">Requirements</span></span>



| <span data-ttu-id="5e9d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9d1-114">Requirement</span></span> | <span data-ttu-id="5e9d1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5e9d1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5e9d1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e9d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5e9d1-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e9d1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5e9d1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e9d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5e9d1-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e9d1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5e9d1-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5e9d1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e9d1-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e9d1-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9d1-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5e9d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9d1-123">**MCIWndPutDest**</span><span class="sxs-lookup"><span data-stu-id="5e9d1-123">**MCIWndPutDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

