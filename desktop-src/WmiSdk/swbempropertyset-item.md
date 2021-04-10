---
description: O método item do objeto SWbemPropertySet Obtém um SWbemProperty nomeado da coleção. Este é o método padrão para esse objeto.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171780"
---
# <a name="swbempropertysetitem-method"></a><span data-ttu-id="ff2cc-104">Método SWbemPropertySet. Item</span><span class="sxs-lookup"><span data-stu-id="ff2cc-104">SWbemPropertySet.Item method</span></span>

<span data-ttu-id="ff2cc-105">O método **Item** do objeto [**SWbemPropertySet**](swbempropertyset.md) Obtém um [**SWbemProperty**](swbemproperty.md) nomeado da coleção.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-105">The **Item** method of the [**SWbemPropertySet**](swbempropertyset.md) object gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="ff2cc-106">Este é o método padrão para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-106">This is the default method for this object.</span></span>

<span data-ttu-id="ff2cc-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ff2cc-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff2cc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff2cc-108">Syntax</span></span>


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ff2cc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff2cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff2cc-110">*strName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff2cc-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff2cc-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-111">Required.</span></span> <span data-ttu-id="ff2cc-112">Nome da propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-112">Name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ff2cc-113">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ff2cc-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ff2cc-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-114">Reserved.</span></span> <span data-ttu-id="ff2cc-115">Esse valor deve ser zero, se especificado.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-115">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff2cc-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff2cc-116">Return value</span></span>

<span data-ttu-id="ff2cc-117">Se for bem-sucedido, o objeto [**SWbemProperty**](swbemproperty.md) solicitado será retornado.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-117">If successful, the requested [**SWbemProperty**](swbemproperty.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff2cc-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ff2cc-118">Error codes</span></span>

<span data-ttu-id="ff2cc-119">Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-119">After the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ff2cc-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ff2cc-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ff2cc-121">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="ff2cc-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ff2cc-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ff2cc-123">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="ff2cc-124">**wbemErrOutOfMemory** -2147749896</span><span class="sxs-lookup"><span data-stu-id="ff2cc-124">**wbemErrOutOfMemory** - 2147749896</span></span>
</dt> <dd>

<span data-ttu-id="ff2cc-125">Não há memória suficiente para execução deste método.</span><span class="sxs-lookup"><span data-stu-id="ff2cc-125">Not enough memory for this method to execute.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff2cc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff2cc-126">Requirements</span></span>



| <span data-ttu-id="ff2cc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff2cc-127">Requirement</span></span> | <span data-ttu-id="ff2cc-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ff2cc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff2cc-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff2cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ff2cc-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff2cc-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff2cc-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff2cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ff2cc-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff2cc-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff2cc-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff2cc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff2cc-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff2cc-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff2cc-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ff2cc-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff2cc-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ff2cc-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ff2cc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ff2cc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff2cc-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff2cc-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff2cc-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="ff2cc-139">CLSID</span></span><br/>                    | <span data-ttu-id="ff2cc-140">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="ff2cc-140">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="ff2cc-141">IID</span><span class="sxs-lookup"><span data-stu-id="ff2cc-141">IID</span></span><br/>                      | <span data-ttu-id="ff2cc-142">ISWbemPropertySet de IID \_</span><span class="sxs-lookup"><span data-stu-id="ff2cc-142">IID\_ISWbemPropertySet</span></span><br/>                                                       |



 

 




