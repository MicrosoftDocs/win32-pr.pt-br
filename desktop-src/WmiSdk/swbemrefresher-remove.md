---
description: O método SWbemRefresher. Remove remove o objeto SWbemRefreshableItem com o índice especificado do atualizador.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Método SWbemRefresher. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930172"
---
# <a name="swbemrefresherremove-method"></a><span data-ttu-id="4364a-103">Método SWbemRefresher. Remove</span><span class="sxs-lookup"><span data-stu-id="4364a-103">SWbemRefresher.Remove method</span></span>

<span data-ttu-id="4364a-104">O método **SWbemRefresher. Remove** remove o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) com o índice especificado do atualizador.</span><span class="sxs-lookup"><span data-stu-id="4364a-104">The **SWbemRefresher.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object with the specified index from the refresher.</span></span> <span data-ttu-id="4364a-105">O objeto **SWbemRefreshableItem** pode representar um único objeto ou um conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="4364a-105">The **SWbemRefreshableItem** object can represent either a single object or an object set.</span></span>

<span data-ttu-id="4364a-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4364a-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4364a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4364a-107">Syntax</span></span>


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4364a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4364a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4364a-109">*LIndex*</span><span class="sxs-lookup"><span data-stu-id="4364a-109">*LIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="4364a-110">Índice do item no objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="4364a-110">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="4364a-111">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4364a-111">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4364a-112">Os sinalizadores devem ser definidos T0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4364a-112">Flags must be set t0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="4364a-113">*objWbemNamedvalueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4364a-113">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4364a-114">Nulo.</span><span class="sxs-lookup"><span data-stu-id="4364a-114">Null.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4364a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4364a-115">Return value</span></span>

<span data-ttu-id="4364a-116">Este método não tem valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="4364a-116">This method has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4364a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4364a-117">Remarks</span></span>

<span data-ttu-id="4364a-118">**Códigos de erro** Se o atualizador não tiver nenhum item com o índice especificado, **wbemErrNotFound** será gerado.</span><span class="sxs-lookup"><span data-stu-id="4364a-118">**Error codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="4364a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4364a-119">Requirements</span></span>



| <span data-ttu-id="4364a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4364a-120">Requirement</span></span> | <span data-ttu-id="4364a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4364a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4364a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4364a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4364a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4364a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4364a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4364a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4364a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4364a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4364a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4364a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4364a-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4364a-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4364a-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4364a-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="4364a-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4364a-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4364a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4364a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4364a-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4364a-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4364a-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="4364a-132">CLSID</span></span><br/>                    | <span data-ttu-id="4364a-133">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="4364a-133">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="4364a-134">IID</span><span class="sxs-lookup"><span data-stu-id="4364a-134">IID</span></span><br/>                      | <span data-ttu-id="4364a-135">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="4364a-135">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="4364a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4364a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4364a-137">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="4364a-137">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




