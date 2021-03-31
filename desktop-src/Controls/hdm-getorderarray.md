---
title: Mensagem de HDM_GETORDERARRAY (commctrl. h)
description: Obtém a ordem da esquerda para a direita atual de itens em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetOrderArray do cabeçalho.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- Controles de HDM_GETORDERARRAY de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085586"
---
# <a name="hdm_getorderarray-message"></a><span data-ttu-id="b984f-105">\_Mensagem HDM GETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="b984f-105">HDM\_GETORDERARRAY message</span></span>

<span data-ttu-id="b984f-106">Obtém a ordem da esquerda para a direita atual de itens em um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b984f-106">Gets the current left-to-right order of items in a header control.</span></span> <span data-ttu-id="b984f-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetOrderArray do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .</span><span class="sxs-lookup"><span data-stu-id="b984f-107">You can send this message explicitly or use the [**Header\_GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b984f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b984f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b984f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b984f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b984f-110">O número de elementos inteiros que o *lParam* pode conter.</span><span class="sxs-lookup"><span data-stu-id="b984f-110">The number of integer elements that *lParam* can hold.</span></span> <span data-ttu-id="b984f-111">Esse valor deve ser igual ao número de itens no controle (consulte [**HDM \_ GetItemCount**](hdm-getitemcount.md)).</span><span class="sxs-lookup"><span data-stu-id="b984f-111">This value must be equal to the number of items in the control (see [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b984f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b984f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b984f-113">Um ponteiro para uma matriz de inteiros que recebe os valores de índice para itens no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b984f-113">A pointer to an array of integers that receive the index values for items in the header.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b984f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b984f-114">Return value</span></span>

<span data-ttu-id="b984f-115">Retornará zero se for bem-sucedido e o buffer em *lParam* receberá o número do item para cada item no controle de cabeçalho na ordem em que eles aparecem da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="b984f-115">Returns nonzero if successful, and the buffer at *lParam* receives the item number for each item in the header control in the order in which they appear from left to right.</span></span> <span data-ttu-id="b984f-116">Caso contrário, a mensagem retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b984f-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b984f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b984f-117">Remarks</span></span>

<span data-ttu-id="b984f-118">O número de elementos em *lParam* é especificado em *wParam* e deve ser igual ao número de itens no controle.</span><span class="sxs-lookup"><span data-stu-id="b984f-118">The number of elements in *lParam* is specified in *wParam* and must be equal to the number of items in the control.</span></span> <span data-ttu-id="b984f-119">Por exemplo, o fragmento de código a seguir reservará memória suficiente para manter os valores de índice.</span><span class="sxs-lookup"><span data-stu-id="b984f-119">For example, the following code fragment will reserve enough memory to hold the index values.</span></span>


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a><span data-ttu-id="b984f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b984f-120">Requirements</span></span>



| <span data-ttu-id="b984f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b984f-121">Requirement</span></span> | <span data-ttu-id="b984f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b984f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b984f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b984f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b984f-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b984f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b984f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b984f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b984f-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b984f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b984f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b984f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b984f-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b984f-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





