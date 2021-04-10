---
title: Mensagem de TTM_SETMAXTIPWIDTH (commctrl. h)
description: Define a largura máxima para uma janela de dica de ferramenta.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- Controles de TTM_SETMAXTIPWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163592"
---
# <a name="ttm_setmaxtipwidth-message"></a><span data-ttu-id="72821-104">\_Mensagem TTM SETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="72821-104">TTM\_SETMAXTIPWIDTH message</span></span>

<span data-ttu-id="72821-105">Define a largura máxima para uma janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="72821-105">Sets the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="72821-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72821-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72821-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="72821-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="72821-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="72821-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72821-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72821-110">Largura máxima da janela de dica de ferramenta ou-1 para permitir qualquer largura.</span><span class="sxs-lookup"><span data-stu-id="72821-110">Maximum tooltip window width, or -1 to allow any width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72821-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72821-111">Return value</span></span>

<span data-ttu-id="72821-112">Retorna a largura máxima da dica de ferramenta anterior.</span><span class="sxs-lookup"><span data-stu-id="72821-112">Returns the previous maximum tooltip width.</span></span>

## <a name="remarks"></a><span data-ttu-id="72821-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="72821-113">Remarks</span></span>

<span data-ttu-id="72821-114">O valor de largura máximo não indica a largura real de uma janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="72821-114">The maximum width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="72821-115">Em vez disso, se uma cadeia de dica de ferramenta exceder a largura máxima, o controle quebrará o texto em várias linhas, usando espaços para determinar as quebras de linha.</span><span class="sxs-lookup"><span data-stu-id="72821-115">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="72821-116">Se o texto não puder ser segmentado em várias linhas, ele será exibido em uma única linha, o que pode exceder a largura máxima da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="72821-116">If the text cannot be segmented into multiple lines, it is displayed on a single line, which may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="72821-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72821-117">Requirements</span></span>



| <span data-ttu-id="72821-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72821-118">Requirement</span></span> | <span data-ttu-id="72821-119">Valor</span><span class="sxs-lookup"><span data-stu-id="72821-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72821-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72821-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72821-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72821-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72821-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72821-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72821-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72821-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72821-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72821-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72821-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72821-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72821-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="72821-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72821-127">**TTM \_ GETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="72821-127">**TTM\_GETMAXTIPWIDTH**</span></span>](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





