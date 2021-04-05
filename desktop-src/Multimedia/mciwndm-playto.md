---
title: Mensagem de MCIWNDM_PLAYTO (VFW. h)
description: A \_ mensagem MCIWNDM playto reproduz o conteúdo de um dispositivo MCI da posição atual para o local final especificado ou até que outro comando pare a reprodução.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PLAYTO
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086139"
---
# <a name="mciwndm_playto-message"></a><span data-ttu-id="0b050-104">\_Mensagem de playto do MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="0b050-104">MCIWNDM\_PLAYTO message</span></span>

<span data-ttu-id="0b050-105">A mensagem **MCIWNDM \_ playto** reproduz o conteúdo de um dispositivo MCI da posição atual para o local final especificado ou até que outro comando pare a reprodução.</span><span class="sxs-lookup"><span data-stu-id="0b050-105">The **MCIWNDM\_PLAYTO** message plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.</span></span> <span data-ttu-id="0b050-106">Se o local final especificado estiver além do fim do conteúdo, a reprodução será interrompida no final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0b050-106">If the specified ending location is beyond the end of the content, playback stops at the end of the content.</span></span> <span data-ttu-id="0b050-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="0b050-107">You can send this message explicitly or by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span>


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a><span data-ttu-id="0b050-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b050-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b050-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Emprestar*</span><span class="sxs-lookup"><span data-stu-id="0b050-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*lEnd*</span></span>
</dt> <dd>

<span data-ttu-id="0b050-110">Local final.</span><span class="sxs-lookup"><span data-stu-id="0b050-110">Ending location.</span></span> <span data-ttu-id="0b050-111">As unidades para o local final dependem do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="0b050-111">The units for the ending location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b050-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0b050-112">Return Value</span></span>

<span data-ttu-id="0b050-113">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="0b050-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b050-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b050-114">Remarks</span></span>

<span data-ttu-id="0b050-115">Essa macro é definida usando as macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) e [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , que, por sua vez, usam o comando [MCI \_ Seek](mci-seek.md) e a mensagem **MCIWNDM \_ playto** .</span><span class="sxs-lookup"><span data-stu-id="0b050-115">This macro is defined using the [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) and [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macros, which in turn use the [MCI\_SEEK](mci-seek.md) command and the **MCIWNDM\_PLAYTO** message.</span></span>

<span data-ttu-id="0b050-116">Você também pode especificar um local de início e de término para reprodução usando a macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="0b050-116">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b050-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b050-117">Requirements</span></span>



| <span data-ttu-id="0b050-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b050-118">Requirement</span></span> | <span data-ttu-id="0b050-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0b050-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0b050-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b050-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0b050-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b050-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0b050-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b050-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0b050-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b050-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0b050-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0b050-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b050-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b050-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b050-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b050-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b050-127">busca de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0b050-127">MCI\_SEEK</span></span>](mci-seek.md)
</dt> <dt>

[<span data-ttu-id="0b050-128">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="0b050-128">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[<span data-ttu-id="0b050-129">**MCIWndPlayTo**</span><span class="sxs-lookup"><span data-stu-id="0b050-129">**MCIWndPlayTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[<span data-ttu-id="0b050-130">**MCIWndSeek**</span><span class="sxs-lookup"><span data-stu-id="0b050-130">**MCIWndSeek**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





