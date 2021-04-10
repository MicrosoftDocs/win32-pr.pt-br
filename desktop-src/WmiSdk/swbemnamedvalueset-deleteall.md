---
description: O método DeleteAll do objeto SWbemNamedValueSet remove todos os valores nomeados da coleção, esvaziando-os.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. DeleteAll (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170004"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a><span data-ttu-id="756bb-103">Método SWbemNamedValueSet. DeleteAll</span><span class="sxs-lookup"><span data-stu-id="756bb-103">SWbemNamedValueSet.DeleteAll method</span></span>

<span data-ttu-id="756bb-104">O método **DeleteAll** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) remove todos os valores nomeados da coleção, esvaziando-os.</span><span class="sxs-lookup"><span data-stu-id="756bb-104">The **DeleteAll** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object removes all named values from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="756bb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="756bb-105">Syntax</span></span>


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="756bb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="756bb-106">Parameters</span></span>

<span data-ttu-id="756bb-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="756bb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="756bb-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="756bb-108">Return value</span></span>

<span data-ttu-id="756bb-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="756bb-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="756bb-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="756bb-110">Error codes</span></span>

<span data-ttu-id="756bb-111">Após a conclusão do método **DeleteAll** , o objeto **Err** pode conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="756bb-111">Upon completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="756bb-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="756bb-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="756bb-113">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="756bb-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="756bb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="756bb-114">Requirements</span></span>



| <span data-ttu-id="756bb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="756bb-115">Requirement</span></span> | <span data-ttu-id="756bb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="756bb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="756bb-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756bb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="756bb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="756bb-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="756bb-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756bb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="756bb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="756bb-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="756bb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="756bb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="756bb-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="756bb-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="756bb-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="756bb-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="756bb-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="756bb-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="756bb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="756bb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="756bb-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="756bb-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="756bb-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="756bb-127">CLSID</span></span><br/>                    | <span data-ttu-id="756bb-128">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="756bb-128">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="756bb-129">IID</span><span class="sxs-lookup"><span data-stu-id="756bb-129">IID</span></span><br/>                      | <span data-ttu-id="756bb-130">ISWbemNamedValueSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="756bb-130">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="756bb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="756bb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756bb-132">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="756bb-132">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> <dt>

[<span data-ttu-id="756bb-133">**SWbemNamedValueSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="756bb-133">**SWbemNamedValueSet.Remove**</span></span>](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




