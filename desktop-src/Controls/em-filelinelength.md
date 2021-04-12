---
title: Mensagem de EM_FILELINELENGTH (CommCtrl. h)
description: Recupera o comprimento, em caracteres, de uma linha em um controle de edição, independentemente de como as linhas são exibidas na tela.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Controles de EM_FILELINELENGTH de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499443"
---
# <a name="em_filelinelength-message"></a><span data-ttu-id="f348e-104">\_Mensagem em FILELINELENGTH</span><span class="sxs-lookup"><span data-stu-id="f348e-104">EM\_FILELINELENGTH message</span></span>

<span data-ttu-id="f348e-105">Recupera o comprimento, em caracteres, de uma linha em um controle de edição, independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="f348e-105">Retrieves the length, in characters, of a line in an edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="f348e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f348e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f348e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f348e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f348e-108">O índice de caracteres de um caractere na linha cujo comprimento deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="f348e-108">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="f348e-109">Se esse parâmetro for maior que o número de caracteres no controle, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="f348e-109">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="f348e-110">Esse parâmetro pode ser-1.</span><span class="sxs-lookup"><span data-stu-id="f348e-110">This parameter can be -1.</span></span> <span data-ttu-id="f348e-111">Nesse caso, a mensagem retorna o número de caracteres não selecionados em linhas que contêm os caracteres selecionados.</span><span class="sxs-lookup"><span data-stu-id="f348e-111">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="f348e-112">Por exemplo, se a seleção estendida do quarto caractere de uma linha até o oitavo caractere do final da linha seguinte, o valor de retorno será 10 (três caracteres na primeira linha e sete no próximo).</span><span class="sxs-lookup"><span data-stu-id="f348e-112">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="f348e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f348e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f348e-114">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="f348e-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f348e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f348e-115">Return value</span></span>

<span data-ttu-id="f348e-116">Para controles de edição de várias linhas, o valor de retorno é o comprimento, em **TCHAR** s, da linha especificada pelo parâmetro *wParam* , independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="f348e-116">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="f348e-117">Ele não inclui o caractere de retorno de carro ou de linhagem no final da linha.</span><span class="sxs-lookup"><span data-stu-id="f348e-117">It does not include the carriage-return or linefeed character at the end of the line.</span></span>

<span data-ttu-id="f348e-118">Para controles de edição de linha única, o valor de retorno é o comprimento, em **TCHAR** s, do texto no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="f348e-118">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="f348e-119">Se *wParam* for maior que o número de caracteres no controle, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="f348e-119">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f348e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f348e-120">Remarks</span></span>

<span data-ttu-id="f348e-121">Use a mensagem em [**\_ FILELINEINDEX**](em-lineindex.md) para recuperar um índice de caracteres para um determinado número de linhas dentro de um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="f348e-121">Use the [**EM\_FILELINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="f348e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f348e-122">Requirements</span></span>



| <span data-ttu-id="f348e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f348e-123">Requirement</span></span> | <span data-ttu-id="f348e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f348e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f348e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f348e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f348e-126">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="f348e-126">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f348e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f348e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f348e-128">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="f348e-128">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f348e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f348e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f348e-130"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f348e-130"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f348e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f348e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f348e-132">**em \_ FILELINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="f348e-132">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





