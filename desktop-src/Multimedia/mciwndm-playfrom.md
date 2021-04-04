---
title: Mensagem de MCIWNDM_PLAYFROM (VFW. h)
description: A \_ mensagem MCIWNDM PLAYFROM reproduz o conteúdo de um dispositivo MCI do local especificado até o final do conteúdo ou até que outro comando pare a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PLAYFROM
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918101"
---
# <a name="mciwndm_playfrom-message"></a><span data-ttu-id="ea9d3-105">\_Mensagem MCIWNDM PLAYFROM</span><span class="sxs-lookup"><span data-stu-id="ea9d3-105">MCIWNDM\_PLAYFROM message</span></span>

<span data-ttu-id="ea9d3-106">A mensagem **MCIWNDM \_ PLAYFROM** reproduz o conteúdo de um dispositivo MCI do local especificado até o final do conteúdo ou até que outro comando pare a reprodução.</span><span class="sxs-lookup"><span data-stu-id="ea9d3-106">The **MCIWNDM\_PLAYFROM** message plays the content of an MCI device from the specified location to the end of the content or until another command stops playback.</span></span> <span data-ttu-id="ea9d3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="ea9d3-107">You can send this message explicitly or by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span>


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a><span data-ttu-id="ea9d3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea9d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9d3-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span><span class="sxs-lookup"><span data-stu-id="ea9d3-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span></span>
</dt> <dd>

<span data-ttu-id="ea9d3-110">Local inicial.</span><span class="sxs-lookup"><span data-stu-id="ea9d3-110">Starting location.</span></span> <span data-ttu-id="ea9d3-111">As unidades para o local inicial dependem do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="ea9d3-111">The units for the starting location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9d3-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ea9d3-112">Return Value</span></span>

<span data-ttu-id="ea9d3-113">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ea9d3-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9d3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea9d3-114">Remarks</span></span>

<span data-ttu-id="ea9d3-115">Você também pode especificar um local de início e de término para reprodução usando a macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="ea9d3-115">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9d3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea9d3-116">Requirements</span></span>



| <span data-ttu-id="ea9d3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea9d3-117">Requirement</span></span> | <span data-ttu-id="ea9d3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ea9d3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ea9d3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea9d3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea9d3-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ea9d3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ea9d3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea9d3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea9d3-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ea9d3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ea9d3-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ea9d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea9d3-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea9d3-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9d3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea9d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9d3-126">**MCIWndPlayFrom**</span><span class="sxs-lookup"><span data-stu-id="ea9d3-126">**MCIWndPlayFrom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[<span data-ttu-id="ea9d3-127">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="ea9d3-127">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





