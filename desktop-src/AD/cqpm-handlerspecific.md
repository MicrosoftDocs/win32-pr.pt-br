---
title: Mensagem de CQPM_HANDLERSPECIFIC (Cmnquery. h)
description: Valor base usado para mensagens que são privadas para o manipulador de consulta.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_HANDLERSPECIFIC Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454769"
---
# <a name="cqpm_handlerspecific-message"></a><span data-ttu-id="1cc21-104">\_Mensagem CQPM HANDLERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="1cc21-104">CQPM\_HANDLERSPECIFIC message</span></span>

<span data-ttu-id="1cc21-105">A mensagem **CQPM \_ HANDLERSPECIFIC** é o valor base usado para mensagens que são particulares ao manipulador de consultas.</span><span class="sxs-lookup"><span data-stu-id="1cc21-105">The **CQPM\_HANDLERSPECIFIC** message is the base value used for messages that are private to the query handler.</span></span> <span data-ttu-id="1cc21-106">O manipulador de consulta deve adicionar esse valor a mensagens privadas para garantir que as colisões de mensagem não ocorram.</span><span class="sxs-lookup"><span data-stu-id="1cc21-106">The query handler should add this value to private messages to ensure that message collisions do not occur.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cc21-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cc21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc21-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cc21-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc21-109">Contém dados de mensagem adicionais.</span><span class="sxs-lookup"><span data-stu-id="1cc21-109">Contains additional message data.</span></span> <span data-ttu-id="1cc21-110">O conteúdo desse parâmetro é definido pelo manipulador de consulta.</span><span class="sxs-lookup"><span data-stu-id="1cc21-110">The content of this parameter is defined by the query handler.</span></span>

</dd> <dt>

<span data-ttu-id="1cc21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cc21-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc21-112">Contém dados de mensagem adicionais.</span><span class="sxs-lookup"><span data-stu-id="1cc21-112">Contains additional message data.</span></span> <span data-ttu-id="1cc21-113">O conteúdo desse parâmetro é definido pelo manipulador de consulta.</span><span class="sxs-lookup"><span data-stu-id="1cc21-113">The content of this parameter is defined by the query handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc21-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cc21-114">Return value</span></span>

<span data-ttu-id="1cc21-115">O significado do valor de retorno é definido pelo manipulador de consulta.</span><span class="sxs-lookup"><span data-stu-id="1cc21-115">The meaning of the return value is defined by the query handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc21-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc21-116">Requirements</span></span>



| <span data-ttu-id="1cc21-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc21-117">Requirement</span></span> | <span data-ttu-id="1cc21-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1cc21-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc21-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cc21-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc21-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cc21-120">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="1cc21-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cc21-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc21-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cc21-122">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="1cc21-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cc21-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc21-124"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc21-124"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc21-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cc21-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc21-126">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="1cc21-126">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





