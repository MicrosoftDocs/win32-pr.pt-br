---
title: Mensagem de MCIWNDM_SETSPEED (VFW. h)
description: A \_ mensagem MCIWNDM SETSPEED define a velocidade de reprodução de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetSpeed.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETSPEED
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918754"
---
# <a name="mciwndm_setspeed-message"></a><span data-ttu-id="9c202-105">Mensagem de MCIWNDM \_ SETspeed</span><span class="sxs-lookup"><span data-stu-id="9c202-105">MCIWNDM\_SETSPEED message</span></span>

<span data-ttu-id="9c202-106">A mensagem **MCIWNDM \_ SETSPEED** define a velocidade de reprodução de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="9c202-106">The **MCIWNDM\_SETSPEED** message sets the playback speed of an MCI device.</span></span> <span data-ttu-id="9c202-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="9c202-107">You can send this message explicitly or by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span>


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a><span data-ttu-id="9c202-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c202-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*ispeedy*</span><span class="sxs-lookup"><span data-stu-id="9c202-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="9c202-110">Velocidade de reprodução.</span><span class="sxs-lookup"><span data-stu-id="9c202-110">Playback speed.</span></span> <span data-ttu-id="9c202-111">Especifique 1000 para velocidade normal, valores maiores para velocidades mais rápidas e valores menores para velocidades mais lentas.</span><span class="sxs-lookup"><span data-stu-id="9c202-111">Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c202-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9c202-112">Return Value</span></span>

<span data-ttu-id="9c202-113">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9c202-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c202-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c202-114">Requirements</span></span>



| <span data-ttu-id="9c202-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c202-115">Requirement</span></span> | <span data-ttu-id="9c202-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9c202-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9c202-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c202-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c202-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c202-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9c202-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c202-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c202-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c202-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9c202-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9c202-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c202-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c202-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c202-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c202-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c202-124">**MCIWndSetSpeed**</span><span class="sxs-lookup"><span data-stu-id="9c202-124">**MCIWndSetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





