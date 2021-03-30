---
title: Mensagem de LVM_SETBKIMAGE (commctrl. h)
description: Define a imagem de plano de fundo em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetBkImage do ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Controles de LVM_SETBKIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455429"
---
# <a name="lvm_setbkimage-message"></a><span data-ttu-id="a6297-105">\_Mensagem SETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="a6297-105">LVM\_SETBKIMAGE message</span></span>

<span data-ttu-id="a6297-106">Define a imagem de plano de fundo em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="a6297-106">Sets the background image in a list-view control.</span></span> <span data-ttu-id="a6297-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetBkImage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .</span><span class="sxs-lookup"><span data-stu-id="a6297-107">You can send this message explicitly or by using the [**ListView\_SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6297-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6297-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6297-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6297-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6297-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a6297-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a6297-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6297-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6297-112">Ponteiro para uma estrutura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que contém as novas informações da imagem de fundo.</span><span class="sxs-lookup"><span data-stu-id="a6297-112">Pointer to a [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that contains the new background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6297-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6297-113">Return value</span></span>

<span data-ttu-id="a6297-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="a6297-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="a6297-115">Retornará zero se o membro **ulFlags** da estrutura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) for **LVBKIF \_ Source \_ None**.</span><span class="sxs-lookup"><span data-stu-id="a6297-115">Returns zero if the **ulFlags** member of the [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure is **LVBKIF\_SOURCE\_NONE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6297-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6297-116">Remarks</span></span>

<span data-ttu-id="a6297-117">Como o controle List-View usa OLE COM para manipular as imagens de plano de fundo, o aplicativo de chamada deve chamar [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de enviar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="a6297-117">Because the list-view control uses OLE COM to manipulate the background images, the calling application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before sending this message.</span></span> <span data-ttu-id="a6297-118">É melhor chamar uma dessas funções quando o aplicativo é inicializado e chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) ou [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) quando o aplicativo estiver sendo encerrado.</span><span class="sxs-lookup"><span data-stu-id="a6297-118">It is best to call one of these functions when the application is initialized and call either [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) or [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) when the application is terminating.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6297-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6297-119">Requirements</span></span>



| <span data-ttu-id="a6297-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6297-120">Requirement</span></span> | <span data-ttu-id="a6297-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a6297-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6297-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6297-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6297-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6297-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6297-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6297-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6297-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6297-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6297-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6297-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6297-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6297-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a6297-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a6297-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a6297-129">**LVM \_ SETBKIMAGEW** (Unicode) e **LVM \_ SETBKIMAGEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a6297-129">**LVM\_SETBKIMAGEW** (Unicode) and **LVM\_SETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a6297-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a6297-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6297-131">**\_GETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="a6297-131">**LVM\_GETBKIMAGE**</span></span>](lvm-getbkimage.md)
</dt> </dl>

 

