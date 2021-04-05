---
title: NM_TVSTATEIMAGECHANGING código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore para sua janela pai que a imagem de estado está sendo alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- NM_TVSTATEIMAGECHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085395"
---
# <a name="nm_tvstateimagechanging-notification-code"></a><span data-ttu-id="3f612-105">\_Código de notificação nm TVSTATEIMAGECHANGING</span><span class="sxs-lookup"><span data-stu-id="3f612-105">NM\_TVSTATEIMAGECHANGING notification code</span></span>

<span data-ttu-id="3f612-106">Enviado por um controle de exibição de árvore para sua janela pai que a imagem de estado está sendo alterada.</span><span class="sxs-lookup"><span data-stu-id="3f612-106">Sent by a tree-view control to its parent window that the state image is changing.</span></span> <span data-ttu-id="3f612-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3f612-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3f612-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f612-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f612-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f612-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f612-110">Um ponteiro para uma estrutura [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="3f612-110">A pointer to an [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f612-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f612-111">Return value</span></span>

<span data-ttu-id="3f612-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="3f612-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f612-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f612-113">Requirements</span></span>



| <span data-ttu-id="3f612-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f612-114">Requirement</span></span> | <span data-ttu-id="3f612-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3f612-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f612-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f612-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f612-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f612-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f612-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f612-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f612-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f612-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f612-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f612-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f612-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f612-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





