---
description: Notifica o aplicativo quando um IME está prestes a alterar o conteúdo da janela candidata. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091666"
---
# <a name="imn_changecandidate-notification-code"></a><span data-ttu-id="1a486-104">Código de notificação do IMN \_ CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="1a486-104">IMN\_CHANGECANDIDATE notification code</span></span>

<span data-ttu-id="1a486-105">Notifica o aplicativo quando um IME está prestes a alterar o conteúdo da janela candidata.</span><span class="sxs-lookup"><span data-stu-id="1a486-105">Notifies the application when an IME is about to change the content of the candidate window.</span></span> <span data-ttu-id="1a486-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="1a486-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="1a486-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a486-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a486-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a486-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1a486-109">Defina como IMN \_ CHANGECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="1a486-109">Set to IMN\_CHANGECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="1a486-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a486-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1a486-111">Sinalizador de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="1a486-111">Candidate list flag.</span></span> <span data-ttu-id="1a486-112">Cada bit corresponde a uma lista de candidatos: bit 0 à primeira lista, bit 1 à segunda lista e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1a486-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second list, and so on.</span></span> <span data-ttu-id="1a486-113">Se um bit especificado for 1, a janela candidata correspondente estará prestes a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="1a486-113">If a specified bit is 1, the corresponding candidate window is about to be changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a486-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1a486-114">Return Value</span></span>

<span data-ttu-id="1a486-115">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1a486-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a486-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a486-116">Remarks</span></span>

<span data-ttu-id="1a486-117">Um aplicativo deve processar esse comando se ele exibir os candidatos em si.</span><span class="sxs-lookup"><span data-stu-id="1a486-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="1a486-118">A janela do IME altera a aparência da janela candidata ao processar esse comando.</span><span class="sxs-lookup"><span data-stu-id="1a486-118">The IME window changes the appearance of the candidate window when it processes this command.</span></span> <span data-ttu-id="1a486-119">Um aplicativo pode obter informações sobre a janela do sistema com [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) e [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span><span class="sxs-lookup"><span data-stu-id="1a486-119">An application can get information about the system window with the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span></span>

## <a name="requirements"></a><span data-ttu-id="1a486-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a486-120">Requirements</span></span>



| <span data-ttu-id="1a486-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a486-121">Requirement</span></span> | <span data-ttu-id="1a486-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1a486-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a486-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a486-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a486-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a486-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1a486-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a486-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a486-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a486-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1a486-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a486-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a486-128"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a486-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a486-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a486-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a486-130">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1a486-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1a486-131">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1a486-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1a486-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="1a486-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="1a486-133">**ImmGetCandidateListCount**</span><span class="sxs-lookup"><span data-stu-id="1a486-133">**ImmGetCandidateListCount**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[<span data-ttu-id="1a486-134">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="1a486-134">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




