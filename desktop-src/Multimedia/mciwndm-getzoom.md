---
title: Mensagem de MCIWNDM_GETZOOM (VFW. h)
description: A \_ mensagem getzoom do MCIWNDM recupera o valor de zoom atual usado por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETZOOM
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454983"
---
# <a name="mciwndm_getzoom-message"></a><span data-ttu-id="0ec92-105">\_Mensagem GETzoom do MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="0ec92-105">MCIWNDM\_GETZOOM message</span></span>

<span data-ttu-id="0ec92-106">A **mensagem \_ Getzoom do MCIWNDM** recupera o valor de zoom atual usado por um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0ec92-106">The **MCIWNDM\_GETZOOM** message retrieves the current zoom value used by an MCI device.</span></span> <span data-ttu-id="0ec92-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="0ec92-107">You can send this message explicitly or by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span>


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="0ec92-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0ec92-108">Return Value</span></span>

<span data-ttu-id="0ec92-109">Retorna os valores mais recentes usados com [**MCIWNDM \_ setZoom**](mciwndm-setzoom.md).</span><span class="sxs-lookup"><span data-stu-id="0ec92-109">Returns the most recent values used with [**MCIWNDM\_SETZOOM**](mciwndm-setzoom.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ec92-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ec92-110">Remarks</span></span>

<span data-ttu-id="0ec92-111">Um valor de retorno de 100 indica que a imagem não está ampliada.</span><span class="sxs-lookup"><span data-stu-id="0ec92-111">A return value of 100 indicates the image is not zoomed.</span></span> <span data-ttu-id="0ec92-112">Um valor de 200 indica que a imagem é ampliada para duas vezes seu tamanho original.</span><span class="sxs-lookup"><span data-stu-id="0ec92-112">A value of 200 indicates the image is enlarged to twice its original size.</span></span> <span data-ttu-id="0ec92-113">Um valor de 50 indica que a imagem é reduzida para metade do tamanho original.</span><span class="sxs-lookup"><span data-stu-id="0ec92-113">A value of 50 indicates the image is reduced to half its original size.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ec92-114">Requirements</span></span>



| <span data-ttu-id="0ec92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ec92-115">Requirement</span></span> | <span data-ttu-id="0ec92-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0ec92-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0ec92-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ec92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec92-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0ec92-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0ec92-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ec92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec92-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0ec92-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ec92-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0ec92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ec92-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ec92-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ec92-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ec92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec92-124">**MCIWndGetZoom**</span><span class="sxs-lookup"><span data-stu-id="0ec92-124">**MCIWndGetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[<span data-ttu-id="0ec92-125">**MCIWNDM \_ SETzoom**</span><span class="sxs-lookup"><span data-stu-id="0ec92-125">**MCIWNDM\_SETZOOM**</span></span>](mciwndm-setzoom.md)
</dt> </dl>

 

 





