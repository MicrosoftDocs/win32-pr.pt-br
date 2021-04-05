---
title: TBN_ENDDRAG código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas que o usuário parou de arrastar um botão em uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086006"
---
# <a name="tbn_enddrag-notification-code"></a><span data-ttu-id="a4849-105">Código de notificação do TBN \_ ENDarraste</span><span class="sxs-lookup"><span data-stu-id="a4849-105">TBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="a4849-106">Notifica a janela pai da barra de ferramentas que o usuário parou de arrastar um botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a4849-106">Notifies the toolbar's parent window that the user has stopped dragging a button in a toolbar.</span></span> <span data-ttu-id="a4849-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a4849-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a4849-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4849-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4849-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4849-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4849-110">Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="a4849-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="a4849-111">O membro **iItem** contém o identificador de comando do botão que está sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="a4849-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4849-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4849-112">Return value</span></span>

<span data-ttu-id="a4849-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a4849-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4849-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4849-114">Requirements</span></span>



| <span data-ttu-id="a4849-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4849-115">Requirement</span></span> | <span data-ttu-id="a4849-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a4849-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4849-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4849-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4849-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4849-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4849-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4849-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4849-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4849-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4849-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4849-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4849-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4849-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





