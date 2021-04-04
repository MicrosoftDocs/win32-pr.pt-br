---
title: Mensagem de LVM_GETCOLUMNORDERARRAY (commctrl. h)
description: Obtém a ordem da esquerda para a direita atual de colunas em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetColumnOrderArray do ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Controles de LVM_GETCOLUMNORDERARRAY de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008867"
---
# <a name="lvm_getcolumnorderarray-message"></a><span data-ttu-id="3625c-105">\_Mensagem GETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="3625c-105">LVM\_GETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="3625c-106">Obtém a ordem da esquerda para a direita atual de colunas em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="3625c-106">Gets the current left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="3625c-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetColumnOrderArray do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="3625c-107">You can send this message explicitly or use the [**ListView\_GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3625c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3625c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3625c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3625c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3625c-110">O número de colunas no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="3625c-110">The number of columns in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="3625c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3625c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3625c-112">Um ponteiro para uma matriz de inteiros que recebe os valores de índice das colunas no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="3625c-112">A pointer to an array of integers that receives the index values of the columns in the list-view control.</span></span> <span data-ttu-id="3625c-113">A matriz deve ser grande o suficiente para conter elementos *wParam* .</span><span class="sxs-lookup"><span data-stu-id="3625c-113">The array must be large enough to hold *wParam* elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3625c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3625c-114">Return value</span></span>

<span data-ttu-id="3625c-115">Se for bem-sucedido, retornará zero e o buffer em *lParam* receberá o índice de coluna de cada coluna no controle na ordem em que aparecem da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="3625c-115">If successful, returns nonzero, and the buffer at *lParam* receives the column index of each column in the control in the order they appear from left to right.</span></span> <span data-ttu-id="3625c-116">Caso contrário, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="3625c-116">Otherwise, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3625c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3625c-117">Requirements</span></span>



| <span data-ttu-id="3625c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3625c-118">Requirement</span></span> | <span data-ttu-id="3625c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3625c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3625c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3625c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3625c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3625c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3625c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3625c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3625c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3625c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3625c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3625c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3625c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3625c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





