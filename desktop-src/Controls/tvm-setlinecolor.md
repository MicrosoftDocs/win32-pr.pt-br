---
title: Mensagem de TVM_SETLINECOLOR (commctrl. h)
description: A \_ mensagem TVM SETLINECOLOR define a cor da linha atual.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Controles de TVM_SETLINECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009479"
---
# <a name="tvm_setlinecolor-message"></a><span data-ttu-id="81dde-104">\_Mensagem TVM SETLINECOLOR</span><span class="sxs-lookup"><span data-stu-id="81dde-104">TVM\_SETLINECOLOR message</span></span>

<span data-ttu-id="81dde-105">A mensagem **TVM \_ SETLINECOLOR** define a cor da linha atual.</span><span class="sxs-lookup"><span data-stu-id="81dde-105">The **TVM\_SETLINECOLOR** message sets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="81dde-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81dde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81dde-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81dde-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="81dde-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="81dde-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="81dde-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81dde-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81dde-110">Nova cor da linha.</span><span class="sxs-lookup"><span data-stu-id="81dde-110">New line color.</span></span> <span data-ttu-id="81dde-111">Use o \_ valor padrão do CLR para restaurar as cores padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="81dde-111">Use the CLR\_DEFAULT value to restore the system default colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81dde-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81dde-112">Return value</span></span>

<span data-ttu-id="81dde-113">Retorna a cor da linha anterior.</span><span class="sxs-lookup"><span data-stu-id="81dde-113">Returns the previous line color.</span></span>

## <a name="remarks"></a><span data-ttu-id="81dde-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="81dde-114">Remarks</span></span>

<span data-ttu-id="81dde-115">Essa mensagem altera apenas as cores de linha.</span><span class="sxs-lookup"><span data-stu-id="81dde-115">This message only changes line colors.</span></span> <span data-ttu-id="81dde-116">Para alterar as cores de ' + ' e '-' dentro dos botões, use a mensagem [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="81dde-116">To change the colors of the '+' and '-' inside the buttons, use the [**TVM\_SETTEXTCOLOR**](tvm-settextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="81dde-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81dde-117">Requirements</span></span>



| <span data-ttu-id="81dde-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="81dde-118">Requirement</span></span> | <span data-ttu-id="81dde-119">Valor</span><span class="sxs-lookup"><span data-stu-id="81dde-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81dde-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81dde-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81dde-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81dde-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81dde-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81dde-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81dde-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81dde-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81dde-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81dde-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="81dde-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81dde-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81dde-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="81dde-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81dde-127">**TVM \_ GETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="81dde-127">**TVM\_GETLINECOLOR**</span></span>](tvm-getlinecolor.md)
</dt> </dl>

 

 





