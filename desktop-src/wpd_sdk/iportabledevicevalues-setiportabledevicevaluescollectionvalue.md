---
description: O método SetIPortableDeviceValuesCollectionValue adiciona um novo valor IPortableDeviceValuesCollection (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: 'Método IPortableDeviceValues:: SetIPortableDeviceValuesCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3f0c545a4daceed75971b0e659f85d72eca6d98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760682"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="e474c-103">Método IPortableDeviceValues:: SetIPortableDeviceValuesCollectionValue</span><span class="sxs-lookup"><span data-stu-id="e474c-103">IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="e474c-104">O método **SetIPortableDeviceValuesCollectionValue** adiciona um novo valor **IPORTABLEDEVICEVALUESCOLLECTION** (tipo VT \_ desconhecido) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="e474c-104">The **SetIPortableDeviceValuesCollectionValue** method adds a new **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e474c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e474c-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e474c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e474c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e474c-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e474c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e474c-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="e474c-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="e474c-109">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e474c-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e474c-110">Ponteiro para uma interface **IPortableDeviceValuesCollection** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="e474c-110">Pointer to an **IPortableDeviceValuesCollection** interface that specifies the new value.</span></span> <span data-ttu-id="e474c-111">O SDK copia uma referência para a interface enviada e chama **AddRef** nela.</span><span class="sxs-lookup"><span data-stu-id="e474c-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e474c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e474c-112">Return value</span></span>

<span data-ttu-id="e474c-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e474c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e474c-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e474c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e474c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e474c-115">Return code</span></span>                                                                          | <span data-ttu-id="e474c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e474c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e474c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e474c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e474c-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e474c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e474c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e474c-119">Remarks</span></span>

<span data-ttu-id="e474c-120">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="e474c-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="e474c-121">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="e474c-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="e474c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e474c-122">Requirements</span></span>



| <span data-ttu-id="e474c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e474c-123">Requirement</span></span> | <span data-ttu-id="e474c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e474c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e474c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e474c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e474c-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e474c-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e474c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e474c-127">Library</span></span><br/> | <dl> <span data-ttu-id="e474c-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e474c-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e474c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e474c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e474c-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e474c-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e474c-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="e474c-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




