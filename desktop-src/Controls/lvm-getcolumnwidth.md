---
title: Mensagem de LVM_GETCOLUMNWIDTH (commctrl. h)
description: Obtém a largura de uma coluna no modo de exibição de relatório ou de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetColumnWidth do ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Controles de LVM_GETCOLUMNWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085173"
---
# <a name="lvm_getcolumnwidth-message"></a><span data-ttu-id="1f96b-105">\_Mensagem GETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="1f96b-105">LVM\_GETCOLUMNWIDTH message</span></span>

<span data-ttu-id="1f96b-106">Obtém a largura de uma coluna no modo de exibição de relatório ou de lista.</span><span class="sxs-lookup"><span data-stu-id="1f96b-106">Gets the width of a column in report or list view.</span></span> <span data-ttu-id="1f96b-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetColumnWidth do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="1f96b-107">You can send this message explicitly or by using the [**ListView\_GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f96b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f96b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f96b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f96b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f96b-110">O índice da coluna.</span><span class="sxs-lookup"><span data-stu-id="1f96b-110">The index of the column.</span></span> <span data-ttu-id="1f96b-111">Esse parâmetro é ignorado na exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="1f96b-111">This parameter is ignored in list view.</span></span>

</dd> <dt>

<span data-ttu-id="1f96b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f96b-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1f96b-113">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1f96b-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f96b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f96b-114">Return value</span></span>

<span data-ttu-id="1f96b-115">Retorna a largura da coluna se for bem-sucedida ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1f96b-115">Returns the column width if successful, or zero otherwise.</span></span> <span data-ttu-id="1f96b-116">Se essa mensagem for enviada a um controle de exibição de lista com o estilo de [**\_ relatório LVS**](list-view-window-styles.md) e a coluna especificada não existir, o valor de retorno será indefinido.</span><span class="sxs-lookup"><span data-stu-id="1f96b-116">If this message is sent to a list-view control with the [**LVS\_REPORT**](list-view-window-styles.md) style and the specified column does not exist, the return value is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f96b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f96b-117">Requirements</span></span>



| <span data-ttu-id="1f96b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f96b-118">Requirement</span></span> | <span data-ttu-id="1f96b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1f96b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f96b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f96b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f96b-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f96b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f96b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f96b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f96b-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f96b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f96b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f96b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f96b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f96b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





