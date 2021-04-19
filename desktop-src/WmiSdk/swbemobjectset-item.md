---
description: O método item do objeto SWbemObjectSet Obtém um SWbemObject da coleção.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Método SWbemObjectSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810818"
---
# <a name="swbemobjectsetitem-method"></a><span data-ttu-id="e28ca-103">Método SWbemObjectSet. Item</span><span class="sxs-lookup"><span data-stu-id="e28ca-103">SWbemObjectSet.Item method</span></span>

<span data-ttu-id="e28ca-104">O método **Item** do objeto [**SWbemObjectSet**](swbemobjectset.md) Obtém um [**SWbemObject**](swbemobject.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="e28ca-104">The **Item** method of the [**SWbemObjectSet**](swbemobjectset.md) object gets an [**SWbemObject**](swbemobject.md) from the collection.</span></span>

<span data-ttu-id="e28ca-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e28ca-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e28ca-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e28ca-106">Syntax</span></span>


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a><span data-ttu-id="e28ca-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e28ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e28ca-108">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="e28ca-108">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="e28ca-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e28ca-109">Required.</span></span> <span data-ttu-id="e28ca-110">Caminho relativo do objeto a ser recuperado da coleção.</span><span class="sxs-lookup"><span data-stu-id="e28ca-110">Relative path of the object to retrieve from the collection.</span></span> <span data-ttu-id="e28ca-111">Exemplo: Win32 \_ LogicalDisk = "C:"</span><span class="sxs-lookup"><span data-stu-id="e28ca-111">Example: Win32\_LogicalDisk="C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e28ca-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e28ca-112">Return value</span></span>

<span data-ttu-id="e28ca-113">Se for bem-sucedido, o objeto [**SWbemObject**](swbemobject.md) solicitado retornará.</span><span class="sxs-lookup"><span data-stu-id="e28ca-113">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e28ca-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e28ca-114">Error codes</span></span>

<span data-ttu-id="e28ca-115">Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="e28ca-115">Upon completion of the **Item** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="e28ca-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e28ca-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e28ca-117">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="e28ca-117">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e28ca-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e28ca-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e28ca-119">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="e28ca-119">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="e28ca-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e28ca-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e28ca-121">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="e28ca-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e28ca-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="e28ca-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="e28ca-123">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e28ca-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e28ca-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e28ca-124">Remarks</span></span>

<span data-ttu-id="e28ca-125">O método **Item** pode exigir muito tempo do processador porque a enumeração completa pelo provedor dos elementos do conjunto é necessária para retornar o resultado.</span><span class="sxs-lookup"><span data-stu-id="e28ca-125">The **Item** method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="e28ca-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e28ca-126">Requirements</span></span>



| <span data-ttu-id="e28ca-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e28ca-127">Requirement</span></span> | <span data-ttu-id="e28ca-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e28ca-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e28ca-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e28ca-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e28ca-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e28ca-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e28ca-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e28ca-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e28ca-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e28ca-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e28ca-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e28ca-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e28ca-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e28ca-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e28ca-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e28ca-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="e28ca-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e28ca-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e28ca-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e28ca-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e28ca-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e28ca-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e28ca-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="e28ca-139">CLSID</span></span><br/>                    | <span data-ttu-id="e28ca-140">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="e28ca-140">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="e28ca-141">IID</span><span class="sxs-lookup"><span data-stu-id="e28ca-141">IID</span></span><br/>                      | <span data-ttu-id="e28ca-142">ISWbemObjectSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="e28ca-142">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




