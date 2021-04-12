---
title: Mensagem de EM_GETHANDLE (WinUser. h)
description: Obtém um identificador da memória atualmente alocada para um texto do controle de edição de várias linhas.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- Controles de EM_GETHANDLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499548"
---
# <a name="em_gethandle-message"></a><span data-ttu-id="ad837-104">\_Mensagem em GEThandle</span><span class="sxs-lookup"><span data-stu-id="ad837-104">EM\_GETHANDLE message</span></span>

<span data-ttu-id="ad837-105">Obtém um identificador da memória atualmente alocada para um texto do controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="ad837-105">Gets a handle of the memory currently allocated for a multiline edit control's text.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad837-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad837-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad837-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad837-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ad837-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ad837-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad837-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad837-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ad837-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad837-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad837-111">Return value</span></span>

<span data-ttu-id="ad837-112">O valor de retorno é um identificador de memória que identifica o buffer que contém o conteúdo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ad837-112">The return value is a memory handle identifying the buffer that holds the content of the edit control.</span></span> <span data-ttu-id="ad837-113">Se ocorrer um erro, como enviar a mensagem para um controle de edição de linha única, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="ad837-113">If an error occurs, such as sending the message to a single-line edit control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad837-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad837-114">Remarks</span></span>

<span data-ttu-id="ad837-115">Se a função for realizada com sucesso, o aplicativo poderá acessar o conteúdo do controle de edição, convertendo o valor de retorno para [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) e passando-o para [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span><span class="sxs-lookup"><span data-stu-id="ad837-115">If the function succeeds, the application can access the contents of the edit control by casting the return value to [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) and passing it to [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span></span> <span data-ttu-id="ad837-116">**LocalLock** retorna um ponteiro para um buffer que é uma matriz terminada em nulo de **Char** s ou **WCHAR** s, dependendo se uma função ANSI ou Unicode criou o controle.</span><span class="sxs-lookup"><span data-stu-id="ad837-116">**LocalLock** returns a pointer to a buffer that is a null-terminated array of **CHAR** s or **WCHAR** s, depending on whether an ANSI or Unicode function created the control.</span></span> <span data-ttu-id="ad837-117">Por exemplo, se [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) foi usado, o buffer é uma matriz de **Char** s, mas se **CreateWindowExW** foi usado, o buffer é uma matriz de **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="ad837-117">For example, if [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) was used the buffer is an array of **CHAR** s, but if **CreateWindowExW** was used the buffer is an array of **WCHAR** s.</span></span> <span data-ttu-id="ad837-118">O aplicativo pode não alterar o conteúdo do buffer.</span><span class="sxs-lookup"><span data-stu-id="ad837-118">The application may not change the contents of the buffer.</span></span> <span data-ttu-id="ad837-119">Para desbloquear o buffer, o aplicativo chama [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) antes de permitir que o controle de edição receba novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="ad837-119">To unlock the buffer, the application calls [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) before allowing the edit control to receive new messages.</span></span>

> [!Note]  
> <span data-ttu-id="ad837-120">Para Comctl32.dll versão 6, o buffer sempre contém uma matriz de **WCHAR** s, independentemente de uma função ANSI ou Unicode ter criado o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ad837-120">For Comctl32.dll version 6, the buffer always contains an array of **WCHAR** s, regardless of whether an ANSI or Unicode function created the edit control.</span></span> <span data-ttu-id="ad837-121">Para obter mais informações sobre versões de DLL, consulte [versões de controle comuns](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ad837-121">For more information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

 

<span data-ttu-id="ad837-122">Se seu aplicativo não puder obedecer às restrições impostas por em **\_ GetHandle**, use as funções [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para copiar o conteúdo do controle de edição em um buffer fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad837-122">If your application cannot abide by the restrictions imposed by **EM\_GETHANDLE**, use the [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) and [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) functions to copy the contents of the edit control into an application-provided buffer.</span></span>

<span data-ttu-id="ad837-123">**Edição avançada:** Não há suporte para a mensagem em **\_ GetHandle** .</span><span class="sxs-lookup"><span data-stu-id="ad837-123">**Rich Edit:** The **EM\_GETHANDLE** message is not supported.</span></span> <span data-ttu-id="ad837-124">Os controles de edição avançados não armazenam texto como uma matriz simples de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ad837-124">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad837-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad837-125">Requirements</span></span>



| <span data-ttu-id="ad837-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad837-126">Requirement</span></span> | <span data-ttu-id="ad837-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ad837-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad837-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad837-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ad837-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad837-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad837-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad837-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ad837-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad837-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad837-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad837-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad837-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad837-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad837-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad837-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad837-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ad837-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad837-136">**\_ONhandle**</span><span class="sxs-lookup"><span data-stu-id="ad837-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

<span data-ttu-id="ad837-137">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="ad837-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ad837-138">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="ad837-138">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="ad837-139">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="ad837-139">**GetWindowTextLength**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="ad837-140">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="ad837-140">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[<span data-ttu-id="ad837-141">**LocalUnlock**</span><span class="sxs-lookup"><span data-stu-id="ad837-141">**LocalUnlock**</span></span>](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

