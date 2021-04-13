---
title: Mensagem de ACM_OPEN (commctrl. h)
description: Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação. Você pode enviar essa mensagem explicitamente ou usar a \_ macro animado abrir ou animar \_ OpenEx. É recomendável usar a versão Unicode desta mensagem, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- Controles de ACM_OPEN de mensagens do Windows
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369352"
---
# <a name="acm_open-message"></a><span data-ttu-id="03fb5-106">\_Mensagem aberta do ACM</span><span class="sxs-lookup"><span data-stu-id="03fb5-106">ACM\_OPEN message</span></span>

<span data-ttu-id="03fb5-107">Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação.</span><span class="sxs-lookup"><span data-stu-id="03fb5-107">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="03fb5-108">Você pode enviar essa mensagem explicitamente ou usar a macro [**animado \_ abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ou [**animar \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) .</span><span class="sxs-lookup"><span data-stu-id="03fb5-108">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <span data-ttu-id="03fb5-109">É recomendável usar a versão Unicode desta mensagem, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="03fb5-109">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

## <a name="parameters"></a><span data-ttu-id="03fb5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03fb5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03fb5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03fb5-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03fb5-112">[Versão 4,71](common-control-versions.md) e posterior.</span><span class="sxs-lookup"><span data-stu-id="03fb5-112">[Version 4.71](common-control-versions.md) and later.</span></span> <span data-ttu-id="03fb5-113">Um identificador de instância para o módulo do qual o recurso deve ser carregado.</span><span class="sxs-lookup"><span data-stu-id="03fb5-113">An instance handle to the module from which the resource should be loaded.</span></span> <span data-ttu-id="03fb5-114">Defina esse valor como **NULL** para que o controle use o valor HINSTANCE usado para criar a janela.</span><span class="sxs-lookup"><span data-stu-id="03fb5-114">Set this value to **NULL** to have the control use the HINSTANCE value used to create the window.</span></span> <span data-ttu-id="03fb5-115">Observe que, se a janela for criada por uma DLL, o valor padrão para *wParam* será o valor HINSTANCE da dll, não do aplicativo que chama a dll.</span><span class="sxs-lookup"><span data-stu-id="03fb5-115">Note that if the window is created by a DLL, the default value for *wParam* is the HINSTANCE value of the DLL, not of the application that calls the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="03fb5-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03fb5-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03fb5-117">Um ponteiro para um buffer que contém o caminho do arquivo AVI ou o nome de um recurso AVI.</span><span class="sxs-lookup"><span data-stu-id="03fb5-117">A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource.</span></span> <span data-ttu-id="03fb5-118">Como alternativa, esse parâmetro pode consistir no identificador de recurso AVI em [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e zero no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03fb5-118">Alternatively, this parameter can consist of the AVI resource identifier in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and zero in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="03fb5-119">Para criar esse valor, use a macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="03fb5-119">To create this value, use the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="03fb5-120">O controle carrega o recurso AVI do módulo especificado pelo identificador de instância passado para a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , a macro de criação de [**animação \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) ou a função de criação da caixa de diálogo que criou o controle.</span><span class="sxs-lookup"><span data-stu-id="03fb5-120">The control loads the AVI resource from the module specified by the instance handle passed to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function, the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro, or the dialog box creation function that created the control.</span></span> <span data-ttu-id="03fb5-121">Na [versão 4,71](common-control-versions.md) e posteriores, o recurso é carregado do módulo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="03fb5-121">In [Version 4.71](common-control-versions.md) and later, the resource is loaded from the module specified by *wParam*.</span></span> <span data-ttu-id="03fb5-122">Um recurso AVI deve ter o tipo "AVI".</span><span class="sxs-lookup"><span data-stu-id="03fb5-122">An AVI resource must have the "AVI" type.</span></span> <span data-ttu-id="03fb5-123">Se esse parâmetro for **nulo**, o sistema fechará o arquivo AVI que foi aberto anteriormente para o controle de animação especificado, se houver.</span><span class="sxs-lookup"><span data-stu-id="03fb5-123">If this parameter is **NULL**, the system closes the AVI file that was previously opened for the specified animation control, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03fb5-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03fb5-124">Return value</span></span>

<span data-ttu-id="03fb5-125">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="03fb5-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="03fb5-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="03fb5-126">Remarks</span></span>

<span data-ttu-id="03fb5-127">O arquivo AVI ou o recurso especificado por *lpszName* não deve conter áudio.</span><span class="sxs-lookup"><span data-stu-id="03fb5-127">The AVI file or resource specified by *lpszName* must not contain audio.</span></span>

<span data-ttu-id="03fb5-128">É recomendável usar a versão Unicode desta mensagem, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="03fb5-128">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

<span data-ttu-id="03fb5-129">Você só pode abrir clipes AVI silenciosos.</span><span class="sxs-lookup"><span data-stu-id="03fb5-129">You can only open silent AVI clips.</span></span> <span data-ttu-id="03fb5-130">Abrir \_ e [**animar \_ abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) falhará se *lParam* especificar um clipe AVI que contenha som.</span><span class="sxs-lookup"><span data-stu-id="03fb5-130">ACM\_OPEN and [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) fail if *lParam* specifies an AVI clip that contains sound.</span></span>

<span data-ttu-id="03fb5-131">Você pode usar a [**animação \_ fechar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) para fechar um arquivo AVI ou um recurso AVI que foi aberto anteriormente para o controle de animação especificado.</span><span class="sxs-lookup"><span data-stu-id="03fb5-131">You can use [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) to close an AVI file or AVI resource that was previously opened for the specified animation control.</span></span>

## <a name="requirements"></a><span data-ttu-id="03fb5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03fb5-132">Requirements</span></span>



| <span data-ttu-id="03fb5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="03fb5-133">Requirement</span></span> | <span data-ttu-id="03fb5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="03fb5-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03fb5-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03fb5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="03fb5-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03fb5-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03fb5-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03fb5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="03fb5-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03fb5-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03fb5-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03fb5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="03fb5-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03fb5-140"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="03fb5-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="03fb5-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="03fb5-142">**ACM \_ OPENW** (Unicode) e **ACM \_ opena** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="03fb5-142">**ACM\_OPENW** (Unicode) and **ACM\_OPENA** (ANSI)</span></span><br/>                         |



 

