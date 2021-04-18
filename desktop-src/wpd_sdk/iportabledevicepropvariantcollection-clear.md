---
description: O método Clear libera e, em seguida, remove todos os itens da coleção. A coleção é considerada vazia depois de chamar esse método.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'Método IPortableDevicePropVariantCollection:: Clear (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765131"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a><span data-ttu-id="588fa-104">Método IPortableDevicePropVariantCollection:: Clear</span><span class="sxs-lookup"><span data-stu-id="588fa-104">IPortableDevicePropVariantCollection::Clear method</span></span>

<span data-ttu-id="588fa-105">O método **Clear** libera e, em seguida, remove todos os itens da coleção.</span><span class="sxs-lookup"><span data-stu-id="588fa-105">The **Clear** method frees, and then removes, all items from the collection.</span></span> <span data-ttu-id="588fa-106">A coleção é considerada vazia depois de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="588fa-106">The collection is considered empty after calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="588fa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="588fa-107">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="588fa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="588fa-108">Parameters</span></span>

<span data-ttu-id="588fa-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="588fa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="588fa-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="588fa-110">Return value</span></span>

<span data-ttu-id="588fa-111">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="588fa-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="588fa-112">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="588fa-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="588fa-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="588fa-113">Return code</span></span>                                                                          | <span data-ttu-id="588fa-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="588fa-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="588fa-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="588fa-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="588fa-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="588fa-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="588fa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="588fa-117">Remarks</span></span>

<span data-ttu-id="588fa-118">Depois de chamar **Clear**, a coleção é considerada sem tipo, o que significa que o VarType definido anteriormente não está mais restringindo as operações de **adição** .</span><span class="sxs-lookup"><span data-stu-id="588fa-118">After calling **Clear**, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting **Add** operations.</span></span> <span data-ttu-id="588fa-119">Uma chamada para **Add** depois de chamar **Clear** é considerada a "primeiro" **Adicionar** para essa coleção.</span><span class="sxs-lookup"><span data-stu-id="588fa-119">A call to **Add** after calling **Clear** is considered the "first" **Add** for this collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="588fa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="588fa-120">Requirements</span></span>



| <span data-ttu-id="588fa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="588fa-121">Requirement</span></span> | <span data-ttu-id="588fa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="588fa-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="588fa-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="588fa-123">Header</span></span><br/>  | <dl> <span data-ttu-id="588fa-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="588fa-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="588fa-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="588fa-125">Library</span></span><br/> | <dl> <span data-ttu-id="588fa-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="588fa-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="588fa-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="588fa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588fa-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="588fa-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




