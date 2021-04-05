---
title: Mensagem de MCIWNDM_GET_DEST (VFW. h)
description: O MCIWNDM \_ obter \_ mensagem de destino recupera as coordenadas do retângulo de destino usado para ampliar ou alongar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetDest.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GET_DEST
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008835"
---
# <a name="mciwndm_get_dest-message"></a><span data-ttu-id="3cc54-105">MCIWNDM \_ obter \_ mensagem de destino</span><span class="sxs-lookup"><span data-stu-id="3cc54-105">MCIWNDM\_GET\_DEST message</span></span>

<span data-ttu-id="3cc54-106">O **MCIWNDM \_ obter \_** mensagem de destino recupera as coordenadas do retângulo de destino usado para ampliar ou alongar as imagens de um arquivo AVI durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="3cc54-106">The **MCIWNDM\_GET\_DEST** message retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="3cc54-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) .</span><span class="sxs-lookup"><span data-stu-id="3cc54-107">You can send this message explicitly or by using the [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) macro.</span></span>


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="3cc54-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cc54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc54-109"><span id="prc"></span><span id="PRC"></span>*popular*</span><span class="sxs-lookup"><span data-stu-id="3cc54-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="3cc54-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para retornar as coordenadas do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="3cc54-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to return the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cc54-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3cc54-111">Return Value</span></span>

<span data-ttu-id="3cc54-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3cc54-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc54-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cc54-113">Requirements</span></span>



| <span data-ttu-id="3cc54-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cc54-114">Requirement</span></span> | <span data-ttu-id="3cc54-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3cc54-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3cc54-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cc54-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3cc54-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3cc54-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3cc54-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cc54-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3cc54-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3cc54-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3cc54-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3cc54-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cc54-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cc54-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc54-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cc54-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc54-123">**MCIWndGetDest**</span><span class="sxs-lookup"><span data-stu-id="3cc54-123">**MCIWndGetDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

