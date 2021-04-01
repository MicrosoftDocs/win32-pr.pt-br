---
title: Mensagem de MCIWNDM_NOTIFYMEDIA (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYMEDIA notifica a janela pai de um aplicativo que a mídia foi alterada.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYMEDIA
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644562"
---
# <a name="mciwndm_notifymedia-message"></a><span data-ttu-id="7352e-104">\_Mensagem MCIWNDM NOTIFYMEDIA</span><span class="sxs-lookup"><span data-stu-id="7352e-104">MCIWNDM\_NOTIFYMEDIA message</span></span>

<span data-ttu-id="7352e-105">A mensagem **MCIWNDM \_ NOTIFYMEDIA** notifica a janela pai de um aplicativo que a mídia foi alterada.</span><span class="sxs-lookup"><span data-stu-id="7352e-105">The **MCIWNDM\_NOTIFYMEDIA** message notifies the parent window of an application that the media has changed.</span></span>


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="7352e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7352e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7352e-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="7352e-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="7352e-108">Manipule a janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="7352e-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="7352e-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="7352e-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="7352e-110">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o novo nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7352e-110">Pointer to a null-terminated string containing the new filename.</span></span> <span data-ttu-id="7352e-111">Se a mídia estiver sendo fechada, ela especificará uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="7352e-111">If the media is closing, it specifies a null string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7352e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7352e-112">Remarks</span></span>

<span data-ttu-id="7352e-113">Você pode habilitar a notificação de alterações de mídia especificando o \_ estilo de janela MCIWNDF NOTIFYMEDIA.</span><span class="sxs-lookup"><span data-stu-id="7352e-113">You can enable notification of media changes by specifying the MCIWNDF\_NOTIFYMEDIA window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="7352e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7352e-114">Requirements</span></span>



| <span data-ttu-id="7352e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7352e-115">Requirement</span></span> | <span data-ttu-id="7352e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7352e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7352e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7352e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7352e-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7352e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7352e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7352e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7352e-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7352e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7352e-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7352e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7352e-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7352e-122"><dt>Vfw.h</dt></span></span> </dl> |



 

 





