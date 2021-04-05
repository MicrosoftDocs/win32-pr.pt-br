---
title: TDN_DIALOG_CONSTRUCTED código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa depois que a caixa de diálogo tiver sido criada e antes de ser exibida. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: e8556039-a74d-4e33-931d-a63ad5b2d4b0
keywords:
- TDN_DIALOG_CONSTRUCTED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_DIALOG_CONSTRUCTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d3360a8cee3542037ea927363de8cab69977e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919162"
---
# <a name="tdn_dialog_constructed-notification-code"></a><span data-ttu-id="7b0c7-105">\_Código de \_ notificação construído pela caixa de diálogo TDN</span><span class="sxs-lookup"><span data-stu-id="7b0c7-105">TDN\_DIALOG\_CONSTRUCTED notification code</span></span>

<span data-ttu-id="7b0c7-106">Enviado por uma caixa de diálogo de tarefa depois que a caixa de diálogo tiver sido criada e antes de ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7b0c7-106">Sent by a task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="7b0c7-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="7b0c7-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DIALOG_CONSTRUCTED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="7b0c7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b0c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b0c7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b0c7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0c7-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7b0c7-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7b0c7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b0c7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0c7-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7b0c7-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b0c7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b0c7-113">Return value</span></span>

<span data-ttu-id="7b0c7-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="7b0c7-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b0c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b0c7-115">Requirements</span></span>



| <span data-ttu-id="7b0c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b0c7-116">Requirement</span></span> | <span data-ttu-id="7b0c7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7b0c7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0c7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b0c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b0c7-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b0c7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b0c7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b0c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b0c7-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b0c7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b0c7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b0c7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b0c7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b0c7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





