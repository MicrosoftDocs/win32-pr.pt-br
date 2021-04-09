---
title: Mensagem de IPM_SETADDRESS (commctrl. h)
description: Define os valores de endereço para todos os quatro campos no controle de endereço IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- Controles de IPM_SETADDRESS de mensagens do Windows
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085817"
---
# <a name="ipm_setaddress-message"></a><span data-ttu-id="c5ad2-104">\_Mensagem de SETADDRESS IPM</span><span class="sxs-lookup"><span data-stu-id="c5ad2-104">IPM\_SETADDRESS message</span></span>

<span data-ttu-id="c5ad2-105">Define os valores de endereço para todos os quatro campos no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-105">Sets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5ad2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ad2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5ad2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c5ad2-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c5ad2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5ad2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ad2-110">Um valor **DWORD** que contém o novo endereço.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-110">A **DWORD** value that contains the new address.</span></span> <span data-ttu-id="c5ad2-111">O valor do campo 3 está contido em bits 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-111">The field 3 value is contained in bits 0 through 7.</span></span> <span data-ttu-id="c5ad2-112">O valor do campo 2 está contido em bits 8 a 15.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-112">The field 2 value is contained in bits 8 through 15.</span></span> <span data-ttu-id="c5ad2-113">O valor do campo 1 está contido nos bits 16 a 23.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-113">The field 1 value is contained in bits 16 through 23.</span></span> <span data-ttu-id="c5ad2-114">O valor do campo 0 está contido em bits 24 a 31.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-114">The field 0 value is contained in bits 24 through 31.</span></span> <span data-ttu-id="c5ad2-115">A macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) também pode ser usada para criar as informações de endereço.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-115">The [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) macro can also be used to create the address information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ad2-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5ad2-116">Return value</span></span>

<span data-ttu-id="c5ad2-117">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-117">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ad2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5ad2-118">Remarks</span></span>

<span data-ttu-id="c5ad2-119">Essa mensagem não gera uma notificação [**\_ FieldChanged IPN**](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ad2-119">This message does not generate an [**IPN\_FIELDCHANGED**](ipn-fieldchanged.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ad2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ad2-120">Requirements</span></span>



| <span data-ttu-id="c5ad2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ad2-121">Requirement</span></span> | <span data-ttu-id="c5ad2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c5ad2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ad2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5ad2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ad2-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5ad2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5ad2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5ad2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ad2-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5ad2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5ad2-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5ad2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ad2-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ad2-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





