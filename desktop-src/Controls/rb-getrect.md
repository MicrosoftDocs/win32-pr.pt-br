---
title: Mensagem de RB_GETRECT (commctrl. h)
description: Recupera o retângulo delimitador para uma determinada faixa em um controle rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- Controles de RB_GETRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163598"
---
# <a name="rb_getrect-message"></a><span data-ttu-id="f4ed1-104">\_Mensagem de GETRECT RB</span><span class="sxs-lookup"><span data-stu-id="f4ed1-104">RB\_GETRECT message</span></span>

<span data-ttu-id="f4ed1-105">Recupera o retângulo delimitador para uma determinada faixa em um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="f4ed1-105">Retrieves the bounding rectangle for a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4ed1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ed1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4ed1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ed1-108">Índice de base zero de uma banda no controle rebar.</span><span class="sxs-lookup"><span data-stu-id="f4ed1-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="f4ed1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4ed1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ed1-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá os limites da faixa Rebar.</span><span class="sxs-lookup"><span data-stu-id="f4ed1-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounds of the rebar band.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ed1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4ed1-111">Return value</span></span>

<span data-ttu-id="f4ed1-112">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="f4ed1-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ed1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4ed1-113">Requirements</span></span>



| <span data-ttu-id="f4ed1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ed1-114">Requirement</span></span> | <span data-ttu-id="f4ed1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f4ed1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ed1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ed1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ed1-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4ed1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4ed1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ed1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ed1-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4ed1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4ed1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4ed1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ed1-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ed1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

