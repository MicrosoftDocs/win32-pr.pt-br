---
description: Postado na janela com o foco quando o usuário escolhe um novo idioma de entrada, seja com a tecla de atalho (especificada no aplicativo do painel de controle teclado) ou do indicador na barra de tarefas do sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Mensagem de WM_INPUTLANGCHANGEREQUEST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761178"
---
# <a name="wm_inputlangchangerequest-message"></a><span data-ttu-id="45fab-103">Mensagem do WM \_ INPUTLANGCHANGEREQUEST</span><span class="sxs-lookup"><span data-stu-id="45fab-103">WM\_INPUTLANGCHANGEREQUEST message</span></span>

<span data-ttu-id="45fab-104">Postado na janela com o foco quando o usuário escolhe um novo idioma de entrada, seja com a tecla de atalho (especificada no aplicativo do painel de controle teclado) ou do indicador na barra de tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="45fab-104">Posted to the window with the focus when the user chooses a new input language, either with the hotkey (specified in the Keyboard control panel application) or from the indicator on the system taskbar.</span></span> <span data-ttu-id="45fab-105">Um aplicativo pode aceitar a alteração passando a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou rejeitar a alteração (e impedir que ela aconteça) retornando imediatamente.</span><span class="sxs-lookup"><span data-stu-id="45fab-105">An application can accept the change by passing the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function or reject the change (and prevent it from taking place) by returning immediately.</span></span>

<span data-ttu-id="45fab-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="45fab-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a><span data-ttu-id="45fab-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45fab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45fab-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45fab-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45fab-109">A nova localidade de entrada.</span><span class="sxs-lookup"><span data-stu-id="45fab-109">The new input locale.</span></span> <span data-ttu-id="45fab-110">Esse parâmetro pode ser uma combinação dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="45fab-110">This parameter can be a combination of the following flags.</span></span>



| <span data-ttu-id="45fab-111">Valor</span><span class="sxs-lookup"><span data-stu-id="45fab-111">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="45fab-112">Significado</span><span class="sxs-lookup"><span data-stu-id="45fab-112">Meaning</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <span data-ttu-id="45fab-113"><dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> retroativa</span><span class="sxs-lookup"><span data-stu-id="45fab-113"><dt>**INPUTLANGCHANGE\_BACKWARD**</dt> <dt>0x0004</dt></span></span> </dl>       | <span data-ttu-id="45fab-114">Uma tecla de acesso foi usada para escolher a localidade de entrada anterior na lista instalada de localidades de entrada.</span><span class="sxs-lookup"><span data-stu-id="45fab-114">A hot key was used to choose the previous input locale in the installed list of input locales.</span></span> <span data-ttu-id="45fab-115">Esse sinalizador não pode ser usado com o \_ sinalizador de encaminhamento INPUTLANGCHANGE.</span><span class="sxs-lookup"><span data-stu-id="45fab-115">This flag cannot be used with the INPUTLANGCHANGE\_FORWARD flag.</span></span><br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <span data-ttu-id="45fab-116"><dt>**INPUTLANGCHANGE \_ Encaminhar**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="45fab-116"><dt>**INPUTLANGCHANGE\_FORWARD**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="45fab-117">Uma tecla de acesso foi usada para escolher a próxima localidade de entrada na lista instalada de localidades de entrada.</span><span class="sxs-lookup"><span data-stu-id="45fab-117">A hot key was used to choose the next input locale in the installed list of input locales.</span></span> <span data-ttu-id="45fab-118">Esse sinalizador não pode ser usado com o \_ sinalizador de retrocesso INPUTLANGCHANGE.</span><span class="sxs-lookup"><span data-stu-id="45fab-118">This flag cannot be used with the INPUTLANGCHANGE\_BACKWARD flag.</span></span><br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <span data-ttu-id="45fab-119"><dt>**INPUTLANGCHANGE \_ SYSCHARSET**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="45fab-119"><dt>**INPUTLANGCHANGE\_SYSCHARSET**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="45fab-120">O layout de teclado da nova localidade de entrada pode ser usado com o conjunto de caracteres do sistema.</span><span class="sxs-lookup"><span data-stu-id="45fab-120">The new input locale's keyboard layout can be used with the system character set.</span></span><br/>                                                                               |



 

</dd> <dt>

<span data-ttu-id="45fab-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45fab-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45fab-122">O identificador de localidade de entrada.</span><span class="sxs-lookup"><span data-stu-id="45fab-122">The input locale identifier.</span></span> <span data-ttu-id="45fab-123">Para obter mais informações, consulte [idiomas, localidades e layouts de teclado](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="45fab-123">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45fab-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45fab-124">Return value</span></span>

<span data-ttu-id="45fab-125">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="45fab-125">Type: **LRESULT**</span></span>

<span data-ttu-id="45fab-126">Essa mensagem é postada, não enviada, para o aplicativo, portanto, o valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="45fab-126">This message is posted, not sent, to the application, so the return value is ignored.</span></span> <span data-ttu-id="45fab-127">Para aceitar a alteração, o aplicativo deve passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="45fab-127">To accept the change, the application should pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="45fab-128">Para rejeitar a alteração, o aplicativo deve retornar zero sem chamar **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="45fab-128">To reject the change, the application should return zero without calling **DefWindowProc**.</span></span>

## <a name="remarks"></a><span data-ttu-id="45fab-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="45fab-129">Remarks</span></span>

<span data-ttu-id="45fab-130">Quando a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) recebe a **mensagem \_ INPUTLANGCHANGEREQUEST do WM** , ela ativa a nova localidade de entrada e notifica o aplicativo sobre a alteração enviando a mensagem [**\_ INPUTLANGCHANGE do WM**](wm-inputlangchange.md) .</span><span class="sxs-lookup"><span data-stu-id="45fab-130">When the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function receives the **WM\_INPUTLANGCHANGEREQUEST** message, it activates the new input locale and notifies the application of the change by sending the [**WM\_INPUTLANGCHANGE**](wm-inputlangchange.md) message.</span></span>

<span data-ttu-id="45fab-131">O indicador de idioma estará presente na barra de tarefas somente se você tiver instalado mais de um layout de teclado e se tiver habilitado o indicador usando o aplicativo painel de controle do teclado.</span><span class="sxs-lookup"><span data-stu-id="45fab-131">The language indicator is present on the taskbar only if you have installed more than one keyboard layout and if you have enabled the indicator using the Keyboard control panel application.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fab-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45fab-132">Requirements</span></span>



| <span data-ttu-id="45fab-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="45fab-133">Requirement</span></span> | <span data-ttu-id="45fab-134">Valor</span><span class="sxs-lookup"><span data-stu-id="45fab-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fab-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45fab-135">Minimum supported client</span></span><br/> | <span data-ttu-id="45fab-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45fab-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="45fab-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45fab-137">Minimum supported server</span></span><br/> | <span data-ttu-id="45fab-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45fab-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="45fab-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45fab-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="45fab-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45fab-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45fab-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="45fab-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="45fab-142">**Referência**</span><span class="sxs-lookup"><span data-stu-id="45fab-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="45fab-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="45fab-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="45fab-144">**INPUTLANGCHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="45fab-144">**WM\_INPUTLANGCHANGE**</span></span>](wm-inputlangchange.md)
</dt> <dt>

<span data-ttu-id="45fab-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="45fab-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="45fab-146">Windows</span><span class="sxs-lookup"><span data-stu-id="45fab-146">Windows</span></span>](windows.md)
</dt> </dl>

 

 
