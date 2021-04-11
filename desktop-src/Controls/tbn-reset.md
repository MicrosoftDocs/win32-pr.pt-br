---
title: TBN_RESET código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas que o usuário redefiniu o conteúdo da caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009709"
---
# <a name="tbn_reset-notification-code"></a><span data-ttu-id="796cf-105">\_Código de notificação de redefinição de tbn</span><span class="sxs-lookup"><span data-stu-id="796cf-105">TBN\_RESET notification code</span></span>

<span data-ttu-id="796cf-106">Notifica a janela pai da barra de ferramentas que o usuário redefiniu o conteúdo da caixa de diálogo Personalizar barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="796cf-106">Notifies the toolbar's parent window that the user has reset the content of the Customize Toolbar dialog box.</span></span> <span data-ttu-id="796cf-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="796cf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="796cf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="796cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="796cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="796cf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="796cf-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="796cf-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="796cf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="796cf-111">Return value</span></span>

<span data-ttu-id="796cf-112">Retorne TBNRF \_ ENDcustomizate para fechar a caixa de diálogo Personalizar barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="796cf-112">Return TBNRF\_ENDCUSTOMIZE to close the Customize Toolbar dialog box.</span></span> <span data-ttu-id="796cf-113">Todos os outros valores de retorno são ignorados.</span><span class="sxs-lookup"><span data-stu-id="796cf-113">All other return values are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="796cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="796cf-114">Requirements</span></span>



| <span data-ttu-id="796cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="796cf-115">Requirement</span></span> | <span data-ttu-id="796cf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="796cf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="796cf-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="796cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="796cf-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="796cf-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="796cf-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="796cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="796cf-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="796cf-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="796cf-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="796cf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="796cf-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="796cf-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





