---
title: Mensagem de TTM_GETMAXTIPWIDTH (commctrl. h)
description: Recupera a largura máxima de uma janela de dica de ferramenta.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- Controles de TTM_GETMAXTIPWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918468"
---
# <a name="ttm_getmaxtipwidth-message"></a><span data-ttu-id="5abc2-104">\_Mensagem TTM GETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="5abc2-104">TTM\_GETMAXTIPWIDTH message</span></span>

<span data-ttu-id="5abc2-105">Recupera a largura máxima de uma janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5abc2-105">Retrieves the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="5abc2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5abc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5abc2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5abc2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5abc2-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5abc2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5abc2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5abc2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5abc2-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5abc2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5abc2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5abc2-111">Return value</span></span>

<span data-ttu-id="5abc2-112">Retorna um valor **int** que representa a largura máxima da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5abc2-112">Returns an **INT** value that represents the maximum tooltip width, in pixels.</span></span> <span data-ttu-id="5abc2-113">Se nenhuma largura máxima tiver sido definida anteriormente, a mensagem retornará-1.</span><span class="sxs-lookup"><span data-stu-id="5abc2-113">If no maximum width was set previously, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="5abc2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5abc2-114">Remarks</span></span>

<span data-ttu-id="5abc2-115">O valor máximo da largura da dica de ferramenta não indica a largura real da janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5abc2-115">The maximum tooltip width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="5abc2-116">Em vez disso, se uma cadeia de dica de ferramenta exceder a largura máxima, o controle quebrará o texto em várias linhas, usando espaços para determinar as quebras de linha.</span><span class="sxs-lookup"><span data-stu-id="5abc2-116">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="5abc2-117">Se o texto não puder ser segmentado em várias linhas, ele será exibido em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="5abc2-117">If the text cannot be segmented into multiple lines, it will be displayed on a single line.</span></span> <span data-ttu-id="5abc2-118">O comprimento dessa linha pode exceder a largura máxima da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5abc2-118">The length of this line may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="5abc2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5abc2-119">Requirements</span></span>



| <span data-ttu-id="5abc2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5abc2-120">Requirement</span></span> | <span data-ttu-id="5abc2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5abc2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5abc2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5abc2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5abc2-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5abc2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5abc2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5abc2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5abc2-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5abc2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5abc2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5abc2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5abc2-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5abc2-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5abc2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5abc2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abc2-129">**TTM \_ SETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="5abc2-129">**TTM\_SETMAXTIPWIDTH**</span></span>](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





