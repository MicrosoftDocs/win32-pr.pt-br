---
title: NM_OUTOFMEMORY código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o controle não pôde concluir uma operação porque não havia memória suficiente disponível. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008928"
---
# <a name="nm_outofmemory-notification-code"></a><span data-ttu-id="48790-105">\_Código de notificação de OUTOFMEMORY nm</span><span class="sxs-lookup"><span data-stu-id="48790-105">NM\_OUTOFMEMORY notification code</span></span>

<span data-ttu-id="48790-106">Notifica uma janela pai do controle que o controle não pôde concluir uma operação porque não havia memória suficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="48790-106">Notifies a control's parent window that the control could not complete an operation because there was not enough memory available.</span></span> <span data-ttu-id="48790-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="48790-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="48790-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48790-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48790-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48790-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48790-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="48790-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48790-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48790-111">Return value</span></span>

<span data-ttu-id="48790-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="48790-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="48790-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48790-113">Requirements</span></span>



| <span data-ttu-id="48790-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="48790-114">Requirement</span></span> | <span data-ttu-id="48790-115">Valor</span><span class="sxs-lookup"><span data-stu-id="48790-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48790-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48790-116">Minimum supported client</span></span><br/> | <span data-ttu-id="48790-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48790-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48790-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48790-118">Minimum supported server</span></span><br/> | <span data-ttu-id="48790-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48790-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48790-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48790-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="48790-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48790-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





