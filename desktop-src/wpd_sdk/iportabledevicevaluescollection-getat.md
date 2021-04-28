---
description: 'Método IPortableDeviceValuesCollection:: GetAt – o método GetAt recupera um item da coleção por um índice baseado em zero.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'Método IPortableDeviceValuesCollection:: GetAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083236"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="203dd-103">Método IPortableDeviceValuesCollection:: GetAt</span><span class="sxs-lookup"><span data-stu-id="203dd-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="203dd-104">O método **GetAt** recupera um item da coleção por um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="203dd-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="203dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="203dd-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="203dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="203dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="203dd-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="203dd-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="203dd-108">**DWORD** que especifica um índice de base zero na coleção.</span><span class="sxs-lookup"><span data-stu-id="203dd-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="203dd-109">*ppValues* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="203dd-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="203dd-110">Endereço de uma variável que recebe um ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="203dd-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="203dd-111">O chamador é responsável por chamar o **lançamento** nessa interface quando feito com ele.</span><span class="sxs-lookup"><span data-stu-id="203dd-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="203dd-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="203dd-112">Return value</span></span>

<span data-ttu-id="203dd-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="203dd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="203dd-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="203dd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="203dd-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="203dd-115">Return code</span></span>                                                                                  | <span data-ttu-id="203dd-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="203dd-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="203dd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="203dd-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="203dd-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="203dd-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="203dd-120">O índice de base zero que foi passado estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="203dd-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="203dd-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="203dd-122">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="203dd-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="203dd-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="203dd-124">A coleção contém um ponteiro **IPortableDeviceValues** **nulo** .</span><span class="sxs-lookup"><span data-stu-id="203dd-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="203dd-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="203dd-125">Remarks</span></span>

<span data-ttu-id="203dd-126">Quaisquer alterações feitas aos valores na interface recuperada serão feitas na versão armazenada na coleção.</span><span class="sxs-lookup"><span data-stu-id="203dd-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="203dd-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="203dd-127">Requirements</span></span>



| <span data-ttu-id="203dd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="203dd-128">Requirement</span></span> | <span data-ttu-id="203dd-129">Valor</span><span class="sxs-lookup"><span data-stu-id="203dd-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203dd-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="203dd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="203dd-131"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="203dd-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="203dd-132">Library</span></span><br/> | <dl> <span data-ttu-id="203dd-133"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203dd-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="203dd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203dd-135">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="203dd-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




