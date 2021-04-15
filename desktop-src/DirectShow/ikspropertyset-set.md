---
description: O método set define uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'Método IKsPropertySet:: Set (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370193"
---
# <a name="ikspropertysetset-method"></a><span data-ttu-id="f9362-103">Método IKsPropertySet:: Set</span><span class="sxs-lookup"><span data-stu-id="f9362-103">IKsPropertySet::Set method</span></span>

<span data-ttu-id="f9362-104">O `Set` método define uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f9362-104">The `Set` method sets a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9362-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9362-105">Syntax</span></span>


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a><span data-ttu-id="f9362-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9362-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9362-107">*guidPropSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9362-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9362-108">GUID do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f9362-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="f9362-109">*dwPropId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9362-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9362-110">Identificador da propriedade dentro do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f9362-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="f9362-111">*pInstanceData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9362-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9362-112">Ponteiro para um buffer que contém dados de instância para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="f9362-112">Pointer to a buffer that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="f9362-113">*cbInstanceData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9362-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9362-114">Tamanho do buffer *pInstanceData* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="f9362-114">Size of the *pInstanceData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9362-115">*pPropData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9362-115">*pPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9362-116">Ponteiro para um buffer que contém o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="f9362-116">Pointer to a buffer that contains the value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="f9362-117">*cbPropData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9362-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9362-118">Sise do buffer *pPropData* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="f9362-118">Sise of the *pPropData* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9362-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9362-119">Return value</span></span>

<span data-ttu-id="f9362-120">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9362-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f9362-121">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="f9362-121">Possible values include the following.</span></span>



| <span data-ttu-id="f9362-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f9362-122">Return code</span></span>                                                                                              | <span data-ttu-id="f9362-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9362-123">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9362-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9362-124"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="f9362-125">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f9362-125">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="f9362-126"><dt>**\_ \_ \_ não há suporte para o conjunto de propriedades E**</dt></span><span class="sxs-lookup"><span data-stu-id="f9362-126"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="f9362-127">Não há suporte para o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f9362-127">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="f9362-128"><dt>**ID de prop. de E \_ \_ \_ sem suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="f9362-128"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="f9362-129">A ID da propriedade não tem suporte para o conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="f9362-129">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9362-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9362-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9362-131">Outra interface com esse nome existe no arquivo de cabeçalho dsound. h.</span><span class="sxs-lookup"><span data-stu-id="f9362-131">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="f9362-132">As duas interfaces não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="f9362-132">The two interfaces are not compatible.</span></span> <span data-ttu-id="f9362-133">A interface **IKsControl** , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="f9362-133">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="f9362-134">Você deve incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="f9362-134">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9362-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9362-135">Requirements</span></span>



| <span data-ttu-id="f9362-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9362-136">Requirement</span></span> | <span data-ttu-id="f9362-137">Valor</span><span class="sxs-lookup"><span data-stu-id="f9362-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9362-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9362-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f9362-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9362-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f9362-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9362-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f9362-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9362-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9362-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f9362-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9362-143"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9362-143"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="f9362-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9362-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9362-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9362-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9362-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9362-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9362-147">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="f9362-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="f9362-148">**Interface IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="f9362-148">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="f9362-149">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="f9362-149">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




