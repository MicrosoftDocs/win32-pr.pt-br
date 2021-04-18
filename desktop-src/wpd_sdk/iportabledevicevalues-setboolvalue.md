---
description: O método SetBoolValue adiciona um novo valor booliano (tipo VT \_ bool) ou substitui um existente.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: 'Método IPortableDeviceValues:: SetBoolValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7adf311e863c08873aa8300f9e940d4a5b49417f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780402"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a><span data-ttu-id="91337-103">Método IPortableDeviceValues:: SetBoolValue</span><span class="sxs-lookup"><span data-stu-id="91337-103">IPortableDeviceValues::SetBoolValue method</span></span>

<span data-ttu-id="91337-104">O método **SetBoolValue** adiciona um novo valor **booliano** (tipo VT \_ bool) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="91337-104">The **SetBoolValue** method adds a new **Boolean** value (type VT\_BOOL) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="91337-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91337-105">Syntax</span></span>


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
);
```



## <a name="parameters"></a><span data-ttu-id="91337-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91337-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91337-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91337-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91337-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="91337-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="91337-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="91337-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91337-110">Um **bool** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="91337-110">A **BOOL** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91337-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91337-111">Return value</span></span>

<span data-ttu-id="91337-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="91337-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="91337-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="91337-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="91337-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="91337-114">Return code</span></span>                                                                          | <span data-ttu-id="91337-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="91337-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="91337-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91337-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="91337-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="91337-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91337-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="91337-118">Remarks</span></span>

<span data-ttu-id="91337-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="91337-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="91337-120">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="91337-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="91337-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91337-121">Requirements</span></span>



| <span data-ttu-id="91337-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="91337-122">Requirement</span></span> | <span data-ttu-id="91337-123">Valor</span><span class="sxs-lookup"><span data-stu-id="91337-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91337-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91337-124">Header</span></span><br/>  | <dl> <span data-ttu-id="91337-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="91337-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="91337-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91337-126">Library</span></span><br/> | <dl> <span data-ttu-id="91337-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91337-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91337-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="91337-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91337-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="91337-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="91337-130">**IPortableDeviceValues:: getboolvalue**</span><span class="sxs-lookup"><span data-stu-id="91337-130">**IPortableDeviceValues::GetBoolValue**</span></span>](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




