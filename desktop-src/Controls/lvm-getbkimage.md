---
title: Mensagem de LVM_GETBKIMAGE (commctrl. h)
description: Obtém a imagem de plano de fundo em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetBkImage do ListView.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- Controles de LVM_GETBKIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644264"
---
# <a name="lvm_getbkimage-message"></a><span data-ttu-id="f2d96-105">\_Mensagem GETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="f2d96-105">LVM\_GETBKIMAGE message</span></span>

<span data-ttu-id="f2d96-106">Obtém a imagem de plano de fundo em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="f2d96-106">Gets the background image in a list-view control.</span></span> <span data-ttu-id="f2d96-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetBkImage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .</span><span class="sxs-lookup"><span data-stu-id="f2d96-107">You can send this message explicitly or by using the [**ListView\_GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2d96-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2d96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d96-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2d96-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2d96-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f2d96-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2d96-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2d96-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d96-112">Um ponteiro para uma estrutura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que receberá as informações da imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="f2d96-112">A pointer to an [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that will receive the background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2d96-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2d96-113">Return value</span></span>

<span data-ttu-id="f2d96-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="f2d96-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d96-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2d96-115">Requirements</span></span>



| <span data-ttu-id="f2d96-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2d96-116">Requirement</span></span> | <span data-ttu-id="f2d96-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f2d96-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d96-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2d96-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d96-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2d96-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2d96-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2d96-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d96-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2d96-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2d96-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2d96-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d96-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2d96-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f2d96-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f2d96-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f2d96-125">**LVM \_ GETBKIMAGEW** (Unicode) e **LVM \_ GETBKIMAGEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f2d96-125">**LVM\_GETBKIMAGEW** (Unicode) and **LVM\_GETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f2d96-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f2d96-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d96-127">**\_SETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="f2d96-127">**LVM\_SETBKIMAGE**</span></span>](lvm-setbkimage.md)
</dt> </dl>

 

 





