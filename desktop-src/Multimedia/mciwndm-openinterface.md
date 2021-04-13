---
title: Mensagem de MCIWNDM_OPENINTERFACE (VFW. h)
description: A \_ mensagem MCIWNDM OPENINTERFACE anexa o fluxo de dados ou o arquivo associado à interface especificada a uma janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- Multimídia do Windows de mensagem MCIWNDM_OPENINTERFACE
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369211"
---
# <a name="mciwndm_openinterface-message"></a><span data-ttu-id="9ffea-105">\_Mensagem MCIWNDM OPENINTERFACE</span><span class="sxs-lookup"><span data-stu-id="9ffea-105">MCIWNDM\_OPENINTERFACE message</span></span>

<span data-ttu-id="9ffea-106">A mensagem **MCIWNDM \_ OPENINTERFACE** anexa o fluxo de dados ou o arquivo associado à interface especificada a uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="9ffea-106">The **MCIWNDM\_OPENINTERFACE** message attaches the data stream or file associated with the specified interface to an MCIWnd window.</span></span> <span data-ttu-id="9ffea-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="9ffea-107">You can send this message explicitly or by using the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span>


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a><span data-ttu-id="9ffea-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ffea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ffea-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span><span class="sxs-lookup"><span data-stu-id="9ffea-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span></span>
</dt> <dd>

<span data-ttu-id="9ffea-110">Ponteiro para uma interface IAVI que aponta para um arquivo ou um fluxo de dados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9ffea-110">Pointer to an IAVI interface that points to a file or a data stream in a file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ffea-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9ffea-111">Return Value</span></span>

<span data-ttu-id="9ffea-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9ffea-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ffea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ffea-113">Requirements</span></span>



| <span data-ttu-id="9ffea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ffea-114">Requirement</span></span> | <span data-ttu-id="9ffea-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9ffea-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9ffea-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ffea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffea-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ffea-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9ffea-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ffea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffea-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ffea-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9ffea-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9ffea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ffea-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ffea-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ffea-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ffea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffea-123">**MCIWndOpenInterface**</span><span class="sxs-lookup"><span data-stu-id="9ffea-123">**MCIWndOpenInterface**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





