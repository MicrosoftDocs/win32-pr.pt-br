---
title: Mensagem de MCIWNDM_SETPALETTE (VFW. h)
description: A \_ mensagem MCIWNDM SetPalette envia um identificador de paleta para o dispositivo MCI associado à janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETPALETTE
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455517"
---
# <a name="mciwndm_setpalette-message"></a><span data-ttu-id="a3cff-105">Mensagem da MCIWNDM \_ SETpalette</span><span class="sxs-lookup"><span data-stu-id="a3cff-105">MCIWNDM\_SETPALETTE message</span></span>

<span data-ttu-id="a3cff-106">A mensagem **MCIWNDM \_ SetPalette** envia um identificador de paleta para o dispositivo MCI associado à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="a3cff-106">The **MCIWNDM\_SETPALETTE** message sends a palette handle to the MCI device associated with the MCIWnd window.</span></span> <span data-ttu-id="a3cff-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="a3cff-107">You can send this message explicitly or by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="a3cff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3cff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3cff-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span><span class="sxs-lookup"><span data-stu-id="a3cff-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span></span>
</dt> <dd>

<span data-ttu-id="a3cff-110">Identificador da paleta.</span><span class="sxs-lookup"><span data-stu-id="a3cff-110">Palette handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3cff-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a3cff-111">Return Value</span></span>

<span data-ttu-id="a3cff-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a3cff-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3cff-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3cff-113">Requirements</span></span>



| <span data-ttu-id="a3cff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3cff-114">Requirement</span></span> | <span data-ttu-id="a3cff-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a3cff-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a3cff-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3cff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a3cff-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a3cff-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a3cff-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3cff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a3cff-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a3cff-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a3cff-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a3cff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3cff-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3cff-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3cff-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3cff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3cff-123">**MCIWndSetPalette**</span><span class="sxs-lookup"><span data-stu-id="a3cff-123">**MCIWndSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





