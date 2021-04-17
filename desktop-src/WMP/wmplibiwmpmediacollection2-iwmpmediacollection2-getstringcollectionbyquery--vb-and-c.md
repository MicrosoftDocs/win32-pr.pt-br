---
title: Método IWMPMediaCollection2 getStringCollectionByQuery
description: O método getStringCollectionByQuery retorna uma interface IWMPStringCollection que fornece acesso ao conjunto de todos os valores de cadeia de caracteres para um atributo especificado que corresponde às condições de consulta.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- método getStringCollectionByQuery Windows Media Player
- método getStringCollectionByQuery Windows Media Player, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 Windows Media Player, método getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782554"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a><span data-ttu-id="39de6-106">Método IWMPMediaCollection2:: getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="39de6-106">IWMPMediaCollection2::getStringCollectionByQuery method</span></span>

<span data-ttu-id="39de6-107">O `getStringCollectionByQuery` método retorna uma interface **IWMPStringCollection** que fornece acesso ao conjunto de todos os valores de cadeia de caracteres para um atributo especificado que corresponde às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="39de6-107">The `getStringCollectionByQuery` method returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="39de6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39de6-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a><span data-ttu-id="39de6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39de6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39de6-110">*bstrattribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39de6-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39de6-111">O **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="39de6-111">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="39de6-112">*pQuery* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39de6-112">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39de6-113">A interface **WMPLib. IWMPQuery** que é a consulta que define as condições usadas para recuperar a coleção de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="39de6-113">The **WMPLib.IWMPQuery** interface that is the query that defines the conditions used to retrieve the string collection.</span></span>

</dd> <dt>

<span data-ttu-id="39de6-114">*bstrMediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39de6-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39de6-115">O **System. String** que é o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="39de6-115">The **System.String** that is the media type.</span></span> <span data-ttu-id="39de6-116">Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".</span><span class="sxs-lookup"><span data-stu-id="39de6-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="39de6-117">*bstrSortAttribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39de6-117">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39de6-118">O **System. String** que é o nome do atributo usado para classificação.</span><span class="sxs-lookup"><span data-stu-id="39de6-118">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="39de6-119">Uma cadeia de caracteres de comprimento zero ("") significa que nenhuma classificação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="39de6-119">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="39de6-120">*fSortAscending* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39de6-120">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39de6-121">O valor **System. Boolean** que indica se o conjunto de valores de cadeia de caracteres deve ser classificado em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="39de6-121">The **System.Boolean** value that indicates whether the set of string values must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39de6-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39de6-122">Return value</span></span>

<span data-ttu-id="39de6-123">Uma interface **WMPLib. IWMPStringCollection** para o conjunto recuperado de valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="39de6-123">A **WMPLib.IWMPStringCollection** interface for the retrieved set of string values.</span></span>

## <a name="remarks"></a><span data-ttu-id="39de6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="39de6-124">Remarks</span></span>

<span data-ttu-id="39de6-125">As consultas compostas usando **IWMPQuery** não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="39de6-125">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="39de6-126">Quando a consulta composta especificada pelo parâmetro *pQuery* contém uma condição criada no atributo **MediaType** , essa condição é ignorada.</span><span class="sxs-lookup"><span data-stu-id="39de6-126">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="39de6-127">O valor para o parâmetro *bstrMediaType* é sempre usado.</span><span class="sxs-lookup"><span data-stu-id="39de6-127">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="39de6-128">Por exemplo, se a consulta composta contiver a condição "MediaType igual a áudio" e o valor do parâmetro *bstrMediaType* for "vídeo", a lista de reprodução resultante conterá apenas itens de vídeo.</span><span class="sxs-lookup"><span data-stu-id="39de6-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="39de6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39de6-129">Requirements</span></span>



| <span data-ttu-id="39de6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="39de6-130">Requirement</span></span> | <span data-ttu-id="39de6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="39de6-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39de6-132">Versão</span><span class="sxs-lookup"><span data-stu-id="39de6-132">Version</span></span><br/>   | <span data-ttu-id="39de6-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="39de6-133">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="39de6-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="39de6-134">Namespace</span></span><br/> | <span data-ttu-id="39de6-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="39de6-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="39de6-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="39de6-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="39de6-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="39de6-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39de6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="39de6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39de6-139">**Interface IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="39de6-139">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="39de6-140">**Interface IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="39de6-140">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="39de6-141">**Interface IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="39de6-141">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="39de6-142">**Atributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="39de6-142">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





