---
title: Mensagem de MCIWNDM_NOTIFYPOS (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYPOS notifica a janela pai de um aplicativo que a posição da janela foi alterada.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYPOS
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918951"
---
# <a name="mciwndm_notifypos-message"></a><span data-ttu-id="6ca83-104">\_Mensagem MCIWNDM NOTIFYPOS</span><span class="sxs-lookup"><span data-stu-id="6ca83-104">MCIWNDM\_NOTIFYPOS message</span></span>

<span data-ttu-id="6ca83-105">A mensagem **MCIWNDM \_ NOTIFYPOS** notifica a janela pai de um aplicativo que a posição da janela foi alterada.</span><span class="sxs-lookup"><span data-stu-id="6ca83-105">The **MCIWNDM\_NOTIFYPOS** message notifies the parent window of an application that the window position has changed.</span></span>


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a><span data-ttu-id="6ca83-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ca83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca83-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="6ca83-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="6ca83-108">Manipule a janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6ca83-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="6ca83-109"><span id="pos"></span><span id="POS"></span>*pos*</span><span class="sxs-lookup"><span data-stu-id="6ca83-109"><span id="pos"></span><span id="POS"></span>*pos*</span></span>
</dt> <dd>

<span data-ttu-id="6ca83-110">Descreve a nova posição.</span><span class="sxs-lookup"><span data-stu-id="6ca83-110">Describes the new position.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ca83-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ca83-111">Remarks</span></span>

<span data-ttu-id="6ca83-112">Você pode habilitar a notificação de alterações na posição de uma janela MCIWnd especificando o estilo de \_ janela MCIWNDF NOTIFYPOS.</span><span class="sxs-lookup"><span data-stu-id="6ca83-112">You can enable notification of changes in the position of an MCIWnd window by specifying the MCIWNDF\_NOTIFYPOS window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca83-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ca83-113">Requirements</span></span>



| <span data-ttu-id="6ca83-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ca83-114">Requirement</span></span> | <span data-ttu-id="6ca83-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6ca83-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ca83-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca83-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca83-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ca83-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6ca83-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca83-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca83-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ca83-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6ca83-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ca83-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca83-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca83-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





