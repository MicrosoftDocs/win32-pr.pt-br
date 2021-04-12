---
description: O método Get recupera uma propriedade identificada por um GUID do conjunto de propriedades e uma ID de propriedade.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Método IKsPropertySet:: Get (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456635"
---
# <a name="ikspropertysetget-method"></a><span data-ttu-id="14c97-103">Método IKsPropertySet:: Get</span><span class="sxs-lookup"><span data-stu-id="14c97-103">IKsPropertySet::Get method</span></span>

<span data-ttu-id="14c97-104">O método **Get** recupera uma propriedade identificada por um GUID do conjunto de propriedades e uma ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="14c97-104">The **Get** method retrieves a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14c97-105">Syntax</span></span>


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a><span data-ttu-id="14c97-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14c97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c97-107">*guidPropSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c97-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c97-108">O GUID do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="14c97-108">The GUID of the property set .</span></span>

</dd> <dt>

<span data-ttu-id="14c97-109">*dwPropId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c97-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c97-110">O identificador da propriedade dentro do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="14c97-110">The identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="14c97-111">*pInstanceData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c97-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c97-112">Um ponteiro para uma matriz de bytes que contém dados de instância para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="14c97-112">A pointer to an array of bytes that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="14c97-113">*cbInstanceData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c97-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c97-114">O tamanho da matriz fornecida em *pInstanceData*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="14c97-114">The size of the array given in *pInstanceData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="14c97-115">*pPropData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="14c97-115">*pPropData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14c97-116">Um ponteiro para uma matriz de bytes que recebe os dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="14c97-116">A pointer to an array of bytes that receives the property data.</span></span>

</dd> <dt>

<span data-ttu-id="14c97-117">*cbPropData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c97-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c97-118">O tamanho da matriz fornecida em *pPropData*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="14c97-118">The size of the array given in *pPropData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="14c97-119">*pcbReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="14c97-119">*pcbReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14c97-120">Recebe o número de bytes que o método copia para a matriz *pPropData* .</span><span class="sxs-lookup"><span data-stu-id="14c97-120">Receives the number of bytes the method copies to the *pPropData* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c97-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14c97-121">Return value</span></span>

<span data-ttu-id="14c97-122">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14c97-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="14c97-123">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="14c97-123">Possible values include the following.</span></span>



| <span data-ttu-id="14c97-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="14c97-124">Return code</span></span>                                                                                              | <span data-ttu-id="14c97-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="14c97-125">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14c97-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14c97-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="14c97-127">Êxito.</span><span class="sxs-lookup"><span data-stu-id="14c97-127">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="14c97-128"><dt>**\_ \_ \_ não há suporte para o conjunto de propriedades E**</dt></span><span class="sxs-lookup"><span data-stu-id="14c97-128"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="14c97-129">Não há suporte para o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="14c97-129">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="14c97-130"><dt>**ID de prop. de E \_ \_ \_ sem suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="14c97-130"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="14c97-131">A ID da propriedade não tem suporte para o conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="14c97-131">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14c97-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="14c97-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="14c97-133">Outra interface com esse nome existe no arquivo de cabeçalho dsound. h.</span><span class="sxs-lookup"><span data-stu-id="14c97-133">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="14c97-134">As duas interfaces não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="14c97-134">The two interfaces are not compatible.</span></span> <span data-ttu-id="14c97-135">A interface [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="14c97-135">The [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="14c97-136">Para recuperar uma propriedade, aloque um buffer que esse método irá preencher.</span><span class="sxs-lookup"><span data-stu-id="14c97-136">To retrieve a property, allocate a buffer which this method will then fill in.</span></span> <span data-ttu-id="14c97-137">Para determinar o tamanho de buffer necessário, especifique **NULL** para *pPropData* e zero (0) para *cbPropData*.</span><span class="sxs-lookup"><span data-stu-id="14c97-137">To determine the necessary buffer size, specify **NULL** for *pPropData* and zero (0) for *cbPropData*.</span></span> <span data-ttu-id="14c97-138">Esse método retorna o tamanho de buffer necessário em *pcbReturned*.</span><span class="sxs-lookup"><span data-stu-id="14c97-138">This method returns the necessary buffer size in *pcbReturned*.</span></span>

<span data-ttu-id="14c97-139">Você deve incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="14c97-139">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="14c97-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14c97-140">Examples</span></span>

<span data-ttu-id="14c97-141">O exemplo a seguir consulta um PIN para sua categoria de PIN, recuperando a propriedade de **\_ \_ categoria AMPROPERTY PIN** .</span><span class="sxs-lookup"><span data-stu-id="14c97-141">The following example queries a pin for its pin category, by retrieving the **AMPROPERTY\_PIN\_CATEGORY** property.</span></span> <span data-ttu-id="14c97-142">(Consulte [PIN conjunto de propriedades](pin-property-set.md).)</span><span class="sxs-lookup"><span data-stu-id="14c97-142">(See [Pin Property Set](pin-property-set.md).)</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="14c97-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14c97-143">Requirements</span></span>



| <span data-ttu-id="14c97-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c97-144">Requirement</span></span> | <span data-ttu-id="14c97-145">Valor</span><span class="sxs-lookup"><span data-stu-id="14c97-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c97-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14c97-146">Minimum supported client</span></span><br/> | <span data-ttu-id="14c97-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14c97-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14c97-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14c97-148">Minimum supported server</span></span><br/> | <span data-ttu-id="14c97-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14c97-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14c97-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="14c97-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c97-151"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c97-151"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="14c97-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14c97-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="14c97-153"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c97-153"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c97-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="14c97-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c97-155">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="14c97-155">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="14c97-156">**Interface IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="14c97-156">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="14c97-157">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="14c97-157">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
