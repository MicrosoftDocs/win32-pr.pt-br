---
description: 'Método IPortableDevicePropVariantCollection:: Add – o método add adiciona um item à coleção.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Método IPortableDevicePropVariantCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112454"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="dc23a-103">Método IPortableDevicePropVariantCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="dc23a-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="dc23a-104">O método **Add** adiciona um item à coleção.</span><span class="sxs-lookup"><span data-stu-id="dc23a-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc23a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc23a-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="dc23a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc23a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc23a-107">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dc23a-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc23a-108">Ponteiro para um novo objeto **PROPVARIANT** para adicionar à coleção.</span><span class="sxs-lookup"><span data-stu-id="dc23a-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="dc23a-109">Esse método copia o **PROPVARIANT** para a coleção, de modo que você deve liberar sua cópia local da variável chamando **PropVariantClear** depois de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="dc23a-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc23a-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dc23a-110">Return value</span></span>

<span data-ttu-id="dc23a-111">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dc23a-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dc23a-112">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc23a-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dc23a-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dc23a-113">Return code</span></span>                                                                          | <span data-ttu-id="dc23a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc23a-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dc23a-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc23a-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dc23a-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dc23a-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc23a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc23a-117">Remarks</span></span>

<span data-ttu-id="dc23a-118">Quando o VARTYPE de  zero é VT \_ vector ou VT \_ UI1, não há suporte para a configuração e a recuperação de um buffer de tamanho **nulo** ou zero.</span><span class="sxs-lookup"><span data-stu-id="dc23a-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="dc23a-119">Por exemplo, não há um zero. caub. pElems = **NULL** nem 1. caub. cElems = 0 são permitidos.</span><span class="sxs-lookup"><span data-stu-id="dc23a-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="dc23a-120">Se um chamador tentar adicionar um item de um VARTYPE diferente contido na coleção e o valor de PROPVARIANT não puder ser alterado por essa interface automaticamente, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="dc23a-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="dc23a-121">Para alterar o tipo de coleção manualmente, chame [**IPortableDevicePropVariantCollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="dc23a-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dc23a-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc23a-122">Examples</span></span>

<span data-ttu-id="dc23a-123">Para obter um exemplo de como usar esse método, consulte [recuperando um identificador de objeto de um identificador exclusivo persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span><span class="sxs-lookup"><span data-stu-id="dc23a-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="dc23a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc23a-124">Requirements</span></span>



| <span data-ttu-id="dc23a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc23a-125">Requirement</span></span> | <span data-ttu-id="dc23a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dc23a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc23a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc23a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="dc23a-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc23a-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc23a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc23a-129">Library</span></span><br/> | <dl> <span data-ttu-id="dc23a-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc23a-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc23a-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dc23a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc23a-132">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="dc23a-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="dc23a-133">Movendo o conteúdo no dispositivo</span><span class="sxs-lookup"><span data-stu-id="dc23a-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="dc23a-134">Recuperando um identificador de objeto de um identificador exclusivo persistente</span><span class="sxs-lookup"><span data-stu-id="dc23a-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




