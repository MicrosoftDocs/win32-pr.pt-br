---
title: Mensagem de MCIWNDM_GETEND (VFW. h)
description: A \_ mensagem MCIWNDM GETEND recupera o local do final do conteúdo de um dispositivo ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETEND
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824734"
---
# <a name="mciwndm_getend-message"></a><span data-ttu-id="826a0-105">\_Mensagem MCIWNDM GETEND</span><span class="sxs-lookup"><span data-stu-id="826a0-105">MCIWNDM\_GETEND message</span></span>

<span data-ttu-id="826a0-106">A mensagem **MCIWNDM \_ GETEND** recupera o local do final do conteúdo de um dispositivo ou arquivo MCI.</span><span class="sxs-lookup"><span data-stu-id="826a0-106">The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file.</span></span> <span data-ttu-id="826a0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="826a0-107">You can send this message explicitly or by using the [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macro.</span></span>


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="826a0-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="826a0-108">Return Value</span></span>

<span data-ttu-id="826a0-109">Retorna o local no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="826a0-109">Returns the location in the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="826a0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="826a0-110">Requirements</span></span>



| <span data-ttu-id="826a0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="826a0-111">Requirement</span></span> | <span data-ttu-id="826a0-112">Valor</span><span class="sxs-lookup"><span data-stu-id="826a0-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="826a0-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="826a0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="826a0-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="826a0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="826a0-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="826a0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="826a0-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="826a0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="826a0-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="826a0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="826a0-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="826a0-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826a0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="826a0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826a0-120">**MCIWndGetEnd**</span><span class="sxs-lookup"><span data-stu-id="826a0-120">**MCIWndGetEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





