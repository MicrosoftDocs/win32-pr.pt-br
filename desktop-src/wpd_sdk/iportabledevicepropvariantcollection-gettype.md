---
description: O método GetType recupera o tipo de dados dos itens na coleção.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Método IPortableDevicePropVariantCollection:: GetType (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759994"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a><span data-ttu-id="e60a3-103">Método IPortableDevicePropVariantCollection:: GetType</span><span class="sxs-lookup"><span data-stu-id="e60a3-103">IPortableDevicePropVariantCollection::GetType method</span></span>

<span data-ttu-id="e60a3-104">O método **GetType** recupera o tipo de dados dos itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="e60a3-104">The **GetType** method retrieves the data type of the items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e60a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e60a3-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a><span data-ttu-id="e60a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e60a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e60a3-107">*Pvt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e60a3-107">*pvt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e60a3-108">Um valor de enumeração do **VarType** do Platform SDK que indica o tipo de dados de todos os itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="e60a3-108">A Platform SDK **VARTYPE** enumeration value that indicates the data type of all the items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e60a3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e60a3-109">Return value</span></span>

<span data-ttu-id="e60a3-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e60a3-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e60a3-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e60a3-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e60a3-112">Return code</span></span>                                                                               | <span data-ttu-id="e60a3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e60a3-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="e60a3-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e60a3-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e60a3-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e60a3-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="e60a3-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e60a3-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e60a3-117">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e60a3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e60a3-118">Remarks</span></span>

<span data-ttu-id="e60a3-119">Todos os itens que são armazenados em um **IPortableDevicePropVariantCollection** são do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="e60a3-119">All items that are stored in an **IPortableDevicePropVariantCollection** are the same type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e60a3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e60a3-120">Requirements</span></span>



| <span data-ttu-id="e60a3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e60a3-121">Requirement</span></span> | <span data-ttu-id="e60a3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e60a3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e60a3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e60a3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e60a3-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e60a3-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e60a3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e60a3-125">Library</span></span><br/> | <dl> <span data-ttu-id="e60a3-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e60a3-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e60a3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e60a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60a3-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="e60a3-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




