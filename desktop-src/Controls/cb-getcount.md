---
title: Mensagem de CB_GETCOUNT (WinUser. h)
description: Obtém o número de itens na caixa de listagem de uma caixa de combinação.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- Controles de CB_GETCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645279"
---
# <a name="cb_getcount-message"></a><span data-ttu-id="a6a1a-104">\_Mensagem de GETCOUNT CB</span><span class="sxs-lookup"><span data-stu-id="a6a1a-104">CB\_GETCOUNT message</span></span>

<span data-ttu-id="a6a1a-105">Obtém o número de itens na caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="a6a1a-105">Gets the number of items in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6a1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6a1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a1a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6a1a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a1a-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a6a1a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a6a1a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6a1a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a1a-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a6a1a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a1a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6a1a-111">Return value</span></span>

<span data-ttu-id="a6a1a-112">O valor de retorno é o número de itens na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="a6a1a-112">The return value is the number of items in the list box.</span></span> <span data-ttu-id="a6a1a-113">Se ocorrer um erro, será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="a6a1a-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a1a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6a1a-114">Remarks</span></span>

<span data-ttu-id="a6a1a-115">O índice é baseado em zero, portanto, a contagem retornada é maior que o valor de índice do último item.</span><span class="sxs-lookup"><span data-stu-id="a6a1a-115">The index is zero-based, so the returned count is one greater than the index value of the last item.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a1a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6a1a-116">Requirements</span></span>



| <span data-ttu-id="a6a1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a1a-117">Requirement</span></span> | <span data-ttu-id="a6a1a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a6a1a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a1a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6a1a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a1a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6a1a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a6a1a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6a1a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a1a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6a1a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a6a1a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6a1a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a1a-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6a1a-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





