---
title: Mensagem de MCIWNDM_VALIDATEMEDIA (VFW. h)
description: A \_ mensagem MCIWNDM VALIDATEMEDIA atualiza os locais inicial e final do conteúdo, a posição atual no conteúdo e o TrackBar de acordo com o formato de hora atual.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- Multimídia do Windows de mensagem MCIWNDM_VALIDATEMEDIA
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499252"
---
# <a name="mciwndm_validatemedia-message"></a><span data-ttu-id="203d7-104">\_Mensagem MCIWNDM VALIDATEMEDIA</span><span class="sxs-lookup"><span data-stu-id="203d7-104">MCIWNDM\_VALIDATEMEDIA message</span></span>

<span data-ttu-id="203d7-105">A mensagem **MCIWNDM \_ VALIDATEMEDIA** atualiza os locais inicial e final do conteúdo, a posição atual no conteúdo e o TrackBar de acordo com o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="203d7-105">The **MCIWNDM\_VALIDATEMEDIA** message updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.</span></span> <span data-ttu-id="203d7-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .</span><span class="sxs-lookup"><span data-stu-id="203d7-106">You can send this message explicitly or by using the [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) macro.</span></span>


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="203d7-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="203d7-107">Return Value</span></span>

<span data-ttu-id="203d7-108">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="203d7-108">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="203d7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="203d7-109">Remarks</span></span>

<span data-ttu-id="203d7-110">Normalmente, você não precisa usar essa macro; no entanto, se seu aplicativo alterar o formato de hora de um dispositivo sem usar MCIWnd; os locais inicial e final do conteúdo, bem como o TrackBar, continuam a usar o formato antigo.</span><span class="sxs-lookup"><span data-stu-id="203d7-110">Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format.</span></span> <span data-ttu-id="203d7-111">Você pode usar essa macro para atualizar esses valores.</span><span class="sxs-lookup"><span data-stu-id="203d7-111">You can use this macro to update these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="203d7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="203d7-112">Requirements</span></span>



| <span data-ttu-id="203d7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="203d7-113">Requirement</span></span> | <span data-ttu-id="203d7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="203d7-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="203d7-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="203d7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="203d7-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="203d7-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="203d7-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="203d7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="203d7-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="203d7-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="203d7-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="203d7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="203d7-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="203d7-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203d7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="203d7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203d7-122">**MCIWndValidateMedia**</span><span class="sxs-lookup"><span data-stu-id="203d7-122">**MCIWndValidateMedia**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





