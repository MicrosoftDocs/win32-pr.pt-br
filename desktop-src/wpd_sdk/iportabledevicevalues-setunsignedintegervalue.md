---
description: O método SetUnsignedIntegerValue adiciona um novo valor ULONG (tipo VT \_ UI4) ou substitui um existente.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'Método IPortableDeviceValues:: SetUnsignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771544"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a><span data-ttu-id="f561b-103">Método IPortableDeviceValues:: SetUnsignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="f561b-103">IPortableDeviceValues::SetUnsignedIntegerValue method</span></span>

<span data-ttu-id="f561b-104">O método **SetUnsignedIntegerValue** adiciona um novo valor **ULONG** (tipo VT \_ UI4) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="f561b-104">The **SetUnsignedIntegerValue** method adds a new **ULONG** value (type VT\_UI4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f561b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f561b-105">Syntax</span></span>


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a><span data-ttu-id="f561b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f561b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f561b-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f561b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f561b-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="f561b-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f561b-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f561b-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f561b-110">Um **ULONG** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="f561b-110">A **ULONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f561b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f561b-111">Return value</span></span>

<span data-ttu-id="f561b-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f561b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f561b-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f561b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f561b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f561b-114">Return code</span></span>                                                                          | <span data-ttu-id="f561b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f561b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f561b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f561b-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f561b-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f561b-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f561b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f561b-118">Remarks</span></span>

<span data-ttu-id="f561b-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="f561b-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="examples"></a><span data-ttu-id="f561b-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f561b-120">Examples</span></span>

<span data-ttu-id="f561b-121">Para obter um exemplo de como usar esse método, consulte [**especificando informações do cliente**](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="f561b-121">For an example of how to use this method, see [**Specifying Client Information**](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f561b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f561b-122">Requirements</span></span>



| <span data-ttu-id="f561b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f561b-123">Requirement</span></span> | <span data-ttu-id="f561b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f561b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f561b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f561b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f561b-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f561b-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f561b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f561b-127">Library</span></span><br/> | <dl> <span data-ttu-id="f561b-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f561b-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f561b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f561b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f561b-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f561b-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f561b-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="f561b-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span></span>](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="f561b-132">**Especificando informações do cliente**</span><span class="sxs-lookup"><span data-stu-id="f561b-132">**Specifying Client Information**</span></span>](specifying-client-information.md)
</dt> </dl>

 

 




