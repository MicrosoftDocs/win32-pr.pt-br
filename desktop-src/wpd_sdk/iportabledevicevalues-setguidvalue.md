---
description: O método setguidvalue adiciona um novo valor de GUID (tipo VT \_ CLSID) ou substitui um existente.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'Método IPortableDeviceValues:: setguidvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791532"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a><span data-ttu-id="de83f-103">Método IPortableDeviceValues:: setguidvalue</span><span class="sxs-lookup"><span data-stu-id="de83f-103">IPortableDeviceValues::SetGuidValue method</span></span>

<span data-ttu-id="de83f-104">O método **Setguidvalue** adiciona um novo valor de **GUID** (tipo VT \_ CLSID) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="de83f-104">The **SetGuidValue** method adds a new **GUID** value (type VT\_CLSID) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="de83f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de83f-105">Syntax</span></span>


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a><span data-ttu-id="de83f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de83f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de83f-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de83f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de83f-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="de83f-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="de83f-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="de83f-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de83f-110">Um **REFGUID** que contém o novo valor.</span><span class="sxs-lookup"><span data-stu-id="de83f-110">A **REFGUID** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de83f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de83f-111">Return value</span></span>

<span data-ttu-id="de83f-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="de83f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="de83f-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="de83f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="de83f-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="de83f-114">Return code</span></span>                                                                          | <span data-ttu-id="de83f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="de83f-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="de83f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de83f-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="de83f-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="de83f-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de83f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="de83f-118">Remarks</span></span>

<span data-ttu-id="de83f-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="de83f-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="de83f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de83f-120">Requirements</span></span>



| <span data-ttu-id="de83f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="de83f-121">Requirement</span></span> | <span data-ttu-id="de83f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="de83f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de83f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de83f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="de83f-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="de83f-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="de83f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de83f-125">Library</span></span><br/> | <dl> <span data-ttu-id="de83f-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de83f-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de83f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="de83f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de83f-128">Adicionando um recurso a um objeto</span><span class="sxs-lookup"><span data-stu-id="de83f-128">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="de83f-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="de83f-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="de83f-130">**IPortableDeviceValues:: getguidvalue**</span><span class="sxs-lookup"><span data-stu-id="de83f-130">**IPortableDeviceValues::GetGuidValue**</span></span>](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




