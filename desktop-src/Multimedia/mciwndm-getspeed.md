---
title: Mensagem de MCIWNDM_GETSPEED (VFW. h)
description: A \_ mensagem GETspeed do MCIWNDM recupera a velocidade de reprodução de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETSPEED
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455883"
---
# <a name="mciwndm_getspeed-message"></a><span data-ttu-id="2debf-105">MCIWNDM \_ mensagem de GETspeed</span><span class="sxs-lookup"><span data-stu-id="2debf-105">MCIWNDM\_GETSPEED message</span></span>

<span data-ttu-id="2debf-106">A **mensagem \_ getspeed do MCIWNDM** recupera a velocidade de reprodução de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="2debf-106">The **MCIWNDM\_GETSPEED** message retrieves the playback speed of an MCI device.</span></span> <span data-ttu-id="2debf-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="2debf-107">You can send this message explicitly or by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span>


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="2debf-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2debf-108">Return Value</span></span>

<span data-ttu-id="2debf-109">Retorna a velocidade de reprodução se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2debf-109">Returns the playback speed if successful.</span></span> <span data-ttu-id="2debf-110">O valor da velocidade normal é de 1000.</span><span class="sxs-lookup"><span data-stu-id="2debf-110">The value for normal speed is 1000.</span></span> <span data-ttu-id="2debf-111">Valores maiores indicam velocidades mais rápidas, valores menores indicam velocidades mais lentas.</span><span class="sxs-lookup"><span data-stu-id="2debf-111">Larger values indicate faster speeds, smaller values indicate slower speeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="2debf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2debf-112">Requirements</span></span>



| <span data-ttu-id="2debf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2debf-113">Requirement</span></span> | <span data-ttu-id="2debf-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2debf-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2debf-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2debf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2debf-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2debf-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2debf-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2debf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2debf-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2debf-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2debf-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2debf-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2debf-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2debf-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2debf-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2debf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2debf-122">**MCIWndGetSpeed**</span><span class="sxs-lookup"><span data-stu-id="2debf-122">**MCIWndGetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





