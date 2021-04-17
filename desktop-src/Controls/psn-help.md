---
title: PSN_HELP código de notificação (Prsht. h)
description: Notifica uma página que o usuário clicou no botão ajuda. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755425"
---
# <a name="psn_help-notification-code"></a><span data-ttu-id="542c0-105">Código de notificação da ajuda do PSN \_</span><span class="sxs-lookup"><span data-stu-id="542c0-105">PSN\_HELP notification code</span></span>

<span data-ttu-id="542c0-106">Notifica uma página que o usuário clicou no botão ajuda.</span><span class="sxs-lookup"><span data-stu-id="542c0-106">Notifies a page that the user has clicked the Help button.</span></span> <span data-ttu-id="542c0-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="542c0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="542c0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="542c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="542c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="542c0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="542c0-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="542c0-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="542c0-111">Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="542c0-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="542c0-112">O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="542c0-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="542c0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="542c0-113">Return value</span></span>

<span data-ttu-id="542c0-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="542c0-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="542c0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="542c0-115">Remarks</span></span>

<span data-ttu-id="542c0-116">Um aplicativo deve exibir informações de ajuda para a página.</span><span class="sxs-lookup"><span data-stu-id="542c0-116">An application should display Help information for the page.</span></span>

> [!Note]  
> <span data-ttu-id="542c0-117">Não há suporte para este código de notificação ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="542c0-117">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="542c0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="542c0-118">Requirements</span></span>



| <span data-ttu-id="542c0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="542c0-119">Requirement</span></span> | <span data-ttu-id="542c0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="542c0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="542c0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="542c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="542c0-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="542c0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="542c0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="542c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="542c0-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="542c0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="542c0-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="542c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="542c0-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="542c0-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





