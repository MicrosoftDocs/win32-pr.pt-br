---
description: Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver descarregando a DLL.
title: Mensagem de FMEVENT_UNLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 24b5b2a77393178cad545cb63c1524a8d7e92c5c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843067"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="5e5c8-103">\_Mensagem de descarregamento de FMEVENT</span><span class="sxs-lookup"><span data-stu-id="5e5c8-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="5e5c8-104">Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver descarregando a DLL.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e5c8-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e5c8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5c8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e5c8-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5e5c8-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5e5c8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e5c8-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5e5c8-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5c8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e5c8-110">Return value</span></span>

<span data-ttu-id="5e5c8-111">Uma DLL de extensão deve retornar zero se ela processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e5c8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e5c8-112">Remarks</span></span>

<span data-ttu-id="5e5c8-113">Os valores *HWND* e **HMENU** passados com as mensagens [**FMEVENT \_ Load**](fmevent-load.md) e [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) podem não ser válidos no momento em que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5c8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e5c8-114">Requirements</span></span>



| <span data-ttu-id="5e5c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e5c8-115">Requirement</span></span> | <span data-ttu-id="5e5c8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5e5c8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5c8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5c8-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e5c8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5e5c8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5c8-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e5c8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e5c8-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5e5c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e5c8-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e5c8-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e5c8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e5c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5c8-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="5e5c8-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




