---
title: TBN_WRAPHOTITEM código de notificação (commctrl. h)
description: Notifica um aplicativo com duas ou mais barras de ferramentas que o item ativo está prestes a alterar. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455007"
---
# <a name="tbn_wraphotitem-notification-code"></a><span data-ttu-id="a3b13-105">Código de notificação do TBN \_ WRAPHOTITEM</span><span class="sxs-lookup"><span data-stu-id="a3b13-105">TBN\_WRAPHOTITEM notification code</span></span>

<span data-ttu-id="a3b13-106">Notifica um aplicativo com duas ou mais barras de ferramentas que o item ativo está prestes a alterar.</span><span class="sxs-lookup"><span data-stu-id="a3b13-106">Notifies an application with two or more toolbars that the hot item is about to change.</span></span> <span data-ttu-id="a3b13-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b13-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a3b13-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3b13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3b13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3b13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3b13-110">Um ponteiro para uma estrutura que contém o item quente antigo (**isniciar**) e se o novo item ativo está antes dele (**iDir** =-1) ou depois dele (**iDir** = 1), bem como um motivo pelo qual o item ativo está mudando.</span><span class="sxs-lookup"><span data-stu-id="a3b13-110">A pointer to a structure that contains the old hot item (**iStart**) and whether the new hot item is before it (**iDir** = -1) or after it (**iDir** = 1), as well as a reason why the hot item is changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3b13-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3b13-111">Return value</span></span>

<span data-ttu-id="a3b13-112">**True** se o aplicativo estiver lidando com a alteração de item quente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="a3b13-112">**TRUE** if the application is handling the hot item change itself; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3b13-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3b13-113">Remarks</span></span>

<span data-ttu-id="a3b13-114">A estrutura **NMTBWRAPHOTITEM** deve ser definida pelo aplicativo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a3b13-114">The **NMTBWRAPHOTITEM** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a><span data-ttu-id="a3b13-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3b13-115">Requirements</span></span>



| <span data-ttu-id="a3b13-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3b13-116">Requirement</span></span> | <span data-ttu-id="a3b13-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a3b13-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b13-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3b13-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a3b13-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3b13-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3b13-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3b13-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a3b13-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3b13-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3b13-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3b13-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3b13-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3b13-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





