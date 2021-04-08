---
title: Mensagem de LVM_SETCOLUMNORDERARRAY (commctrl. h)
description: Define a ordem da esquerda para a direita de colunas em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetColumnOrderArray do ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Controles de LVM_SETCOLUMNORDERARRAY de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008859"
---
# <a name="lvm_setcolumnorderarray-message"></a><span data-ttu-id="5bb02-105">\_Mensagem SETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="5bb02-105">LVM\_SETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="5bb02-106">Define a ordem da esquerda para a direita de colunas em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="5bb02-106">Sets the left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="5bb02-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetColumnOrderArray do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="5bb02-107">You can send this message explicitly or use the [**ListView\_SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5bb02-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bb02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb02-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5bb02-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5bb02-110">Tamanho, em elementos, do buffer em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="5bb02-110">Size, in elements, of the buffer at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="5bb02-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5bb02-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5bb02-112">Ponteiro para uma matriz que especifica a ordem na qual as colunas devem ser exibidas, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="5bb02-112">Pointer to an array that specifies the order in which columns should be displayed, from left to right.</span></span> <span data-ttu-id="5bb02-113">Por exemplo, se o conteúdo da matriz for {2,0,1} , o controle exibirá coluna 2, coluna 0 e coluna 1 nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="5bb02-113">For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1 in that order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb02-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bb02-114">Return value</span></span>

<span data-ttu-id="5bb02-115">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="5bb02-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb02-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bb02-116">Requirements</span></span>



| <span data-ttu-id="5bb02-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb02-117">Requirement</span></span> | <span data-ttu-id="5bb02-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5bb02-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb02-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bb02-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb02-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bb02-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5bb02-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bb02-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb02-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5bb02-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5bb02-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bb02-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bb02-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bb02-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





