---
description: Enviado a um aplicativo que iniciou um cartão de treinamento com a ajuda do Windows.
title: Mensagem de WM_TCARD (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169416"
---
# <a name="wm_tcard-message"></a><span data-ttu-id="76f55-103">Mensagem do WM \_ TCARD</span><span class="sxs-lookup"><span data-stu-id="76f55-103">WM\_TCARD message</span></span>

<span data-ttu-id="76f55-104">Enviado a um aplicativo que iniciou um cartão de treinamento com a ajuda do Windows.</span><span class="sxs-lookup"><span data-stu-id="76f55-104">Sent to an application that has initiated a training card with Windows Help.</span></span> <span data-ttu-id="76f55-105">A mensagem informa ao aplicativo quando o usuário clica em um botão autoria.</span><span class="sxs-lookup"><span data-stu-id="76f55-105">The message informs the application when the user clicks an authorable button.</span></span> <span data-ttu-id="76f55-106">Um aplicativo inicia um cartão de treinamento especificando o comando HELP \_ TCARD em uma chamada para a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .</span><span class="sxs-lookup"><span data-stu-id="76f55-106">An application initiates a training card by specifying the HELP\_TCARD command in a call to the [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="76f55-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76f55-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f55-108">*idAction*</span><span class="sxs-lookup"><span data-stu-id="76f55-108">*idAction*</span></span> 
</dt> <dd>

<span data-ttu-id="76f55-109">Um valor que indica a ação que o usuário executou.</span><span class="sxs-lookup"><span data-stu-id="76f55-109">A value that indicates the action the user has taken.</span></span> <span data-ttu-id="76f55-110">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="76f55-110">This can be one of the following values.</span></span>

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span data-ttu-id="76f55-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span><span class="sxs-lookup"><span data-stu-id="76f55-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-112">O usuário clicou em um botão de **anulação** autorizada.</span><span class="sxs-lookup"><span data-stu-id="76f55-112">The user clicked an authorable **Abort** button.</span></span>

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span data-ttu-id="76f55-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="76f55-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-114">O usuário clicou em um botão **Cancelar** autorizado.</span><span class="sxs-lookup"><span data-stu-id="76f55-114">The user clicked an authorable **Cancel** button.</span></span>

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span data-ttu-id="76f55-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span><span class="sxs-lookup"><span data-stu-id="76f55-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-116">O usuário fechou o cartão de treinamento.</span><span class="sxs-lookup"><span data-stu-id="76f55-116">The user closed the training card.</span></span>

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span data-ttu-id="76f55-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span><span class="sxs-lookup"><span data-stu-id="76f55-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-118">O usuário clicou em um botão de **ajuda** do Windows autorizado.</span><span class="sxs-lookup"><span data-stu-id="76f55-118">The user clicked an authorable Windows **Help** button.</span></span>

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span data-ttu-id="76f55-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span><span class="sxs-lookup"><span data-stu-id="76f55-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-120">O usuário clicou em um botão **ignorar** autorizado.</span><span class="sxs-lookup"><span data-stu-id="76f55-120">The user clicked an authorable **Ignore** button.</span></span>

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span data-ttu-id="76f55-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span><span class="sxs-lookup"><span data-stu-id="76f55-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-122">O usuário clicou em um botão **OK** autorizado.</span><span class="sxs-lookup"><span data-stu-id="76f55-122">The user clicked an authorable **OK** button.</span></span>

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span data-ttu-id="76f55-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span><span class="sxs-lookup"><span data-stu-id="76f55-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-124">O usuário clicou em um botão **não** autorizado.</span><span class="sxs-lookup"><span data-stu-id="76f55-124">The user clicked an authorable **No** button.</span></span>

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span data-ttu-id="76f55-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span><span class="sxs-lookup"><span data-stu-id="76f55-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-126">O usuário clicou em um botão de **repetição** autoria.</span><span class="sxs-lookup"><span data-stu-id="76f55-126">The user clicked an authorable **Retry** button.</span></span>

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span data-ttu-id="76f55-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**\_dados de TCARD de ajuda \_**</span><span class="sxs-lookup"><span data-stu-id="76f55-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP\_TCARD\_DATA**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-128">O usuário clicou em um botão autoria.</span><span class="sxs-lookup"><span data-stu-id="76f55-128">The user clicked an authorable button.</span></span> <span data-ttu-id="76f55-129">O parâmetro *dwActionData* contém um inteiro longo especificado pelo autor da ajuda.</span><span class="sxs-lookup"><span data-stu-id="76f55-129">The *dwActionData* parameter contains a long integer specified by the Help author.</span></span>

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span data-ttu-id="76f55-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**AJUDE a \_ TCARD \_ outro \_ chamador**</span><span class="sxs-lookup"><span data-stu-id="76f55-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP\_TCARD\_OTHER\_CALLER**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-131">Outro aplicativo solicitou cartões de treinamento.</span><span class="sxs-lookup"><span data-stu-id="76f55-131">Another application has requested training cards.</span></span>

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span data-ttu-id="76f55-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span><span class="sxs-lookup"><span data-stu-id="76f55-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span></span>


</dt> <dd>

<span data-ttu-id="76f55-133">O usuário clicou em um botão **Sim** autorizado.</span><span class="sxs-lookup"><span data-stu-id="76f55-133">The user clicked an authorable **Yes** button.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="76f55-134">*dwActionData*</span><span class="sxs-lookup"><span data-stu-id="76f55-134">*dwActionData*</span></span> 
</dt> <dd>

<span data-ttu-id="76f55-135">Se *idAction* especificar \_ o help TCARD \_ data, esse parâmetro será um **longo** especificado pelo autor da ajuda.</span><span class="sxs-lookup"><span data-stu-id="76f55-135">If *idAction* specifies HELP\_TCARD\_DATA, this parameter is a **long** specified by the Help author.</span></span> <span data-ttu-id="76f55-136">Caso contrário, esse parâmetro será zero.</span><span class="sxs-lookup"><span data-stu-id="76f55-136">Otherwise, this parameter is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f55-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76f55-137">Return value</span></span>

<span data-ttu-id="76f55-138">O valor de retorno é ignorado; Use zero.</span><span class="sxs-lookup"><span data-stu-id="76f55-138">The return value is ignored; use zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f55-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76f55-139">Requirements</span></span>



| <span data-ttu-id="76f55-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f55-140">Requirement</span></span> | <span data-ttu-id="76f55-141">Valor</span><span class="sxs-lookup"><span data-stu-id="76f55-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76f55-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76f55-142">Minimum supported client</span></span><br/> | <span data-ttu-id="76f55-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="76f55-143">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="76f55-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76f55-144">Minimum supported server</span></span><br/> | <span data-ttu-id="76f55-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76f55-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76f55-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="76f55-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f55-147"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f55-147"><dt>Winuser.h</dt></span></span> </dl> |



 

 




