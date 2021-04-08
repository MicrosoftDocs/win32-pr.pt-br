---
title: Mensagem de TVM_GETLINECOLOR (commctrl. h)
description: A \_ mensagem TVM GETLINECOLOR Obtém a cor da linha atual.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Controles de TVM_GETLINECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009517"
---
# <a name="tvm_getlinecolor-message"></a><span data-ttu-id="4c776-104">\_Mensagem TVM GETLINECOLOR</span><span class="sxs-lookup"><span data-stu-id="4c776-104">TVM\_GETLINECOLOR message</span></span>

<span data-ttu-id="4c776-105">A mensagem **TVM \_ GETLINECOLOR** Obtém a cor da linha atual.</span><span class="sxs-lookup"><span data-stu-id="4c776-105">The **TVM\_GETLINECOLOR** message gets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c776-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c776-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c776-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4c776-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4c776-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4c776-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c776-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4c776-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4c776-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c776-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c776-111">Return value</span></span>

<span data-ttu-id="4c776-112">Retorna a cor da linha atual ou o \_ valor padrão do CLR se nenhum tiver sido especificado.</span><span class="sxs-lookup"><span data-stu-id="4c776-112">Returns the current line color, or the CLR\_DEFAULT value if none has been specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c776-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c776-113">Remarks</span></span>

<span data-ttu-id="4c776-114">Esta mensagem recupera apenas as cores de linha.</span><span class="sxs-lookup"><span data-stu-id="4c776-114">This message only retrieves line colors.</span></span> <span data-ttu-id="4c776-115">Para recuperar as cores de ' + ' e '-' dentro dos botões, use a mensagem [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="4c776-115">To retrieve the colors of the '+' and '-' inside the buttons, use the [**TVM\_GETTEXTCOLOR**](tvm-gettextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c776-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c776-116">Requirements</span></span>



| <span data-ttu-id="4c776-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c776-117">Requirement</span></span> | <span data-ttu-id="4c776-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4c776-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c776-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c776-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c776-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c776-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c776-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c776-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c776-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c776-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c776-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c776-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c776-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c776-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c776-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c776-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c776-126">**TVM \_ SETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="4c776-126">**TVM\_SETLINECOLOR**</span></span>](tvm-setlinecolor.md)
</dt> </dl>

 

 





