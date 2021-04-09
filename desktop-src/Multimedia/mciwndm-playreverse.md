---
title: Mensagem de MCIWNDM_PLAYREVERSE (VFW. h)
description: A \_ mensagem MCIWNDM PLAYREVERSE reproduz o conteúdo atual na direção inversa, começando na posição atual e terminando no início do conteúdo ou até que outro comando pare a reprodução.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PLAYREVERSE
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085143"
---
# <a name="mciwndm_playreverse-message"></a><span data-ttu-id="ec693-104">\_Mensagem MCIWNDM PLAYREVERSE</span><span class="sxs-lookup"><span data-stu-id="ec693-104">MCIWNDM\_PLAYREVERSE message</span></span>

<span data-ttu-id="ec693-105">A mensagem **MCIWNDM \_ PLAYREVERSE** reproduz o conteúdo atual na direção inversa, começando na posição atual e terminando no início do conteúdo ou até que outro comando pare a reprodução.</span><span class="sxs-lookup"><span data-stu-id="ec693-105">The **MCIWNDM\_PLAYREVERSE** message plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.</span></span> <span data-ttu-id="ec693-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="ec693-106">You can send this message explicitly or by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span>


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ec693-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ec693-107">Return Value</span></span>

<span data-ttu-id="ec693-108">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ec693-108">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec693-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec693-109">Requirements</span></span>



| <span data-ttu-id="ec693-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec693-110">Requirement</span></span> | <span data-ttu-id="ec693-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ec693-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec693-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec693-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ec693-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec693-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec693-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec693-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ec693-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec693-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec693-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec693-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec693-117"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec693-117"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec693-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec693-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec693-119">**MCIWndPlayReverse**</span><span class="sxs-lookup"><span data-stu-id="ec693-119">**MCIWndPlayReverse**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





