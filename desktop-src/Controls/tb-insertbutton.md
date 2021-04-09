---
title: Mensagem de TB_INSERTBUTTON (commctrl. h)
description: Insere um botão em uma barra de ferramentas.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- Controles de TB_INSERTBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085394"
---
# <a name="tb_insertbutton-message"></a><span data-ttu-id="8e253-104">TB de \_ mensagem INSERTBUTTON</span><span class="sxs-lookup"><span data-stu-id="8e253-104">TB\_INSERTBUTTON message</span></span>

<span data-ttu-id="8e253-105">Insere um botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="8e253-105">Inserts a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e253-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e253-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e253-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e253-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e253-108">Índice baseado em zero de um botão.</span><span class="sxs-lookup"><span data-stu-id="8e253-108">Zero-based index of a button.</span></span> <span data-ttu-id="8e253-109">A mensagem insere o botão novo à esquerda deste botão.</span><span class="sxs-lookup"><span data-stu-id="8e253-109">The message inserts the new button to the left of this button.</span></span>

</dd> <dt>

<span data-ttu-id="8e253-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e253-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e253-111">Ponteiro para uma estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contém informações sobre o botão a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="8e253-111">Pointer to a [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure containing information about the button to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e253-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e253-112">Return value</span></span>

<span data-ttu-id="8e253-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8e253-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e253-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e253-114">Requirements</span></span>



| <span data-ttu-id="8e253-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e253-115">Requirement</span></span> | <span data-ttu-id="8e253-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8e253-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e253-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e253-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e253-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e253-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e253-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e253-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e253-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e253-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e253-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e253-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e253-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e253-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8e253-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8e253-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8e253-124">**TB \_ INSERTBUTTONW** (Unicode) e **TB \_ INSERTBUTTONA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8e253-124">**TB\_INSERTBUTTONW** (Unicode) and **TB\_INSERTBUTTONA** (ANSI)</span></span><br/>           |



 

 





