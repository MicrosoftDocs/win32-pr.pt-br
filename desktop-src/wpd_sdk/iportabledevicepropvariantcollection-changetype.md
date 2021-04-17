---
description: O método Altertype converte todos os itens da coleção no VARTYPE especificado.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'Método IPortableDevicePropVariantCollection:: ChangeType (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797916"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a><span data-ttu-id="14c1f-103">Método IPortableDevicePropVariantCollection:: ChangeType</span><span class="sxs-lookup"><span data-stu-id="14c1f-103">IPortableDevicePropVariantCollection::ChangeType method</span></span>

<span data-ttu-id="14c1f-104">O método **altertype** converte todos os itens da coleção no VarType especificado.</span><span class="sxs-lookup"><span data-stu-id="14c1f-104">The **ChangeType** method converts all items in the collection to the specified VARTYPE.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14c1f-105">Syntax</span></span>


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a><span data-ttu-id="14c1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14c1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c1f-107">*VT* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c1f-107">*vt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c1f-108">Especifica o **VarType** para o qual você deseja converter todos os itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="14c1f-108">Specifies the **VARTYPE** to which you want to convert all items in the collection.</span></span> <span data-ttu-id="14c1f-109">Os tipos de exemplo incluem VT \_ UI4 e VT \_ UI8.</span><span class="sxs-lookup"><span data-stu-id="14c1f-109">Example types include VT\_UI4 and VT\_UI8.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c1f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14c1f-110">Return value</span></span>

<span data-ttu-id="14c1f-111">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="14c1f-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="14c1f-112">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="14c1f-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="14c1f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="14c1f-113">Return code</span></span>                                                                          | <span data-ttu-id="14c1f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="14c1f-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="14c1f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14c1f-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="14c1f-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="14c1f-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14c1f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="14c1f-117">Remarks</span></span>

<span data-ttu-id="14c1f-118">Se esse método falhar, a coleção poderá ser deixada em um estado intermediário, com alguns membros convertidos e alguns não convertidos.</span><span class="sxs-lookup"><span data-stu-id="14c1f-118">If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c1f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14c1f-119">Requirements</span></span>



| <span data-ttu-id="14c1f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c1f-120">Requirement</span></span> | <span data-ttu-id="14c1f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="14c1f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c1f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14c1f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="14c1f-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c1f-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="14c1f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14c1f-124">Library</span></span><br/> | <dl> <span data-ttu-id="14c1f-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c1f-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c1f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="14c1f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c1f-127">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="14c1f-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




