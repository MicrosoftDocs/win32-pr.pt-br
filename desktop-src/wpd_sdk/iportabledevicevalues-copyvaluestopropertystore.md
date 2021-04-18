---
description: O método CopyValuesToPropertyStore copia todos os valores de uma coleção para uma interface IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Método IPortableDeviceValues:: CopyValuesToPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797958"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a><span data-ttu-id="d7f62-103">Método IPortableDeviceValues:: CopyValuesToPropertyStore</span><span class="sxs-lookup"><span data-stu-id="d7f62-103">IPortableDeviceValues::CopyValuesToPropertyStore method</span></span>

<span data-ttu-id="d7f62-104">O método **CopyValuesToPropertyStore** copia todos os valores de uma coleção para uma interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="d7f62-104">The **CopyValuesToPropertyStore** method copies all the values from a collection into an **IPropertyStore** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f62-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7f62-105">Syntax</span></span>


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="d7f62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7f62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f62-107">*Pstore* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7f62-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f62-108">Ponteiro para um objeto de repositório.</span><span class="sxs-lookup"><span data-stu-id="d7f62-108">Pointer to a store object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f62-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7f62-109">Return value</span></span>

<span data-ttu-id="d7f62-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d7f62-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d7f62-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7f62-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d7f62-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d7f62-112">Return code</span></span>                                                                          | <span data-ttu-id="d7f62-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7f62-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d7f62-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f62-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d7f62-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d7f62-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7f62-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7f62-116">Remarks</span></span>

<span data-ttu-id="d7f62-117">Este método não converte valores de VT \_ LPWSTR em VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="d7f62-117">This method does not convert values of VT\_LPWSTR into VT\_BSTR.</span></span> <span data-ttu-id="d7f62-118">Muitos aplicativos externos ou componentes que se comunicam com seu aplicativo, como alguns aplicativos de Shell, usam a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="d7f62-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="d7f62-119">Esse método fornece uma maneira rápida e fácil de trocar dados com esses programas.</span><span class="sxs-lookup"><span data-stu-id="d7f62-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="d7f62-120">Esse método tem suporte no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="d7f62-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f62-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f62-121">Requirements</span></span>



| <span data-ttu-id="d7f62-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f62-122">Requirement</span></span> | <span data-ttu-id="d7f62-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f62-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f62-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7f62-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d7f62-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f62-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7f62-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7f62-126">Library</span></span><br/> | <dl> <span data-ttu-id="d7f62-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7f62-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f62-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7f62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f62-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d7f62-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d7f62-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="d7f62-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span></span>](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




