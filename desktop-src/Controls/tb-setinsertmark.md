---
title: Mensagem de TB_SETINSERTMARK (commctrl. h)
description: Define a marca de inserção atual para a barra de ferramentas.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- Controles de TB_SETINSERTMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085157"
---
# <a name="tb_setinsertmark-message"></a><span data-ttu-id="9f45a-104">TB de \_ mensagem SETINSERTMARK</span><span class="sxs-lookup"><span data-stu-id="9f45a-104">TB\_SETINSERTMARK message</span></span>

<span data-ttu-id="9f45a-105">Define a marca de inserção atual para a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="9f45a-105">Sets the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f45a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f45a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f45a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f45a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9f45a-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9f45a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9f45a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f45a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f45a-110">Ponteiro para uma estrutura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que contém a marca de inserção.</span><span class="sxs-lookup"><span data-stu-id="9f45a-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that contains the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f45a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f45a-111">Return value</span></span>

<span data-ttu-id="9f45a-112">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="9f45a-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f45a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f45a-113">Requirements</span></span>



| <span data-ttu-id="9f45a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f45a-114">Requirement</span></span> | <span data-ttu-id="9f45a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9f45a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f45a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f45a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f45a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f45a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f45a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f45a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f45a-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f45a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f45a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f45a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f45a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f45a-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f45a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f45a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f45a-123">**TB de \_ GETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="9f45a-123">**TB\_GETINSERTMARK**</span></span>](tb-getinsertmark.md)
</dt> </dl>

 

 





