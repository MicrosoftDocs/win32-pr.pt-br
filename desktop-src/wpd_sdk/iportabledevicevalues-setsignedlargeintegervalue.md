---
description: O método SetSignedLargeIntegerValue adiciona um novo valor LONGLONG (tipo VT \_ i8) ou substitui um existente.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'Método IPortableDeviceValues:: SetSignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793272"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a><span data-ttu-id="f7e54-103">Método IPortableDeviceValues:: SetSignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="f7e54-103">IPortableDeviceValues::SetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="f7e54-104">O método **SetSignedLargeIntegerValue** adiciona um novo valor **LONGLONG** (tipo VT \_ i8) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="f7e54-104">The **SetSignedLargeIntegerValue** method adds a new **LONGLONG** value (type VT\_I8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7e54-105">Syntax</span></span>


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a><span data-ttu-id="f7e54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7e54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e54-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7e54-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7e54-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="f7e54-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f7e54-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f7e54-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7e54-110">Um **LONGLONG** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="f7e54-110">A **LONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7e54-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7e54-111">Return value</span></span>

<span data-ttu-id="f7e54-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f7e54-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f7e54-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7e54-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f7e54-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f7e54-114">Return code</span></span>                                                                          | <span data-ttu-id="f7e54-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7e54-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f7e54-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f7e54-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f7e54-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f7e54-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7e54-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7e54-118">Remarks</span></span>

<span data-ttu-id="f7e54-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="f7e54-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e54-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7e54-120">Requirements</span></span>



| <span data-ttu-id="f7e54-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7e54-121">Requirement</span></span> | <span data-ttu-id="f7e54-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f7e54-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e54-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7e54-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f7e54-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7e54-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7e54-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7e54-125">Library</span></span><br/> | <dl> <span data-ttu-id="f7e54-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7e54-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e54-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7e54-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e54-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f7e54-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f7e54-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="f7e54-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




