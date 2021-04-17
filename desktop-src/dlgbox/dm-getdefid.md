---
title: Mensagem de DM_GETDEFID (WinUser. h)
description: Recupera o identificador do controle de botão de ação padrão de uma caixa de diálogo.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- Caixas de diálogo de DM_GETDEFID mensagem
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499742"
---
# <a name="dm_getdefid-message"></a><span data-ttu-id="200b4-104">\_Mensagem DM GETDEFID</span><span class="sxs-lookup"><span data-stu-id="200b4-104">DM\_GETDEFID message</span></span>

<span data-ttu-id="200b4-105">Recupera o identificador do controle de botão de ação padrão de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="200b4-105">Retrieves the identifier of the default push button control for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a><span data-ttu-id="200b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="200b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="200b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="200b4-108">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="200b4-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="200b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="200b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="200b4-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="200b4-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200b4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="200b4-111">Return value</span></span>

<span data-ttu-id="200b4-112">Se houver um botão de ação padrão, a palavra de ordem superior do valor de retorno conterá o valor **DC \_ HASDEFID** e a palavra de ordem inferior conterá o identificador de controle.</span><span class="sxs-lookup"><span data-stu-id="200b4-112">If a default push button exists, the high-order word of the return value contains the value **DC\_HASDEFID** and the low-order word contains the control identifier.</span></span> <span data-ttu-id="200b4-113">Caso contrário, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="200b4-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="200b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="200b4-114">Remarks</span></span>

<span data-ttu-id="200b4-115">A função [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) processa essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="200b4-115">The [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="200b4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="200b4-116">Requirements</span></span>



| <span data-ttu-id="200b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="200b4-117">Requirement</span></span> | <span data-ttu-id="200b4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="200b4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200b4-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="200b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="200b4-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="200b4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="200b4-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="200b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="200b4-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="200b4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="200b4-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="200b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="200b4-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="200b4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200b4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="200b4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="200b4-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="200b4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="200b4-127">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="200b4-127">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="200b4-128">**\_SETDEFID DM**</span><span class="sxs-lookup"><span data-stu-id="200b4-128">**DM\_SETDEFID**</span></span>](dm-setdefid.md)
</dt> <dt>

<span data-ttu-id="200b4-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="200b4-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="200b4-130">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="200b4-130">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





