---
description: O método SetUnsignedLargeIntegerValue adiciona um novo valor ULONGLONG (tipo VT \_ UI8) ou substitui um existente.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'Método IPortableDeviceValues:: SetUnsignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813674"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a><span data-ttu-id="f95f6-103">Método IPortableDeviceValues:: SetUnsignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="f95f6-103">IPortableDeviceValues::SetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="f95f6-104">O método **SetUnsignedLargeIntegerValue** adiciona um novo valor **ULONGLONG** (tipo VT \_ UI8) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="f95f6-104">The **SetUnsignedLargeIntegerValue** method adds a new **ULONGLONG** value (type VT\_UI8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f95f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f95f6-105">Syntax</span></span>


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a><span data-ttu-id="f95f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f95f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f95f6-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f95f6-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f95f6-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="f95f6-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f95f6-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f95f6-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f95f6-110">Um **ULONGLONG** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="f95f6-110">A **ULONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f95f6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f95f6-111">Return value</span></span>

<span data-ttu-id="f95f6-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f95f6-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f95f6-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f95f6-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f95f6-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f95f6-114">Return code</span></span>                                                                          | <span data-ttu-id="f95f6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f95f6-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f95f6-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f95f6-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f95f6-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f95f6-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f95f6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f95f6-118">Requirements</span></span>



| <span data-ttu-id="f95f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f95f6-119">Requirement</span></span> | <span data-ttu-id="f95f6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f95f6-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f95f6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f95f6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f95f6-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f95f6-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f95f6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f95f6-123">Library</span></span><br/> | <dl> <span data-ttu-id="f95f6-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f95f6-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f95f6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f95f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95f6-126">Adicionando um recurso a um objeto</span><span class="sxs-lookup"><span data-stu-id="f95f6-126">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="f95f6-127">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f95f6-127">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f95f6-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="f95f6-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




