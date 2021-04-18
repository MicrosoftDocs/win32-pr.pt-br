---
description: O método SetKeyValue adiciona um novo valor REFPROPERTYKEY (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'Método IPortableDeviceValues:: SetKeyValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793310"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a><span data-ttu-id="66b31-103">Método IPortableDeviceValues:: SetKeyValue</span><span class="sxs-lookup"><span data-stu-id="66b31-103">IPortableDeviceValues::SetKeyValue method</span></span>

<span data-ttu-id="66b31-104">O método **SetKeyValue** adiciona um novo valor **REFPROPERTYKEY** (tipo VT \_ desconhecido) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="66b31-104">The **SetKeyValue** method adds a new **REFPROPERTYKEY** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b31-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66b31-105">Syntax</span></span>


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a><span data-ttu-id="66b31-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66b31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b31-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66b31-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66b31-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="66b31-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="66b31-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="66b31-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66b31-110">Um **REFPROPERTYKEY** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="66b31-110">A **REFPROPERTYKEY** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b31-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66b31-111">Return value</span></span>

<span data-ttu-id="66b31-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66b31-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66b31-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="66b31-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66b31-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="66b31-114">Return code</span></span>                                                                          | <span data-ttu-id="66b31-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="66b31-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="66b31-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66b31-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="66b31-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="66b31-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66b31-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="66b31-118">Remarks</span></span>

<span data-ttu-id="66b31-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="66b31-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="66b31-120">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="66b31-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b31-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66b31-121">Requirements</span></span>



| <span data-ttu-id="66b31-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b31-122">Requirement</span></span> | <span data-ttu-id="66b31-123">Valor</span><span class="sxs-lookup"><span data-stu-id="66b31-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66b31-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66b31-124">Header</span></span><br/>  | <dl> <span data-ttu-id="66b31-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b31-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="66b31-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66b31-126">Library</span></span><br/> | <dl> <span data-ttu-id="66b31-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66b31-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b31-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="66b31-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b31-129">Adicionando um recurso a um objeto</span><span class="sxs-lookup"><span data-stu-id="66b31-129">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="66b31-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="66b31-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="66b31-131">**IPortableDeviceValues::GetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="66b31-131">**IPortableDeviceValues::GetKeyValue**</span></span>](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




