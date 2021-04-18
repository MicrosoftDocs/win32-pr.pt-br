---
description: O método item do objeto SWbemMethodSet retorna um objeto nomeado SWbemMethod da coleção.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Método SWbemMethodSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813543"
---
# <a name="swbemmethodsetitem-method"></a><span data-ttu-id="3e902-103">Método SWbemMethodSet. Item</span><span class="sxs-lookup"><span data-stu-id="3e902-103">SWbemMethodSet.Item method</span></span>

<span data-ttu-id="3e902-104">O método **Item** do objeto [**SWbemMethodSet**](swbemmethodset.md) retorna um objeto nomeado [**SWbemMethod**](swbemmethod.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="3e902-104">The **Item** method of the [**SWbemMethodSet**](swbemmethodset.md) object returns a named [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span>

<span data-ttu-id="3e902-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e902-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e902-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e902-106">Syntax</span></span>


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3e902-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e902-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e902-108">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e902-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e902-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3e902-109">Required.</span></span> <span data-ttu-id="3e902-110">Nome do método a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3e902-110">Name of the method to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3e902-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3e902-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e902-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3e902-112">Reserved.</span></span> <span data-ttu-id="3e902-113">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="3e902-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e902-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e902-114">Return value</span></span>

<span data-ttu-id="3e902-115">Se for bem-sucedido, o objeto [**SWbemMethod**](swbemmethod.md) solicitado retornará.</span><span class="sxs-lookup"><span data-stu-id="3e902-115">If successful, the requested [**SWbemMethod**](swbemmethod.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e902-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3e902-116">Error codes</span></span>

<span data-ttu-id="3e902-117">Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e902-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="3e902-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="3e902-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="3e902-119">O parâmetro *iFlags* não era válido.</span><span class="sxs-lookup"><span data-stu-id="3e902-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3e902-120">**wbemErrFailed** -2147749894</span><span class="sxs-lookup"><span data-stu-id="3e902-120">**wbemErrFailed** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="3e902-121">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="3e902-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="3e902-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="3e902-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="3e902-123">O método especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="3e902-123">The specified method does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e902-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e902-124">Requirements</span></span>



| <span data-ttu-id="3e902-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e902-125">Requirement</span></span> | <span data-ttu-id="3e902-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3e902-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e902-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e902-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3e902-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e902-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e902-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e902-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3e902-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e902-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e902-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e902-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e902-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e902-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e902-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3e902-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e902-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e902-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e902-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3e902-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e902-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e902-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e902-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e902-137">CLSID</span></span><br/>                    | <span data-ttu-id="3e902-138">\_SWBEMMETHODSET CLSID</span><span class="sxs-lookup"><span data-stu-id="3e902-138">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="3e902-139">IID</span><span class="sxs-lookup"><span data-stu-id="3e902-139">IID</span></span><br/>                      | <span data-ttu-id="3e902-140">ISWbemMethodSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="3e902-140">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="3e902-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e902-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e902-142">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="3e902-142">**SWbemMethodSet**</span></span>](swbemmethodset.md)
</dt> <dt>

[<span data-ttu-id="3e902-143">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="3e902-143">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> </dl>

 

 




