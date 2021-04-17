---
description: O método setfloatvalue adiciona um novo valor FLOAT (tipo VT \_ R4) ou substitui um existente.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'Método IPortableDeviceValues:: setfloatvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 60b42217c925c83e96f2c893c7bc7f11449ebdd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797962"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a><span data-ttu-id="ff78c-103">Método IPortableDeviceValues:: setfloatvalue</span><span class="sxs-lookup"><span data-stu-id="ff78c-103">IPortableDeviceValues::SetFloatValue method</span></span>

<span data-ttu-id="ff78c-104">O método **Setfloatvalue** adiciona um novo valor **float** (tipo VT \_ R4) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="ff78c-104">The **SetFloatValue** method adds a new **FLOAT** value (type VT\_R4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff78c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff78c-105">Syntax</span></span>


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
);
```



## <a name="parameters"></a><span data-ttu-id="ff78c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff78c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff78c-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff78c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff78c-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="ff78c-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ff78c-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ff78c-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff78c-110">Um **float** que contém o novo valor.</span><span class="sxs-lookup"><span data-stu-id="ff78c-110">A **FLOAT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff78c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff78c-111">Return value</span></span>

<span data-ttu-id="ff78c-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ff78c-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ff78c-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff78c-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ff78c-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ff78c-114">Return code</span></span>                                                                          | <span data-ttu-id="ff78c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff78c-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ff78c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff78c-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ff78c-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ff78c-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ff78c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff78c-118">Remarks</span></span>

<span data-ttu-id="ff78c-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="ff78c-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff78c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff78c-120">Requirements</span></span>



| <span data-ttu-id="ff78c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff78c-121">Requirement</span></span> | <span data-ttu-id="ff78c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ff78c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff78c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff78c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ff78c-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff78c-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff78c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff78c-125">Library</span></span><br/> | <dl> <span data-ttu-id="ff78c-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff78c-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff78c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff78c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff78c-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ff78c-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ff78c-129">**IPortableDeviceValues:: getfloatvalue**</span><span class="sxs-lookup"><span data-stu-id="ff78c-129">**IPortableDeviceValues::GetFloatValue**</span></span>](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




