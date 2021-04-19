---
description: O método setiunknownvalue adiciona um novo valor IUnknown (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'Método IPortableDeviceValues:: setiunknownvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2c3a27fe5ea89359884d70162000b5164b7c1aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784671"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a><span data-ttu-id="bc06a-103">Método IPortableDeviceValues:: setiunknownvalue</span><span class="sxs-lookup"><span data-stu-id="bc06a-103">IPortableDeviceValues::SetIUnknownValue method</span></span>

<span data-ttu-id="bc06a-104">O método **Setiunknownvalue** adiciona um novo valor **IUnknown** (tipo VT \_ desconhecido) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="bc06a-104">The **SetIUnknownValue** method adds a new **IUnknown** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc06a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc06a-105">Syntax</span></span>


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="bc06a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc06a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc06a-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc06a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc06a-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="bc06a-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="bc06a-109">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc06a-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc06a-110">Um ponteiro para uma interface **IUnknown** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="bc06a-110">A pointer to an **IUnknown** interface that specifies the new value.</span></span> <span data-ttu-id="bc06a-111">O SDK copia uma referência para a interface enviada e chama **AddRef** nela.</span><span class="sxs-lookup"><span data-stu-id="bc06a-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc06a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc06a-112">Return value</span></span>

<span data-ttu-id="bc06a-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bc06a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bc06a-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bc06a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bc06a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bc06a-115">Return code</span></span>                                                                          | <span data-ttu-id="bc06a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc06a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bc06a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bc06a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bc06a-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bc06a-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc06a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc06a-119">Remarks</span></span>

<span data-ttu-id="bc06a-120">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="bc06a-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="bc06a-121">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="bc06a-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc06a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc06a-122">Requirements</span></span>



| <span data-ttu-id="bc06a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc06a-123">Requirement</span></span> | <span data-ttu-id="bc06a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bc06a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc06a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc06a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bc06a-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc06a-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc06a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc06a-127">Library</span></span><br/> | <dl> <span data-ttu-id="bc06a-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc06a-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc06a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc06a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc06a-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="bc06a-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="bc06a-131">**IPortableDeviceValues:: getiunknownvalue**</span><span class="sxs-lookup"><span data-stu-id="bc06a-131">**IPortableDeviceValues::GetIUnknownValue**</span></span>](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




