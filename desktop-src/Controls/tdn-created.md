---
title: TDN_CREATED código de notificação (commctrl. h)
description: Enviado pela caixa de diálogo de tarefa depois que a caixa de diálogo tiver sido criada e antes de ser exibida. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: cfe13db3-9c3c-425c-a6ef-17c5cb33eeb6
keywords:
- TDN_CREATED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_CREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25aa40af6b2cb002f2da7aab7c71fd68702ae65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919164"
---
# <a name="tdn_created-notification-code"></a><span data-ttu-id="dad2c-105">\_Código de notificação criado pelo TDN</span><span class="sxs-lookup"><span data-stu-id="dad2c-105">TDN\_CREATED notification code</span></span>

<span data-ttu-id="dad2c-106">Enviado pela caixa de diálogo de tarefa depois que a caixa de diálogo tiver sido criada e antes de ser exibida.</span><span class="sxs-lookup"><span data-stu-id="dad2c-106">Sent by the task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="dad2c-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="dad2c-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_CREATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="dad2c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dad2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad2c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dad2c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dad2c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dad2c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dad2c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dad2c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dad2c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dad2c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad2c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dad2c-113">Return value</span></span>

<span data-ttu-id="dad2c-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="dad2c-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad2c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad2c-115">Requirements</span></span>



| <span data-ttu-id="dad2c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad2c-116">Requirement</span></span> | <span data-ttu-id="dad2c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dad2c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dad2c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad2c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dad2c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dad2c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dad2c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad2c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dad2c-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dad2c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dad2c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dad2c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dad2c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dad2c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





