---
title: Mensagem de TB_SETINSERTMARKCOLOR (commctrl. h)
description: Define a cor usada para desenhar a marca de inserção para a barra de ferramentas.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- Controles de TB_SETINSERTMARKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085156"
---
# <a name="tb_setinsertmarkcolor-message"></a><span data-ttu-id="ebf17-104">TB de \_ mensagem SETINSERTMARKCOLOR</span><span class="sxs-lookup"><span data-stu-id="ebf17-104">TB\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="ebf17-105">Define a cor usada para desenhar a marca de inserção para a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ebf17-105">Sets the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebf17-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebf17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebf17-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ebf17-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ebf17-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ebf17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebf17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf17-110">Valor **COLORREF** que contém a nova cor de marca de inserção.</span><span class="sxs-lookup"><span data-stu-id="ebf17-110">**COLORREF** value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf17-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebf17-111">Return value</span></span>

<span data-ttu-id="ebf17-112">Retorna um valor **COLORREF** que contém a cor de marca de inserção anterior.</span><span class="sxs-lookup"><span data-stu-id="ebf17-112">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf17-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebf17-113">Requirements</span></span>



| <span data-ttu-id="ebf17-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebf17-114">Requirement</span></span> | <span data-ttu-id="ebf17-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ebf17-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf17-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf17-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf17-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ebf17-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ebf17-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf17-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf17-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ebf17-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ebf17-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebf17-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf17-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf17-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf17-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebf17-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf17-123">**TB de \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="ebf17-123">**TB\_GETINSERTMARKCOLOR**</span></span>](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





