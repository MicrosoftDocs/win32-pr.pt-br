---
title: Mensagem de MCIWNDM_GETALIAS (VFW. h)
description: A \_ mensagem GETALIAS MCIWNDM recupera o alias usado para abrir um dispositivo ou arquivo MCI com a função mciSendString. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETALIAS
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105785411"
---
# <a name="mciwndm_getalias-message"></a><span data-ttu-id="6bd35-105">\_Mensagem GETALIAS MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="6bd35-105">MCIWNDM\_GETALIAS message</span></span>

<span data-ttu-id="6bd35-106">A **mensagem \_ getalias MCIWNDM** recupera o alias usado para abrir um dispositivo ou arquivo MCI com a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6bd35-106">The **MCIWNDM\_GETALIAS** message retrieves the alias used to open an MCI device or file with the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="6bd35-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="6bd35-107">You can send this message explicitly or by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span>


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="6bd35-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6bd35-108">Return Value</span></span>

<span data-ttu-id="6bd35-109">Retorna o alias do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6bd35-109">Returns the device alias.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd35-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bd35-110">Requirements</span></span>



| <span data-ttu-id="6bd35-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bd35-111">Requirement</span></span> | <span data-ttu-id="6bd35-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6bd35-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6bd35-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bd35-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6bd35-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6bd35-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6bd35-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bd35-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6bd35-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6bd35-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6bd35-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6bd35-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bd35-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bd35-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bd35-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bd35-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="6bd35-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6bd35-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6bd35-121">**MCIWndGetAlias**</span><span class="sxs-lookup"><span data-stu-id="6bd35-121">**MCIWndGetAlias**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

