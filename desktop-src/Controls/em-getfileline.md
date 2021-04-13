---
title: Mensagem de EM_GETFILELINE (CommCtrl. h)
description: Copia uma linha de texto de um controle de edição, independentemente de como as linhas são exibidas na tela e as coloca em um buffer especificado.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controles de EM_GETFILELINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455547"
---
# <a name="em_getfileline-message-commctrlh"></a><span data-ttu-id="bb7c7-104">Mensagem de EM_GETFILELINE (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="bb7c7-104">EM_GETFILELINE message (CommCtrl.h)</span></span>

<span data-ttu-id="bb7c7-105">Copia uma linha de texto de um controle de edição, independentemente de como as linhas são exibidas na tela e as coloca em um buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-105">Copies a line of text from an edit control, independently of how lines are displayed on the screen, and places it in a specified buffer.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb7c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb7c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb7c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7c7-108">O índice de base zero da linha a ser recuperada de um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-108">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="bb7c7-109">Um valor de zero Especifica a linha superior.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-109">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="bb7c7-110">Esse parâmetro é ignorado por um controle de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-110">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="bb7c7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb7c7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7c7-112">Um ponteiro para o buffer que recebe uma cópia da linha.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-112">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="bb7c7-113">Antes de enviar a mensagem, defina a primeira palavra desse buffer com o tamanho, em **TCHAR** s, do buffer.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-113">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="bb7c7-114">Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="bb7c7-115">O tamanho na primeira palavra é substituído pela linha copiada.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-115">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb7c7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb7c7-116">Return value</span></span>

<span data-ttu-id="bb7c7-117">O valor de retorno é o número de **TCHAR** s copiados.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-117">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="bb7c7-118">O valor de retorno será zero se o número de linha especificado pelo parâmetro *wParam* for maior que o número de linhas no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-118">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7c7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb7c7-119">Remarks</span></span>

<span data-ttu-id="bb7c7-120">A linha copiada não contém um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="bb7c7-120">The copied line does not contain a terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7c7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb7c7-121">Requirements</span></span>



| <span data-ttu-id="bb7c7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb7c7-122">Requirement</span></span> | <span data-ttu-id="bb7c7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bb7c7-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7c7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb7c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7c7-125">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="bb7c7-125">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb7c7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb7c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7c7-127">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="bb7c7-127">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb7c7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb7c7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb7c7-129"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb7c7-129"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7c7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb7c7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb7c7-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bb7c7-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb7c7-132">**em \_ FILELINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="bb7c7-132">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="bb7c7-133">**Editar \_ GetFile**</span><span class="sxs-lookup"><span data-stu-id="bb7c7-133">**Edit\_GetFileLine**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

<span data-ttu-id="bb7c7-134">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="bb7c7-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bb7c7-135">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="bb7c7-135">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

