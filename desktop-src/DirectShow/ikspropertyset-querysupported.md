---
description: O método QuerySupported determina se um objeto dá suporte a um conjunto de propriedades especificado.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Método IKsPropertySet:: QuerySupported (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163780"
---
# <a name="ikspropertysetquerysupported-method"></a><span data-ttu-id="3ee2b-103">Método IKsPropertySet:: QuerySupported</span><span class="sxs-lookup"><span data-stu-id="3ee2b-103">IKsPropertySet::QuerySupported method</span></span>

<span data-ttu-id="3ee2b-104">O `QuerySupported` método determina se um objeto dá suporte a um conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-104">The `QuerySupported` method determines whether an object supports a specified property set.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee2b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ee2b-105">Syntax</span></span>


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a><span data-ttu-id="3ee2b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ee2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ee2b-107">*guidPropSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ee2b-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee2b-108">GUID do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="3ee2b-109">*dwPropId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ee2b-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee2b-110">Identificador da propriedade dentro do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="3ee2b-111">*pTypeSupport* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ee2b-111">*pTypeSupport* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee2b-112">Ponteiro para um valor no qual armazenar sinalizadores indicando o suporte fornecido pelo driver.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-112">Pointer to a value in which to store flags indicating the support provided by the driver.</span></span> <span data-ttu-id="3ee2b-113">Os sinalizadores com suporte incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-113">Supported flags include the following.</span></span>



| <span data-ttu-id="3ee2b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3ee2b-114">Value</span></span>                    | <span data-ttu-id="3ee2b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ee2b-115">Description</span></span>                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee2b-116">\_Get de suporte do KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="3ee2b-116">KSPROPERTY\_SUPPORT\_GET</span></span> | <span data-ttu-id="3ee2b-117">Você pode recuperar a propriedade chamando o método [**IKsPropertySet:: Get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="3ee2b-117">You can retrieve the property by calling the [**IKsPropertySet::Get**](ikspropertyset-get.md) method.</span></span> |
| <span data-ttu-id="3ee2b-118">\_conjunto de suporte do KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="3ee2b-118">KSPROPERTY\_SUPPORT\_SET</span></span> | <span data-ttu-id="3ee2b-119">Você pode alterar a propriedade chamando [**IKsPropertySet:: Set**](ikspropertyset-set.md).</span><span class="sxs-lookup"><span data-stu-id="3ee2b-119">You can change the property by calling [**IKsPropertySet::Set**](ikspropertyset-set.md).</span></span>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ee2b-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ee2b-120">Return value</span></span>

<span data-ttu-id="3ee2b-121">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ee2b-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3ee2b-122">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-122">Possible values include the following.</span></span>



| <span data-ttu-id="3ee2b-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3ee2b-123">Return code</span></span>                                                                                              | <span data-ttu-id="3ee2b-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ee2b-124">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ee2b-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2b-125"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="3ee2b-126">Há suporte para a combinação de conjunto de propriedades e ID de propriedade especificados.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-126">The specified property set and property ID combination is supported.</span></span><br/> |
| <dl> <span data-ttu-id="3ee2b-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2b-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                | <span data-ttu-id="3ee2b-128">Não há suporte para o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-128">Property set is not supported.</span></span><br/>                                       |
| <dl> <span data-ttu-id="3ee2b-129"><dt>**ID de prop. de E \_ \_ \_ sem suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2b-129"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="3ee2b-130">A ID da propriedade não tem suporte para o conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-130">Property ID is not supported for the specified property set.</span></span><br/>         |
| <dl> <span data-ttu-id="3ee2b-131"><dt>**\_ \_ \_ não há suporte para o conjunto de propriedades E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2b-131"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="3ee2b-132">Não há suporte para o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-132">Property set is not supported.</span></span><br/>                                       |



 

## <a name="remarks"></a><span data-ttu-id="3ee2b-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ee2b-133">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3ee2b-134">Outra interface com esse nome existe no arquivo de cabeçalho dsound. h.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-134">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="3ee2b-135">As duas interfaces não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-135">The two interfaces are not compatible.</span></span> <span data-ttu-id="3ee2b-136">A interface **IKsControl** , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-136">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="3ee2b-137">Você deve incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="3ee2b-137">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ee2b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ee2b-138">Requirements</span></span>



| <span data-ttu-id="3ee2b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ee2b-139">Requirement</span></span> | <span data-ttu-id="3ee2b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="3ee2b-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee2b-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ee2b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee2b-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ee2b-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                       |
| <span data-ttu-id="3ee2b-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ee2b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee2b-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ee2b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="3ee2b-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ee2b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ee2b-146"><dt>KS. h; </dt> <dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2b-146"><dt>Ks.h; </dt> <dt>Ksproxy.h</dt></span></span> </dl> |
| <span data-ttu-id="3ee2b-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ee2b-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ee2b-148"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2b-148"><dt>Strmiids.lib</dt></span></span> </dl>                                                          |



## <a name="see-also"></a><span data-ttu-id="3ee2b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ee2b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee2b-150">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="3ee2b-150">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="3ee2b-151">**Interface IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="3ee2b-151">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="3ee2b-152">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="3ee2b-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




