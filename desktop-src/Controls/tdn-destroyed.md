---
title: TDN_DESTROYED código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa quando é destruído e seu identificador de janela não é mais válido. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- TDN_DESTROYED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824789"
---
# <a name="tdn_destroyed-notification-code"></a><span data-ttu-id="ff657-105">\_Código de notificação destruído TDN</span><span class="sxs-lookup"><span data-stu-id="ff657-105">TDN\_DESTROYED notification code</span></span>

<span data-ttu-id="ff657-106">Enviado por uma caixa de diálogo de tarefa quando é destruído e seu identificador de janela não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="ff657-106">Sent by a task dialog when it is destroyed and its window handle is no longer valid.</span></span> <span data-ttu-id="ff657-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="ff657-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="ff657-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff657-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff657-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff657-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff657-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ff657-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ff657-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff657-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff657-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ff657-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff657-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff657-113">Return value</span></span>

<span data-ttu-id="ff657-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff657-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff657-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff657-115">Requirements</span></span>



| <span data-ttu-id="ff657-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff657-116">Requirement</span></span> | <span data-ttu-id="ff657-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ff657-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff657-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff657-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ff657-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff657-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff657-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff657-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ff657-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff657-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff657-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff657-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff657-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff657-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





