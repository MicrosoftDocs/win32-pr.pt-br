---
title: Mensagem de MCIWNDM_SETVOLUME (VFW. h)
description: A \_ mensagem SETVOLUME MCIWNDM define o nível de volume de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETVOLUME
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644332"
---
# <a name="mciwndm_setvolume-message"></a><span data-ttu-id="31bf3-105">Mensagem do MCIWNDM \_ SETvolume</span><span class="sxs-lookup"><span data-stu-id="31bf3-105">MCIWNDM\_SETVOLUME message</span></span>

<span data-ttu-id="31bf3-106">A **mensagem \_ SetVolume MCIWNDM** define o nível de volume de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="31bf3-106">The **MCIWNDM\_SETVOLUME** message sets the volume level of an MCI device.</span></span> <span data-ttu-id="31bf3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="31bf3-107">You can send this message explicitly or by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span>


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a><span data-ttu-id="31bf3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31bf3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31bf3-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span><span class="sxs-lookup"><span data-stu-id="31bf3-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span></span>
</dt> <dd>

<span data-ttu-id="31bf3-110">Novo nível de volume.</span><span class="sxs-lookup"><span data-stu-id="31bf3-110">New volume level.</span></span> <span data-ttu-id="31bf3-111">Especifique 1000 para o nível de volume normal.</span><span class="sxs-lookup"><span data-stu-id="31bf3-111">Specify 1000 for normal volume level.</span></span> <span data-ttu-id="31bf3-112">Especifique um valor mais alto para um volume mais alto ou um valor inferior para um volume mais silencioso.</span><span class="sxs-lookup"><span data-stu-id="31bf3-112">Specify a higher value for a louder volume or a lower value for a quieter volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31bf3-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="31bf3-113">Return Value</span></span>

<span data-ttu-id="31bf3-114">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="31bf3-114">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="31bf3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31bf3-115">Requirements</span></span>



| <span data-ttu-id="31bf3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="31bf3-116">Requirement</span></span> | <span data-ttu-id="31bf3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="31bf3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="31bf3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31bf3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31bf3-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31bf3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="31bf3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31bf3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31bf3-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31bf3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="31bf3-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31bf3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="31bf3-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="31bf3-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31bf3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="31bf3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31bf3-125">**MCIWndSetVolume**</span><span class="sxs-lookup"><span data-stu-id="31bf3-125">**MCIWndSetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





