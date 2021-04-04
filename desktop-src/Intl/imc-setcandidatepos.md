---
description: Instrui uma janela do IME para definir a posição da janela de candidatos. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Comando IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647361"
---
# <a name="imc_setcandidatepos-command"></a><span data-ttu-id="b8a9e-104">\_Comando SETCANDIDATEPOS do IMC</span><span class="sxs-lookup"><span data-stu-id="b8a9e-104">IMC\_SETCANDIDATEPOS command</span></span>

<span data-ttu-id="b8a9e-105">Instrui uma janela do IME para definir a posição da janela de candidatos.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-105">Instructs an IME window to set the position of the candidates window.</span></span> <span data-ttu-id="b8a9e-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="b8a9e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8a9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a9e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8a9e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b8a9e-109">Defina como IMC \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-109">Set to IMC\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="b8a9e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8a9e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b8a9e-111">Ponteiro para uma estrutura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contém a coordenada x e a coordenada y para a janela candidatos.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the x coordinate and y coordinate for the candidates window.</span></span> <span data-ttu-id="b8a9e-112">O aplicativo deve definir o membro **dwIndex** dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-112">The application should set the **dwIndex** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a9e-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b8a9e-113">Return Value</span></span>

<span data-ttu-id="b8a9e-114">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a9e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8a9e-115">Remarks</span></span>

<span data-ttu-id="b8a9e-116">Esse comando destina-se a aplicativos que exibem caracteres de composição por conta própria, mas usam a janela do IME para exibir candidatos.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-116">This command is intended for applications that display composition characters on their own but use the IME window to display candidates.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a9e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8a9e-117">Requirements</span></span>



| <span data-ttu-id="b8a9e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a9e-118">Requirement</span></span> | <span data-ttu-id="b8a9e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b8a9e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a9e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8a9e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a9e-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8a9e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b8a9e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8a9e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a9e-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8a9e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8a9e-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b8a9e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a9e-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8a9e-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a9e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8a9e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a9e-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b8a9e-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b8a9e-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b8a9e-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b8a9e-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="b8a9e-130">**\_controle IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-130">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




