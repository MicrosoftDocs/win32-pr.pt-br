---
title: TBN_DUPACCELERATOR código de notificação (commctrl. h)
description: Asseguro se uma tecla aceleradora pode ser usada em duas ou mais barras de ferramentas ativas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009597"
---
# <a name="tbn_dupaccelerator-notification-code"></a><span data-ttu-id="f37ee-105">Código de notificação do TBN \_ DUPACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="f37ee-105">TBN\_DUPACCELERATOR notification code</span></span>

<span data-ttu-id="f37ee-106">Asseguro se uma tecla aceleradora pode ser usada em duas ou mais barras de ferramentas ativas.</span><span class="sxs-lookup"><span data-stu-id="f37ee-106">Ascertains whether an accelerator key can be used on two or more active toolbars.</span></span> <span data-ttu-id="f37ee-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f37ee-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f37ee-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f37ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f37ee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f37ee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f37ee-110">Um ponteiro para uma estrutura que fornece um acelerador e que recebe um valor que especifica se várias barras de ferramentas respondem ao mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="f37ee-110">A pointer to a structure that provides an accelerator and that receives a value specifying whether multiple toolbars respond to the same character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f37ee-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f37ee-111">Return value</span></span>

<span data-ttu-id="f37ee-112">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f37ee-112">Returns **TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f37ee-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f37ee-113">Remarks</span></span>

<span data-ttu-id="f37ee-114">O aplicativo deve declarar a estrutura **NMTBDUPACCELERATOR** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f37ee-114">The application must declare the **NMTBDUPACCELERATOR** structure as follows:</span></span>

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="f37ee-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f37ee-115">Requirements</span></span>



| <span data-ttu-id="f37ee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f37ee-116">Requirement</span></span> | <span data-ttu-id="f37ee-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f37ee-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f37ee-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f37ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f37ee-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f37ee-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f37ee-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f37ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f37ee-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f37ee-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f37ee-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f37ee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f37ee-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f37ee-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





