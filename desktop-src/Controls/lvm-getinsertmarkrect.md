---
title: Mensagem de LVM_GETINSERTMARKRECT (commctrl. h)
description: Recupera o retângulo que limita o ponto de inserção.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- Controles de LVM_GETINSERTMARKRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918974"
---
# <a name="lvm_getinsertmarkrect-message"></a><span data-ttu-id="87f5a-104">\_Mensagem GETINSERTMARKRECT LVM</span><span class="sxs-lookup"><span data-stu-id="87f5a-104">LVM\_GETINSERTMARKRECT message</span></span>

<span data-ttu-id="87f5a-105">Recupera o retângulo que limita o ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="87f5a-105">Retrieves the rectangle that bounds the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="87f5a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87f5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f5a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87f5a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="87f5a-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="87f5a-108">Not used; must be zero.</span></span></dd> <dt>

<span data-ttu-id="87f5a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87f5a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87f5a-110">Ponteiro para uma estrutura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> que contém as coordenadas de um retângulo que limita o ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="87f5a-110">Pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure that contains the coordinates of a rectangle that bounds the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f5a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87f5a-111">Return value</span></span>

<span data-ttu-id="87f5a-112">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="87f5a-112">Returns one of the following values.</span></span>



| <span data-ttu-id="87f5a-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="87f5a-113">Return code</span></span>                                                                      | <span data-ttu-id="87f5a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="87f5a-114">Description</span></span>                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="87f5a-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="87f5a-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="87f5a-116">Nenhum ponto de inserção encontrado.</span><span class="sxs-lookup"><span data-stu-id="87f5a-116">No insertion point found.</span></span><br/> |
| <dl> <span data-ttu-id="87f5a-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="87f5a-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="87f5a-118">Ponto de inserção encontrado.</span><span class="sxs-lookup"><span data-stu-id="87f5a-118">Insertion point found.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="87f5a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="87f5a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87f5a-120">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="87f5a-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="87f5a-121">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="87f5a-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87f5a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87f5a-122">Requirements</span></span>



| <span data-ttu-id="87f5a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="87f5a-123">Requirement</span></span> | <span data-ttu-id="87f5a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="87f5a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87f5a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87f5a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="87f5a-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87f5a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87f5a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87f5a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="87f5a-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87f5a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87f5a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87f5a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f5a-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87f5a-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

