---
title: Session.BatPropriedade chItems (WSManDisp. h)
description: Define e Obtém o número de itens em cada lote de enumeração.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade BatchItems
- Gerenciamento Remoto do Windows da propriedade BatchItems, objeto Session
- Objeto de sessão Gerenciamento Remoto do Windows, Propriedade BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105791308"
---
# <a name="sessionbatchitems-property"></a><span data-ttu-id="7ff5d-106">Session.BatPropriedade chItems</span><span class="sxs-lookup"><span data-stu-id="7ff5d-106">Session.BatchItems property</span></span>

<span data-ttu-id="7ff5d-107">Define e Obtém o número de itens em cada lote de enumeração.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-107">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="7ff5d-108">Esse valor não pode ser alterado durante uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-108">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="7ff5d-109">O provedor de recursos pode definir um limite.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-109">The resource provider may set a limit.</span></span>

<span data-ttu-id="7ff5d-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff5d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ff5d-111">Syntax</span></span>


```VB
Session.BatchItems As long
```



## <a name="property-value"></a><span data-ttu-id="7ff5d-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7ff5d-112">Property value</span></span>

<span data-ttu-id="7ff5d-113">Especifica o número máximo de elementos retornados para cada chamada de rede subjacente ao serviço.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-113">Specifies the maximum number of elements returned for each underlying network call to the service.</span></span> <span data-ttu-id="7ff5d-114">O padrão é 20.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-114">The default is 20.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff5d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ff5d-115">Remarks</span></span>

<span data-ttu-id="7ff5d-116">Esse é um recurso de otimização que controla a frequência com que as chamadas de rede são feitas entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-116">This is an optimization feature that controls how often network calls are made between the client and the server.</span></span> <span data-ttu-id="7ff5d-117">Atualmente, ele é usado apenas para enumerações.</span><span class="sxs-lookup"><span data-stu-id="7ff5d-117">Currently, it is used only for enumerations.</span></span> <span data-ttu-id="7ff5d-118">Para obter mais informações sobre como enumerar recursos, consulte [**enumerar**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="7ff5d-118">For more information about enumerating resources, see [**Enumerate**](session-enumerate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff5d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ff5d-119">Requirements</span></span>



| <span data-ttu-id="7ff5d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff5d-120">Requirement</span></span> | <span data-ttu-id="7ff5d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7ff5d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff5d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ff5d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff5d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ff5d-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7ff5d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ff5d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff5d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ff5d-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7ff5d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ff5d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ff5d-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5d-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ff5d-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="7ff5d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ff5d-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5d-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ff5d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ff5d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ff5d-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5d-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ff5d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff5d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff5d-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5d-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ff5d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ff5d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff5d-135">**Session**</span><span class="sxs-lookup"><span data-stu-id="7ff5d-135">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="7ff5d-136">**Enumerar**</span><span class="sxs-lookup"><span data-stu-id="7ff5d-136">**Enumerate**</span></span>](session-enumerate.md)
</dt> <dt>

[<span data-ttu-id="7ff5d-137">**Enumerator. ReadItem**</span><span class="sxs-lookup"><span data-stu-id="7ff5d-137">**Enumerator.ReadItem**</span></span>](enumerator-readitem.md)
</dt> </dl>

 

 





