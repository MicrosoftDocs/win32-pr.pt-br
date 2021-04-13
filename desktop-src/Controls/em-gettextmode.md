---
title: Mensagem de EM_GETTEXTMODE (RichEdit. h)
description: Obtém o modo de texto atual e o nível de desfazer de um controle de edição rico.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- Controles de EM_GETTEXTMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455612"
---
# <a name="em_gettextmode-message"></a><span data-ttu-id="9a0c1-104">\_Mensagem em GETtextmode</span><span class="sxs-lookup"><span data-stu-id="9a0c1-104">EM\_GETTEXTMODE message</span></span>

<span data-ttu-id="9a0c1-105">Obtém o modo de texto atual e o nível de desfazer de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-105">Gets the current text mode and undo level of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a0c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a0c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a0c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a0c1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a0c1-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a0c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a0c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a0c1-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a0c1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a0c1-111">Return value</span></span>

<span data-ttu-id="9a0c1-112">O valor de retorno é um ou mais valores do tipo de enumeração [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="9a0c1-112">The return value is one or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="9a0c1-113">Os valores indicam o modo de texto atual e o nível de desfazer do controle.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-113">The values indicate the current text mode and undo level of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0c1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a0c1-114">Requirements</span></span>



| <span data-ttu-id="9a0c1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a0c1-115">Requirement</span></span> | <span data-ttu-id="9a0c1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9a0c1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0c1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a0c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0c1-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a0c1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a0c1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a0c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0c1-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a0c1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a0c1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a0c1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a0c1-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a0c1-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0c1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a0c1-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a0c1-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9a0c1-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a0c1-125">**em \_ SETtextmode**</span><span class="sxs-lookup"><span data-stu-id="9a0c1-125">**EM\_SETTEXTMODE**</span></span>](em-settextmode.md)
</dt> <dt>

[<span data-ttu-id="9a0c1-126">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="9a0c1-126">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





