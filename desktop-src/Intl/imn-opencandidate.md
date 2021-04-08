---
description: Notifica um aplicativo quando um IME está prestes a abrir a janela candidata. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: Evento de IMN_OPENCANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828576"
---
# <a name="imn_opencandidate-event"></a><span data-ttu-id="a32eb-104">\_Evento IMN OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="a32eb-104">IMN\_OPENCANDIDATE event</span></span>

<span data-ttu-id="a32eb-105">Notifica um aplicativo quando um IME está prestes a abrir a janela candidata.</span><span class="sxs-lookup"><span data-stu-id="a32eb-105">Notifies an application when an IME is about to open the candidate window.</span></span> <span data-ttu-id="a32eb-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="a32eb-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="a32eb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a32eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a32eb-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="a32eb-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="a32eb-109">Defina como IMN \_ OPENCANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="a32eb-109">Set to IMN\_OPENCANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="a32eb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a32eb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a32eb-111">Sinalizador de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="a32eb-111">Candidate list flag.</span></span> <span data-ttu-id="a32eb-112">Cada bit corresponde a uma lista de candidatos: bit 0 à primeira lista, bit 1 até o segundo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a32eb-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="a32eb-113">Se um bit especificado for 1, a janela candidata correspondente estará prestes a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="a32eb-113">If a specified bit is 1, the corresponding candidate window is about to be opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a32eb-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a32eb-114">Return Value</span></span>

<span data-ttu-id="a32eb-115">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a32eb-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a32eb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a32eb-116">Remarks</span></span>

<span data-ttu-id="a32eb-117">Um aplicativo deve processar esse comando se ele exibir os candidatos em si.</span><span class="sxs-lookup"><span data-stu-id="a32eb-117">An application should process this command if it displays candidates itself.</span></span> <span data-ttu-id="a32eb-118">O aplicativo pode recuperar uma lista de candidatos a serem exibidos usando a função [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .</span><span class="sxs-lookup"><span data-stu-id="a32eb-118">The application can retrieve a list of candidates to display by using the [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) function.</span></span>

<span data-ttu-id="a32eb-119">Por padrão, a janela do IME cria uma janela candidata quando processa esse comando.</span><span class="sxs-lookup"><span data-stu-id="a32eb-119">By default, the IME window creates a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32eb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a32eb-120">Requirements</span></span>



| <span data-ttu-id="a32eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a32eb-121">Requirement</span></span> | <span data-ttu-id="a32eb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a32eb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a32eb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a32eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a32eb-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a32eb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a32eb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a32eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a32eb-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a32eb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a32eb-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a32eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a32eb-128"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a32eb-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a32eb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a32eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a32eb-130">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a32eb-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a32eb-131">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a32eb-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="a32eb-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="a32eb-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="a32eb-133">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a32eb-133">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




