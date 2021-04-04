---
description: O método item do objeto SWbemQualifierSet retorna um objeto nomeado SWbemQualifier da coleção. Esse é o método padrão deste objeto.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837166"
---
# <a name="swbemqualifiersetitem-method"></a><span data-ttu-id="b2331-104">Método SWbemQualifierSet. Item</span><span class="sxs-lookup"><span data-stu-id="b2331-104">SWbemQualifierSet.Item method</span></span>

<span data-ttu-id="b2331-105">O método **Item** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) retorna um objeto nomeado [**SWbemQualifier**](swbemqualifier.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="b2331-105">The **Item** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span> <span data-ttu-id="b2331-106">Esse é o método padrão deste objeto.</span><span class="sxs-lookup"><span data-stu-id="b2331-106">This is the default method of this object.</span></span>

<span data-ttu-id="b2331-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b2331-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2331-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2331-108">Syntax</span></span>


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b2331-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2331-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2331-110">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2331-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2331-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="b2331-111">Required.</span></span> <span data-ttu-id="b2331-112">Nome do qualificador a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b2331-112">Name of the qualifier to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b2331-113">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b2331-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2331-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b2331-114">Reserved.</span></span> <span data-ttu-id="b2331-115">O valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b2331-115">The default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2331-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2331-116">Return value</span></span>

<span data-ttu-id="b2331-117">Se for bem-sucedido, o objeto [**SWbemQualifier**](swbemqualifier.md) solicitado será retornado.</span><span class="sxs-lookup"><span data-stu-id="b2331-117">If successful, the requested [**SWbemQualifier**](swbemqualifier.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2331-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b2331-118">Error codes</span></span>

<span data-ttu-id="b2331-119">Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="b2331-119">After completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b2331-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b2331-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b2331-121">O parâmetro *iFlags* não era válido.</span><span class="sxs-lookup"><span data-stu-id="b2331-121">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b2331-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b2331-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b2331-123">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b2331-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b2331-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="b2331-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b2331-125">O qualificador especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="b2331-125">Specified qualifier does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2331-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2331-126">Requirements</span></span>



| <span data-ttu-id="b2331-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2331-127">Requirement</span></span> | <span data-ttu-id="b2331-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b2331-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2331-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2331-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2331-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2331-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2331-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2331-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2331-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2331-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2331-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2331-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2331-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2331-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2331-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b2331-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2331-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2331-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2331-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b2331-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2331-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2331-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2331-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="b2331-139">CLSID</span></span><br/>                    | <span data-ttu-id="b2331-140">\_SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="b2331-140">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="b2331-141">IID</span><span class="sxs-lookup"><span data-stu-id="b2331-141">IID</span></span><br/>                      | <span data-ttu-id="b2331-142">ISWbemQualifierSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="b2331-142">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="b2331-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2331-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2331-144">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="b2331-144">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="b2331-145">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="b2331-145">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

 




