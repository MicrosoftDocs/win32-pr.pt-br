---
title: Mensagem de PBM_GETSTATE (commctrl. h)
description: Obtém o estado da barra de progresso.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- Controles de PBM_GETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918794"
---
# <a name="pbm_getstate-message"></a><span data-ttu-id="726e9-104">\_Mensagem GETstate do PBM</span><span class="sxs-lookup"><span data-stu-id="726e9-104">PBM\_GETSTATE message</span></span>

<span data-ttu-id="726e9-105">Obtém o estado da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="726e9-105">Gets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="726e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="726e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="726e9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="726e9-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="726e9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="726e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="726e9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="726e9-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="726e9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726e9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="726e9-111">Return value</span></span>

<span data-ttu-id="726e9-112">Retorna o estado atual da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="726e9-112">Returns the current state of the progress bar.</span></span> <span data-ttu-id="726e9-113">Um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="726e9-113">One of the following values.</span></span>



| <span data-ttu-id="726e9-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="726e9-114">Return code</span></span>                                                                                 | <span data-ttu-id="726e9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="726e9-115">Description</span></span>             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="726e9-116"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="726e9-116"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="726e9-117">Em andamento.</span><span class="sxs-lookup"><span data-stu-id="726e9-117">In progress.</span></span><br/> |
| <dl> <span data-ttu-id="726e9-118"><dt>**erro de PBST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="726e9-118"><dt>**PBST\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="726e9-119">Erro.</span><span class="sxs-lookup"><span data-stu-id="726e9-119">Error.</span></span><br/>       |
| <dl> <span data-ttu-id="726e9-120"><dt>**PBST em \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="726e9-120"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="726e9-121">Em pausa.</span><span class="sxs-lookup"><span data-stu-id="726e9-121">Paused.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="726e9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726e9-122">Requirements</span></span>



| <span data-ttu-id="726e9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="726e9-123">Requirement</span></span> | <span data-ttu-id="726e9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="726e9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="726e9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726e9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="726e9-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="726e9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="726e9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726e9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="726e9-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="726e9-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="726e9-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="726e9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="726e9-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="726e9-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





