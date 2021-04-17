---
title: Mensagem de TB_GETMAXSIZE (commctrl. h)
description: Recupera o tamanho total de todos os botões e separadores visíveis na barra de ferramentas.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- Controles de TB_GETMAXSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755649"
---
# <a name="tb_getmaxsize-message"></a><span data-ttu-id="e791d-104">Mensagem de TB \_ GETmaxsize</span><span class="sxs-lookup"><span data-stu-id="e791d-104">TB\_GETMAXSIZE message</span></span>

<span data-ttu-id="e791d-105">Recupera o tamanho total de todos os botões e separadores visíveis na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e791d-105">Retrieves the total size of all of the visible buttons and separators in the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e791d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e791d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e791d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e791d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e791d-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e791d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e791d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e791d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e791d-110">Ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) que recebe o tamanho dos itens.</span><span class="sxs-lookup"><span data-stu-id="e791d-110">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the size of the items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e791d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e791d-111">Return value</span></span>

<span data-ttu-id="e791d-112">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="e791d-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e791d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e791d-113">Requirements</span></span>



| <span data-ttu-id="e791d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e791d-114">Requirement</span></span> | <span data-ttu-id="e791d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e791d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e791d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e791d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e791d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e791d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e791d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e791d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e791d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e791d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e791d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e791d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e791d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e791d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

