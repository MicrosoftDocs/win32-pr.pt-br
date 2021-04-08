---
title: TBN_GETINFOTIP código de notificação (commctrl. h)
description: Recupera informações de InfoTip para um item da barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009113"
---
# <a name="tbn_getinfotip-notification-code"></a><span data-ttu-id="431be-105">Código de notificação do TBN \_ GETINFOTIP</span><span class="sxs-lookup"><span data-stu-id="431be-105">TBN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="431be-106">Recupera informações de InfoTip para um item da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="431be-106">Retrieves infotip information for a toolbar item.</span></span> <span data-ttu-id="431be-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="431be-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="431be-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="431be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="431be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="431be-110">Ponteiro para uma estrutura [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) que contém informações de item e recebe informações de InfoTip.</span><span class="sxs-lookup"><span data-stu-id="431be-110">Pointer to an [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) structure that contains item information and receives infotip information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431be-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="431be-111">Return value</span></span>

<span data-ttu-id="431be-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="431be-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="431be-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="431be-113">Remarks</span></span>

<span data-ttu-id="431be-114">O suporte de infotip na barra de ferramentas permite que a barra de ferramentas exiba dicas de ferramenta para itens que são tão grandes quanto INFOTIPSIZE caracteres.</span><span class="sxs-lookup"><span data-stu-id="431be-114">The infotip support in the toolbar allows the toolbar to display tooltips for items that are as large as INFOTIPSIZE characters.</span></span> <span data-ttu-id="431be-115">Se esse código de notificação não for processado, a barra de ferramentas usará o texto do item para o InfoTip.</span><span class="sxs-lookup"><span data-stu-id="431be-115">If this notification code is not processed, the toolbar will use the item's text for the infotip.</span></span>

## <a name="requirements"></a><span data-ttu-id="431be-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431be-116">Requirements</span></span>



| <span data-ttu-id="431be-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="431be-117">Requirement</span></span> | <span data-ttu-id="431be-118">Valor</span><span class="sxs-lookup"><span data-stu-id="431be-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="431be-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="431be-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="431be-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="431be-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="431be-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="431be-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="431be-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="431be-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="431be-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="431be-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="431be-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="431be-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="431be-126">**Tbn \_ GETINFOTIPW** (Unicode) e **tbn \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="431be-126">**TBN\_GETINFOTIPW** (Unicode) and **TBN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





