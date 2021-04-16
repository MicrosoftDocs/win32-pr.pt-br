---
title: Mensagem de RB_IDTOINDEX (commctrl. h)
description: Converte um identificador de banda em um índice de faixa em um controle rebar.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- Controles de RB_IDTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454689"
---
# <a name="rb_idtoindex-message"></a><span data-ttu-id="bf893-104">\_Mensagem IDTOINDEX RB</span><span class="sxs-lookup"><span data-stu-id="bf893-104">RB\_IDTOINDEX message</span></span>

<span data-ttu-id="bf893-105">Converte um identificador de banda em um índice de faixa em um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="bf893-105">Converts a band identifier to a band index in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf893-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf893-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf893-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf893-108">O identificador definido pelo aplicativo da banda em questão.</span><span class="sxs-lookup"><span data-stu-id="bf893-108">The application-defined identifier of the band in question.</span></span> <span data-ttu-id="bf893-109">Esse é o valor que foi passado no membro **wid** da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) quando a banda foi inserida.</span><span class="sxs-lookup"><span data-stu-id="bf893-109">This is the value that was passed in the **wID** member of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure when the band was inserted.</span></span>

</dd> <dt>

<span data-ttu-id="bf893-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf893-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bf893-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bf893-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf893-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf893-112">Return value</span></span>

<span data-ttu-id="bf893-113">Retorna o índice de faixa com base em zero se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bf893-113">Returns the zero-based band index if successful, or -1 otherwise.</span></span> <span data-ttu-id="bf893-114">Se existirem identificadores de banda duplicados, o primeiro será retornado.</span><span class="sxs-lookup"><span data-stu-id="bf893-114">If duplicate band identifiers exist, the first one is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf893-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf893-115">Requirements</span></span>



| <span data-ttu-id="bf893-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf893-116">Requirement</span></span> | <span data-ttu-id="bf893-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bf893-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf893-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf893-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf893-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf893-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf893-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf893-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf893-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf893-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf893-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf893-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf893-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf893-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





