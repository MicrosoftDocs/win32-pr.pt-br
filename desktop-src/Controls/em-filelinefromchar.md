---
title: Mensagem de EM_FILELINEFROMCHAR (CommCtrl. h)
description: Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controles de EM_FILELINEFROMCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455351"
---
# <a name="em_filelinefromchar-message"></a><span data-ttu-id="ed268-104">\_Mensagem em FILELINEFROMCHAR</span><span class="sxs-lookup"><span data-stu-id="ed268-104">EM\_FILELINEFROMCHAR message</span></span>

<span data-ttu-id="ed268-105">Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="ed268-105">Gets the index of the line that contains the specified character index in a multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="ed268-106">Um índice de caracteres é o índice de base zero do caractere do início do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ed268-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed268-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed268-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed268-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed268-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed268-109">O índice de caracteres do caractere contido na linha cujo número deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="ed268-109">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="ed268-110">Se esse parâmetro for-1, **em \_ FILELINEFROMCHAR** recuperará o número de linha da linha atual (a linha que contém o cursor) ou, se houver uma seleção, o número de linha da linha que contém o início da seleção.</span><span class="sxs-lookup"><span data-stu-id="ed268-110">If this parameter is -1, **EM\_FILELINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="ed268-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed268-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed268-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ed268-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed268-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed268-113">Return value</span></span>

<span data-ttu-id="ed268-114">O valor de retorno é o número de linha com base em zero da linha que contém o índice de caracteres especificado por *wParam*, independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="ed268-114">The return value is the zero-based line number of the line containing the character index specified by *wParam*, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed268-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed268-115">Requirements</span></span>



| <span data-ttu-id="ed268-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed268-116">Requirement</span></span> | <span data-ttu-id="ed268-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ed268-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed268-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed268-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ed268-119">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="ed268-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ed268-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed268-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ed268-121">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="ed268-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed268-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed268-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed268-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed268-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed268-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ed268-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed268-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ed268-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed268-126">**em \_ FILELINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="ed268-126">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





