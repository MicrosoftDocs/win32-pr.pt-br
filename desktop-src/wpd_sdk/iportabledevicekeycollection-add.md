---
description: O método add adiciona uma chave de propriedade à coleção.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Método IPortableDeviceKeyCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764227"
---
# <a name="iportabledevicekeycollectionadd-method"></a><span data-ttu-id="8ea26-103">Método IPortableDeviceKeyCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="8ea26-103">IPortableDeviceKeyCollection::Add method</span></span>

<span data-ttu-id="8ea26-104">O método **Add** adiciona uma chave de propriedade à coleção.</span><span class="sxs-lookup"><span data-stu-id="8ea26-104">The **Add** method adds a property key to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea26-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ea26-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a><span data-ttu-id="8ea26-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ea26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea26-107">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8ea26-107">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea26-108">Um **REFPROPERTYKEY** a ser adicionado à coleção.</span><span class="sxs-lookup"><span data-stu-id="8ea26-108">A **REFPROPERTYKEY** to add to the collection.</span></span> <span data-ttu-id="8ea26-109">Esse método copia a chave para a coleção, para que você possa liberar a variável local depois de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="8ea26-109">This method copies the key to the collection, so you can release the local variable after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea26-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ea26-110">Return value</span></span>

<span data-ttu-id="8ea26-111">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8ea26-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8ea26-112">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8ea26-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8ea26-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8ea26-113">Return code</span></span>                                                                                   | <span data-ttu-id="8ea26-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ea26-114">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ea26-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ea26-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8ea26-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8ea26-116">The method succeeded.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="8ea26-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8ea26-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8ea26-118">Não há memória suficiente disponível para adicionar a chave à coleção.</span><span class="sxs-lookup"><span data-stu-id="8ea26-118">There is not enough memory available to add the key to the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="8ea26-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ea26-119">Examples</span></span>

<span data-ttu-id="8ea26-120">Para obter um exemplo de como usar esse método, consulte [Recuperando propriedades de um único objeto](retrieving-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="8ea26-120">For an example of how to use this method, see [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea26-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ea26-121">Requirements</span></span>



| <span data-ttu-id="8ea26-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea26-122">Requirement</span></span> | <span data-ttu-id="8ea26-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8ea26-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea26-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ea26-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8ea26-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ea26-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ea26-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ea26-126">Library</span></span><br/> | <dl> <span data-ttu-id="8ea26-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ea26-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea26-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ea26-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea26-129">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="8ea26-129">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="8ea26-130">Recuperando propriedades de conteúdo-objeto</span><span class="sxs-lookup"><span data-stu-id="8ea26-130">Retrieving Content-Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="8ea26-131">Recuperando propriedades de um único objeto</span><span class="sxs-lookup"><span data-stu-id="8ea26-131">Retrieving Properties for a Single Object</span></span>](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="8ea26-132">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ea26-132">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




