---
title: TDN_HYPERLINK_CLICKED código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa quando o usuário clica em um hiperlink no conteúdo da caixa de diálogo da tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- TDN_HYPERLINK_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086407"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a><span data-ttu-id="fbe50-105">\_Código de \_ notificação clicado no hiperlink TDN</span><span class="sxs-lookup"><span data-stu-id="fbe50-105">TDN\_HYPERLINK\_CLICKED notification code</span></span>

<span data-ttu-id="fbe50-106">Enviado por uma caixa de diálogo de tarefa quando o usuário clica em um hiperlink no conteúdo da caixa de diálogo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="fbe50-106">Sent by a task dialog when the user clicks a hyperlink in the task dialog content.</span></span> <span data-ttu-id="fbe50-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="fbe50-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="fbe50-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbe50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbe50-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbe50-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbe50-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fbe50-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fbe50-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbe50-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbe50-112">Ponteiro para uma cadeia de caracteres largos que contém a URL do hiperlink.</span><span class="sxs-lookup"><span data-stu-id="fbe50-112">Pointer to a wide-character string containing the URL of the hyperlink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbe50-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbe50-113">Return value</span></span>

<span data-ttu-id="fbe50-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="fbe50-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbe50-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbe50-115">Requirements</span></span>



| <span data-ttu-id="fbe50-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe50-116">Requirement</span></span> | <span data-ttu-id="fbe50-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fbe50-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe50-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbe50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fbe50-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbe50-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbe50-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbe50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fbe50-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbe50-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbe50-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbe50-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbe50-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe50-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





