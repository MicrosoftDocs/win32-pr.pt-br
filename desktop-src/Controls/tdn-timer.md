---
title: TDN_TIMER código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa aproximadamente a cada 200 milissegundos.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749301"
---
# <a name="tdn_timer-notification-code"></a><span data-ttu-id="e368f-104">\_Código de notificação do temporizador TDN</span><span class="sxs-lookup"><span data-stu-id="e368f-104">TDN\_TIMER notification code</span></span>

<span data-ttu-id="e368f-105">Enviado por uma caixa de diálogo de tarefa aproximadamente a cada 200 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="e368f-105">Sent by a task dialog approximately every 200 milliseconds.</span></span> <span data-ttu-id="e368f-106">Esse código de notificação é enviado quando o \_ sinalizador do temporizador de retorno de chamada TDF foi \_ definido no membro **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que foi passada para a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="e368f-106">This notification code is sent when the TDF\_CALLBACK\_TIMER flag has been set in the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that was passed to the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="e368f-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método **TaskDialogIndirect** .</span><span class="sxs-lookup"><span data-stu-id="e368f-107">This notification code is received only through the task dialog callback function, which can be registered using the **TaskDialogIndirect** method.</span></span>


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e368f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e368f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e368f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e368f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e368f-110">Um **DWORD** que especifica o número de milissegundos desde que a caixa de diálogo foi criada ou esse código de notificação retornou **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e368f-110">A **DWORD** that specifies the number of milliseconds since the dialog was created or this notification code returned **S\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e368f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e368f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e368f-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e368f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e368f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e368f-113">Return value</span></span>

<span data-ttu-id="e368f-114">Para redefinir o desejo, o aplicativo deve retornar **S \_ false**, caso contrário, o or continuará a ser incrementado.</span><span class="sxs-lookup"><span data-stu-id="e368f-114">To reset the tickcount, the application must return **S\_FALSE**, otherwise the tickcount will continue to increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="e368f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e368f-115">Requirements</span></span>



| <span data-ttu-id="e368f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e368f-116">Requirement</span></span> | <span data-ttu-id="e368f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e368f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e368f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e368f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e368f-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e368f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e368f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e368f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e368f-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e368f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e368f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e368f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e368f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e368f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





