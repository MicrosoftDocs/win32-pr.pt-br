---
description: O método clone do objeto SWbemNamedValueSet retorna um novo objeto que é um clone da coleção atual.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Clone (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662313"
---
# <a name="swbemnamedvaluesetclone-method"></a><span data-ttu-id="5b5a4-103">Método SWbemNamedValueSet. Clone</span><span class="sxs-lookup"><span data-stu-id="5b5a4-103">SWbemNamedValueSet.Clone method</span></span>

<span data-ttu-id="5b5a4-104">O método **clone** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) retorna um novo objeto que é um clone da coleção atual.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-104">The **Clone** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns a new object that is a clone of the current collection.</span></span>

<span data-ttu-id="5b5a4-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5b5a4-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5a4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b5a4-106">Syntax</span></span>


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a><span data-ttu-id="5b5a4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b5a4-107">Parameters</span></span>

<span data-ttu-id="5b5a4-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b5a4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b5a4-109">Return value</span></span>

<span data-ttu-id="5b5a4-110">Se for bem-sucedido, um novo objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) retornará.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-110">If successful, a new [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5b5a4-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5b5a4-111">Error codes</span></span>

<span data-ttu-id="5b5a4-112">Após a conclusão do método **clone** , o objeto **Err** pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-112">Upon completion of the **Clone** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="5b5a4-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5b5a4-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5b5a4-114">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5b5a4-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5b5a4-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5b5a4-116">Não há memória suficiente para clonar o objeto.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-116">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b5a4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b5a4-117">Remarks</span></span>

<span data-ttu-id="5b5a4-118">Use este método para duplicar uma coleção [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="5b5a4-118">Use this method to duplicate an [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5a4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5a4-119">Requirements</span></span>



| <span data-ttu-id="5b5a4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5a4-120">Requirement</span></span> | <span data-ttu-id="5b5a4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5b5a4-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5a4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5a4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5a4-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b5a4-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b5a4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5a4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5a4-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b5a4-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b5a4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b5a4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5a4-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5a4-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b5a4-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5b5a4-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b5a4-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5b5a4-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5b5a4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5b5a4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b5a4-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b5a4-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b5a4-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="5b5a4-132">CLSID</span></span><br/>                    | <span data-ttu-id="5b5a4-133">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="5b5a4-133">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="5b5a4-134">IID</span><span class="sxs-lookup"><span data-stu-id="5b5a4-134">IID</span></span><br/>                      | <span data-ttu-id="5b5a4-135">ISWbemNamedValueSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="5b5a4-135">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="5b5a4-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b5a4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5a4-137">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="5b5a4-137">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




