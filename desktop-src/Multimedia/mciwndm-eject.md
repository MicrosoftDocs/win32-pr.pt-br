---
title: Mensagem de MCIWNDM_EJECT (VFW. h)
description: A \_ mensagem de ejeção MCIWNDM envia um comando para um dispositivo MCI para ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- Multimídia do Windows de mensagem MCIWNDM_EJECT
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369348"
---
# <a name="mciwndm_eject-message"></a><span data-ttu-id="7901f-105">Mensagem de ejeção de MCIWNDM \_</span><span class="sxs-lookup"><span data-stu-id="7901f-105">MCIWNDM\_EJECT message</span></span>

<span data-ttu-id="7901f-106">A mensagem de **\_ ejeção MCIWNDM** envia um comando para um dispositivo MCI para ejetar sua mídia.</span><span class="sxs-lookup"><span data-stu-id="7901f-106">The **MCIWNDM\_EJECT** message sends a command to an MCI device to eject its media.</span></span> <span data-ttu-id="7901f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .</span><span class="sxs-lookup"><span data-stu-id="7901f-107">You can send this message explicitly or by using the [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) macro.</span></span>


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="7901f-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7901f-108">Return Value</span></span>

<span data-ttu-id="7901f-109">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="7901f-109">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7901f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7901f-110">Requirements</span></span>



| <span data-ttu-id="7901f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7901f-111">Requirement</span></span> | <span data-ttu-id="7901f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7901f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7901f-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7901f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7901f-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7901f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7901f-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7901f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7901f-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7901f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7901f-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7901f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7901f-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7901f-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7901f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7901f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7901f-120">**MCIWndEject**</span><span class="sxs-lookup"><span data-stu-id="7901f-120">**MCIWndEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





