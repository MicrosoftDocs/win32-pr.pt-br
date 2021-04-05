---
title: LVN_COLUMNCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um cabeçalho de coluna foi clicado enquanto o controle de exibição de lista estava no modo de relatório. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008930"
---
# <a name="lvn_columnclick-notification-code"></a><span data-ttu-id="1fcff-105">Código de notificação do LVN \_ COLUMNCLICK</span><span class="sxs-lookup"><span data-stu-id="1fcff-105">LVN\_COLUMNCLICK notification code</span></span>

<span data-ttu-id="1fcff-106">Notifica uma janela pai do controle de exibição de lista que um cabeçalho de coluna foi clicado enquanto o controle de exibição de lista estava no modo de relatório.</span><span class="sxs-lookup"><span data-stu-id="1fcff-106">Notifies a list-view control's parent window that a column header was clicked while the list-view control was in report mode.</span></span> <span data-ttu-id="1fcff-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcff-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1fcff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fcff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fcff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fcff-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="1fcff-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="1fcff-111">O membro **iItem** é-1 e o membro **iSubItem** identifica a coluna.</span><span class="sxs-lookup"><span data-stu-id="1fcff-111">The **iItem** member is -1, and the **iSubItem** member identifies the column.</span></span> <span data-ttu-id="1fcff-112">Todos os outros membros são zero.</span><span class="sxs-lookup"><span data-stu-id="1fcff-112">All other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcff-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fcff-113">Return value</span></span>

<span data-ttu-id="1fcff-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1fcff-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcff-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fcff-115">Remarks</span></span>

<span data-ttu-id="1fcff-116">Usar formatos de controle de cabeçalho, como a \_ caixa de seleção HDF, para modificar o formato dos cabeçalhos de coluna em um controle de exibição de lista, faz com que o controle envie o código de notificação [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) em vez de LVN \_ COLUMNCLICK quando um item de cabeçalho é clicado.</span><span class="sxs-lookup"><span data-stu-id="1fcff-116">Using header control formats such as HDF\_CHECKBOX to modify the format of column headers in a list-view control causes the control to send the [HDN\_ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) notification code instead of LVN\_COLUMNCLICK when a header item is clicked.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcff-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcff-117">Requirements</span></span>



| <span data-ttu-id="1fcff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcff-118">Requirement</span></span> | <span data-ttu-id="1fcff-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1fcff-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcff-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fcff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1fcff-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1fcff-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1fcff-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fcff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1fcff-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fcff-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1fcff-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fcff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fcff-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcff-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





