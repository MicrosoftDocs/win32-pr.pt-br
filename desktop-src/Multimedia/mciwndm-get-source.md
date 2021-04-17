---
title: Mensagem de MCIWNDM_GET_SOURCE (VFW. h)
description: O MCIWNDM \_ obter \_ a mensagem de origem recupera as coordenadas do retângulo de origem usado para cortar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GET_SOURCE
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369799"
---
# <a name="mciwndm_get_source-message"></a><span data-ttu-id="f3231-105">MCIWNDM \_ obter \_ mensagem de origem</span><span class="sxs-lookup"><span data-stu-id="f3231-105">MCIWNDM\_GET\_SOURCE message</span></span>

<span data-ttu-id="f3231-106">O **MCIWNDM \_ obter \_** a mensagem de origem recupera as coordenadas do retângulo de origem usado para cortar as imagens de um arquivo AVI durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="f3231-106">The **MCIWNDM\_GET\_SOURCE** message retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="f3231-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .</span><span class="sxs-lookup"><span data-stu-id="f3231-107">You can send this message explicitly or by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span>


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="f3231-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3231-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3231-109"><span id="prc"></span><span id="PRC"></span>*popular*</span><span class="sxs-lookup"><span data-stu-id="f3231-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="f3231-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para conter as coordenadas do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="f3231-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to contain the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3231-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f3231-111">Return Value</span></span>

<span data-ttu-id="f3231-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f3231-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3231-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3231-113">Requirements</span></span>



| <span data-ttu-id="f3231-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3231-114">Requirement</span></span> | <span data-ttu-id="f3231-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f3231-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3231-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3231-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f3231-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3231-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3231-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3231-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f3231-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3231-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3231-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f3231-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3231-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3231-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3231-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3231-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3231-123">**MCIWndGetSource**</span><span class="sxs-lookup"><span data-stu-id="f3231-123">**MCIWndGetSource**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

