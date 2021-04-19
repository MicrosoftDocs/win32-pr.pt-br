---
title: TBN_WRAPACCELERATOR código de notificação (commctrl. h)
description: Solicita o índice do botão em uma ou mais barras de ferramentas correspondentes ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748252"
---
# <a name="tbn_wrapaccelerator-notification-code"></a><span data-ttu-id="707c9-105">Código de notificação do TBN \_ WRAPACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="707c9-105">TBN\_WRAPACCELERATOR notification code</span></span>

<span data-ttu-id="707c9-106">Solicita o índice do botão em uma ou mais barras de ferramentas correspondentes ao caractere de acelerador especificado.</span><span class="sxs-lookup"><span data-stu-id="707c9-106">Requests the index of the button in one or more toolbars corresponding to the specified accelerator character.</span></span> <span data-ttu-id="707c9-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="707c9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="707c9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="707c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="707c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="707c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="707c9-110">Um ponteiro para uma estrutura que contém o caractere de tecla acelerador e que recebe o índice do botão correspondente.</span><span class="sxs-lookup"><span data-stu-id="707c9-110">A pointer to a structure that contains the accelerator key character, and that receives the index of the corresponding button.</span></span> <span data-ttu-id="707c9-111">O índice será-1 se o acelerador não corresponder a um comando.</span><span class="sxs-lookup"><span data-stu-id="707c9-111">The index is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="707c9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="707c9-112">Return value</span></span>

<span data-ttu-id="707c9-113">**True** se um índice for retornado, caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="707c9-113">**TRUE** if an index is returned, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="707c9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="707c9-114">Remarks</span></span>

<span data-ttu-id="707c9-115">Aplicativos com uma ou mais barras de ferramentas podem receber esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="707c9-115">Applications with one or more toolbars may receive this notification code.</span></span>

<span data-ttu-id="707c9-116">A estrutura **NMTBWRAPACCELERATOR** deve ser definida pelo aplicativo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="707c9-116">The **NMTBWRAPACCELERATOR** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="707c9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="707c9-117">Requirements</span></span>



| <span data-ttu-id="707c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="707c9-118">Requirement</span></span> | <span data-ttu-id="707c9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="707c9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="707c9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="707c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="707c9-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="707c9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="707c9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="707c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="707c9-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="707c9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="707c9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="707c9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="707c9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="707c9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





