---
title: Mensagem de MCIWNDM_GETVOLUME (VFW. h)
description: A \_ mensagem GETVOLUME MCIWNDM recupera a configuração de volume atual de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETVOLUME
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369884"
---
# <a name="mciwndm_getvolume-message"></a><span data-ttu-id="396d8-105">\_Mensagem GETVOLUME MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="396d8-105">MCIWNDM\_GETVOLUME message</span></span>

<span data-ttu-id="396d8-106">A **mensagem \_ GetVolume MCIWNDM** recupera a configuração de volume atual de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="396d8-106">The **MCIWNDM\_GETVOLUME** message retrieves the current volume setting of an MCI device.</span></span> <span data-ttu-id="396d8-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="396d8-107">You can send this message explicitly or by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span>


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="396d8-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="396d8-108">Return Value</span></span>

<span data-ttu-id="396d8-109">Retorna a configuração de volume atual.</span><span class="sxs-lookup"><span data-stu-id="396d8-109">Returns the current volume setting.</span></span> <span data-ttu-id="396d8-110">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="396d8-110">The default value is 1000.</span></span> <span data-ttu-id="396d8-111">Valores mais altos indicam volumes mais altos, valores mais baixos indicam volumes mais silenciosos.</span><span class="sxs-lookup"><span data-stu-id="396d8-111">Higher values indicate louder volumes, lower values indicate quieter volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="396d8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="396d8-112">Requirements</span></span>



| <span data-ttu-id="396d8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="396d8-113">Requirement</span></span> | <span data-ttu-id="396d8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="396d8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="396d8-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="396d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="396d8-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="396d8-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="396d8-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="396d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="396d8-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="396d8-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="396d8-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="396d8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="396d8-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="396d8-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="396d8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="396d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396d8-122">**MCIWndGetVolume**</span><span class="sxs-lookup"><span data-stu-id="396d8-122">**MCIWndGetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





