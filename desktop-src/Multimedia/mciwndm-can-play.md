---
title: Mensagem de MCIWNDM_CAN_PLAY (VFW. h)
description: O MCIWNDM \_ pode \_ reproduzir a mensagem para determinar se um dispositivo MCI pode reproduzir um arquivo de dados ou conteúdo de algum outro tipo. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_PLAY
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757771"
---
# <a name="mciwndm_can_play-message"></a><span data-ttu-id="a946e-105">MCIWNDM \_ pode \_ reproduzir a mensagem</span><span class="sxs-lookup"><span data-stu-id="a946e-105">MCIWNDM\_CAN\_PLAY message</span></span>

<span data-ttu-id="a946e-106">O **MCIWNDM \_ pode \_ reproduzir** a mensagem para determinar se um dispositivo MCI pode reproduzir um arquivo de dados ou conteúdo de algum outro tipo.</span><span class="sxs-lookup"><span data-stu-id="a946e-106">The **MCIWNDM\_CAN\_PLAY** message determines if an MCI device can play a data file or content of some other kind.</span></span> <span data-ttu-id="a946e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .</span><span class="sxs-lookup"><span data-stu-id="a946e-107">You can send this message explicitly or by using the [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) macro.</span></span>


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="a946e-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a946e-108">Return Value</span></span>

<span data-ttu-id="a946e-109">Retornará **true** se o dispositivo der suporte à reprodução dos dados ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a946e-109">Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a946e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a946e-110">Requirements</span></span>



| <span data-ttu-id="a946e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a946e-111">Requirement</span></span> | <span data-ttu-id="a946e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a946e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a946e-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a946e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a946e-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a946e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a946e-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a946e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a946e-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a946e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a946e-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a946e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a946e-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a946e-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a946e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a946e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a946e-120">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="a946e-120">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





