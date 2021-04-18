---
description: O método SetValue adiciona um novo valor PROPVARIANT ou substitui um existente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'Método IPortableDeviceValues:: SetValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811028"
---
# <a name="iportabledevicevaluessetvalue-method"></a><span data-ttu-id="dea1f-103">Método IPortableDeviceValues:: SetValue</span><span class="sxs-lookup"><span data-stu-id="dea1f-103">IPortableDeviceValues::SetValue method</span></span>

<span data-ttu-id="dea1f-104">O método **SetValue** adiciona um novo valor **PROPVARIANT** ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="dea1f-104">The **SetValue** method adds a new **PROPVARIANT** value or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dea1f-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="dea1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dea1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea1f-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dea1f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea1f-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="dea1f-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="dea1f-109">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dea1f-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea1f-110">Um **PROPVARIANT** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="dea1f-110">A **PROPVARIANT** that specifies the new value.</span></span> <span data-ttu-id="dea1f-111">O SDK copia o valor para que o chamador possa liberar a variável local chamando **PropVariantClear** depois de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="dea1f-111">The SDK copies the value, so the caller can release the local variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea1f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dea1f-112">Return value</span></span>

<span data-ttu-id="dea1f-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dea1f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dea1f-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dea1f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dea1f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dea1f-115">Return code</span></span>                                                                          | <span data-ttu-id="dea1f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="dea1f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dea1f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dea1f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dea1f-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dea1f-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dea1f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="dea1f-119">Remarks</span></span>

<span data-ttu-id="dea1f-120">Quando o VARTYPE de  zero é VT \_ vector ou VT \_ UI1, não há suporte para definir um buffer **nulo** ou de tamanho zero.</span><span class="sxs-lookup"><span data-stu-id="dea1f-120">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="dea1f-121">Por exemplo, não há um zero. caub. pElems = **NULL** nem 1. caub. cElems = 0 são permitidos.</span><span class="sxs-lookup"><span data-stu-id="dea1f-121">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="dea1f-122">Esse método pode ser usado para recuperar um valor de qualquer tipo da coleção.</span><span class="sxs-lookup"><span data-stu-id="dea1f-122">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="dea1f-123">No entanto, se você souber o tipo de valor com antecedência, use um dos métodos **set...** especializados dessa interface para evitar a sobrecarga de trabalhar com valores de PROPVARIANT diretamente.</span><span class="sxs-lookup"><span data-stu-id="dea1f-123">However, if you know the value type in advance, use one of the specialized **Set...** methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

<span data-ttu-id="dea1f-124">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="dea1f-124">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="dea1f-125">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="dea1f-125">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea1f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea1f-126">Requirements</span></span>



| <span data-ttu-id="dea1f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea1f-127">Requirement</span></span> | <span data-ttu-id="dea1f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dea1f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea1f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dea1f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dea1f-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea1f-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="dea1f-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dea1f-131">Library</span></span><br/> | <dl> <span data-ttu-id="dea1f-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dea1f-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea1f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="dea1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea1f-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="dea1f-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="dea1f-135">**IPortableDeviceValues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="dea1f-135">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="dea1f-136">**IPortableDeviceValues:: RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="dea1f-136">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




