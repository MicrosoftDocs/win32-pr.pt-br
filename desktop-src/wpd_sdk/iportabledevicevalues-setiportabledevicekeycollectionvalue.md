---
description: O método SetIPortableDeviceKeyCollectionValue adiciona um novo valor SetIPortableDeviceKeyCollectionValue (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'Método IPortableDeviceValues:: SetIPortableDeviceKeyCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786251"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="b49c9-103">Método IPortableDeviceValues:: SetIPortableDeviceKeyCollectionValue</span><span class="sxs-lookup"><span data-stu-id="b49c9-103">IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="b49c9-104">O método **SetIPortableDeviceKeyCollectionValue** adiciona um novo valor **SETIPORTABLEDEVICEKEYCOLLECTIONVALUE** (tipo VT \_ desconhecido) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="b49c9-104">The **SetIPortableDeviceKeyCollectionValue** method adds a new **SetIPortableDeviceKeyCollectionValue** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b49c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b49c9-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b49c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b49c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b49c9-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b49c9-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49c9-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="b49c9-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="b49c9-109">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b49c9-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49c9-110">Ponteiro para uma interface **IPortableDeviceKeyCollection** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="b49c9-110">Pointer to an **IPortableDeviceKeyCollection** interface that specifies the new value.</span></span> <span data-ttu-id="b49c9-111">O SDK copia uma referência para a interface enviada e chama **AddRef** nela.</span><span class="sxs-lookup"><span data-stu-id="b49c9-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b49c9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b49c9-112">Return value</span></span>

<span data-ttu-id="b49c9-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b49c9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b49c9-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b49c9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b49c9-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b49c9-115">Return code</span></span>                                                                          | <span data-ttu-id="b49c9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b49c9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b49c9-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b49c9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b49c9-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b49c9-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b49c9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b49c9-119">Remarks</span></span>

<span data-ttu-id="b49c9-120">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="b49c9-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="b49c9-121">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="b49c9-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49c9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b49c9-122">Requirements</span></span>



| <span data-ttu-id="b49c9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b49c9-123">Requirement</span></span> | <span data-ttu-id="b49c9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b49c9-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49c9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b49c9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b49c9-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b49c9-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b49c9-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b49c9-127">Library</span></span><br/> | <dl> <span data-ttu-id="b49c9-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b49c9-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49c9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b49c9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49c9-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b49c9-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b49c9-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="b49c9-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




