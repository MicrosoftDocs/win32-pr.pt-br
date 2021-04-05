---
title: Mensagem de MCIWNDM_NOTIFYSIZE (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYSIZE notifica a janela pai de um aplicativo que o tamanho da janela foi alterado.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYSIZE
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085440"
---
# <a name="mciwndm_notifysize-message"></a><span data-ttu-id="7c1f2-104">\_Mensagem MCIWNDM NOTIFYSIZE</span><span class="sxs-lookup"><span data-stu-id="7c1f2-104">MCIWNDM\_NOTIFYSIZE message</span></span>

<span data-ttu-id="7c1f2-105">A mensagem **MCIWNDM \_ NOTIFYSIZE** notifica a janela pai de um aplicativo que o tamanho da janela foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-105">The **MCIWNDM\_NOTIFYSIZE** message notifies the parent window of an application that the window size has changed.</span></span>


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="7c1f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c1f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c1f2-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="7c1f2-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="7c1f2-108">Manipule a janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-108">Handle to the MCIWnd window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c1f2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c1f2-109">Remarks</span></span>

<span data-ttu-id="7c1f2-110">Você pode habilitar a notificação de alterações no tamanho de uma janela MCIWnd especificando o estilo de \_ janela MCIWNDF NOTIFYSIZE.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-110">You can enable notification of changes in the size of an MCIWnd window by specifying the MCIWNDF\_NOTIFYSIZE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1f2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c1f2-111">Requirements</span></span>



| <span data-ttu-id="7c1f2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c1f2-112">Requirement</span></span> | <span data-ttu-id="7c1f2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7c1f2-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7c1f2-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c1f2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1f2-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c1f2-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7c1f2-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c1f2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1f2-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c1f2-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7c1f2-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c1f2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c1f2-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c1f2-119"><dt>Vfw.h</dt></span></span> </dl> |



 

 





