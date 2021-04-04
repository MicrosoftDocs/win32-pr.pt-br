---
title: Mensagem de EM_FILELINEINDEX (CommCtrl. h)
description: Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controles de EM_FILELINEINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085738"
---
# <a name="em_filelineindex-message-commctrlh"></a><span data-ttu-id="7102b-104">Mensagem de EM_FILELINEINDEX (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="7102b-104">EM_FILELINEINDEX message (CommCtrl.h)</span></span>

<span data-ttu-id="7102b-105">Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="7102b-105">Gets the character index of the first character of a specified line in a multiline edit control, independently of how lines are displayed on the screen..</span></span> <span data-ttu-id="7102b-106">Um índice de caracteres é o índice de base zero do caractere do início do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="7102b-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7102b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7102b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7102b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7102b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7102b-109">O número de linha com base em zero.</span><span class="sxs-lookup"><span data-stu-id="7102b-109">The zero-based line number.</span></span> <span data-ttu-id="7102b-110">Um valor de-1 especifica o número de linha atual (a linha que contém o cursor).</span><span class="sxs-lookup"><span data-stu-id="7102b-110">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="7102b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7102b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7102b-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="7102b-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7102b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7102b-113">Return value</span></span>

<span data-ttu-id="7102b-114">O valor de retorno é o índice de caracteres da linha especificada no parâmetro *wParam* , independentemente de como as linhas são exibidas na tela, ou é-1 se o número de linha especificado for maior que o número de linhas no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="7102b-114">The return value is the character index of the line specified in the *wParam* parameter, independently of how lines are displayed on the screen, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7102b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7102b-115">Requirements</span></span>



| <span data-ttu-id="7102b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7102b-116">Requirement</span></span> | <span data-ttu-id="7102b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7102b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7102b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7102b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7102b-119">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="7102b-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7102b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7102b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7102b-121">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="7102b-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7102b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7102b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7102b-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7102b-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7102b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7102b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7102b-125">**em \_ FILELINEFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="7102b-125">**EM\_FILELINEFROMCHAR**</span></span>](em-filelinefromchar.md)
</dt> </dl>

 

 





