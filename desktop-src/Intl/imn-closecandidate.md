---
description: Notifica um aplicativo quando um IME está prestes a fechar a janela de candidatos. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: IMN_CLOSECANDIDATE código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768741"
---
# <a name="imn_closecandidate-notification-code"></a><span data-ttu-id="69ed7-104">Código de notificação do IMN \_ CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="69ed7-104">IMN\_CLOSECANDIDATE notification code</span></span>

<span data-ttu-id="69ed7-105">Notifica um aplicativo quando um IME está prestes a fechar a janela de candidatos.</span><span class="sxs-lookup"><span data-stu-id="69ed7-105">Notifies an application when an IME is about to close the candidates window.</span></span> <span data-ttu-id="69ed7-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="69ed7-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="69ed7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69ed7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ed7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="69ed7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="69ed7-109">Defina como IMN \_ CLOSECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="69ed7-109">Set to IMN\_CLOSECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="69ed7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="69ed7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="69ed7-111">Sinalizador de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="69ed7-111">Candidate list flag.</span></span> <span data-ttu-id="69ed7-112">Cada bit corresponde a uma lista de candidatos: bit 0 à primeira lista, bit 1 até o segundo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="69ed7-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="69ed7-113">Se um bit especificado for 1, a janela de candidatos correspondente estará prestes a ser fechada.</span><span class="sxs-lookup"><span data-stu-id="69ed7-113">If a specified bit is 1, the corresponding candidates window is about to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69ed7-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="69ed7-114">Return Value</span></span>

<span data-ttu-id="69ed7-115">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="69ed7-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69ed7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="69ed7-116">Remarks</span></span>

<span data-ttu-id="69ed7-117">Um aplicativo deve processar esse comando se ele exibir os candidatos em si.</span><span class="sxs-lookup"><span data-stu-id="69ed7-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="69ed7-118">Por padrão, a janela do IME destrói uma janela candidata ao processar esse comando.</span><span class="sxs-lookup"><span data-stu-id="69ed7-118">By default, the IME window destroys a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ed7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69ed7-119">Requirements</span></span>



| <span data-ttu-id="69ed7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="69ed7-120">Requirement</span></span> | <span data-ttu-id="69ed7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="69ed7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ed7-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ed7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="69ed7-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69ed7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="69ed7-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ed7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="69ed7-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69ed7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69ed7-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="69ed7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="69ed7-127"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69ed7-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ed7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="69ed7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ed7-129">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="69ed7-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="69ed7-130">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="69ed7-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="69ed7-131">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="69ed7-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




