---
description: O método SetIPortableDevicePropVariantCollectionValue adiciona um novo valor IPortableDevicePropVariantCollection (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: 8ea6be5e-1d03-4d59-9acc-5cd56ee81cd3
title: 'Método IPortableDeviceValues:: SetIPortableDevicePropVariantCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f39ad6745dbf30df87e87be7fba358b4d9ad2c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814124"
---
# <a name="iportabledevicevaluessetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="a4b56-103">Método IPortableDeviceValues:: SetIPortableDevicePropVariantCollectionValue</span><span class="sxs-lookup"><span data-stu-id="a4b56-103">IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="a4b56-104">O método **SetIPortableDevicePropVariantCollectionValue** adiciona um novo valor **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (tipo VT \_ desconhecido) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="a4b56-104">The **SetIPortableDevicePropVariantCollectionValue** method adds a new **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b56-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4b56-105">Syntax</span></span>


```C++
HRESULT SetIPortableDevicePropVariantCollectionValue(
  [in] REFPROPERTYKEY                       key,
  [in] IPortableDevicePropVariantCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="a4b56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4b56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b56-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4b56-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b56-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="a4b56-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="a4b56-109">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4b56-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b56-110">Ponteiro para uma interface **IPortableDevicePropVariantCollection** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="a4b56-110">Pointer to an **IPortableDevicePropVariantCollection** interface that specifies the new value.</span></span> <span data-ttu-id="a4b56-111">O SDK copia uma referência para a interface enviada e chama **AddRef** nela.</span><span class="sxs-lookup"><span data-stu-id="a4b56-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b56-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4b56-112">Return value</span></span>

<span data-ttu-id="a4b56-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a4b56-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a4b56-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4b56-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a4b56-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a4b56-115">Return code</span></span>                                                                          | <span data-ttu-id="a4b56-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4b56-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a4b56-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b56-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a4b56-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a4b56-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4b56-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4b56-119">Remarks</span></span>

<span data-ttu-id="a4b56-120">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="a4b56-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="a4b56-121">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="a4b56-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b56-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b56-122">Requirements</span></span>



| <span data-ttu-id="a4b56-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b56-123">Requirement</span></span> | <span data-ttu-id="a4b56-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a4b56-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b56-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4b56-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a4b56-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b56-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4b56-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4b56-127">Library</span></span><br/> | <dl> <span data-ttu-id="a4b56-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4b56-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b56-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4b56-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b56-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a4b56-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a4b56-131">**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="a4b56-131">**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




