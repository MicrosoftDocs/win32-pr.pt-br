---
description: O método CopyValuesFromPropertyStore copia o conteúdo de um IPropertyStore na coleção.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'Método IPortableDeviceValues:: CopyValuesFromPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791272"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a><span data-ttu-id="22ffd-103">Método IPortableDeviceValues:: CopyValuesFromPropertyStore</span><span class="sxs-lookup"><span data-stu-id="22ffd-103">IPortableDeviceValues::CopyValuesFromPropertyStore method</span></span>

<span data-ttu-id="22ffd-104">O método **CopyValuesFromPropertyStore** copia o conteúdo de um **IPropertyStore** na coleção.</span><span class="sxs-lookup"><span data-stu-id="22ffd-104">The **CopyValuesFromPropertyStore** method copies the contents of an **IPropertyStore** into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ffd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22ffd-105">Syntax</span></span>


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="22ffd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22ffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ffd-107">*Pstore* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="22ffd-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22ffd-108">Ponteiro para um **IPropertyStore** a ser copiado para a coleção.</span><span class="sxs-lookup"><span data-stu-id="22ffd-108">Pointer to an **IPropertyStore** to copy into the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ffd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22ffd-109">Return value</span></span>

<span data-ttu-id="22ffd-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22ffd-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22ffd-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="22ffd-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22ffd-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="22ffd-112">Return code</span></span>                                                                          | <span data-ttu-id="22ffd-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="22ffd-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="22ffd-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22ffd-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="22ffd-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="22ffd-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22ffd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="22ffd-116">Remarks</span></span>

<span data-ttu-id="22ffd-117">Esse método converte automaticamente todos os valores **VT \_ BSTR** em valores de **VT \_ LPWSTR** .</span><span class="sxs-lookup"><span data-stu-id="22ffd-117">This method automatically converts all **VT\_BSTR** values to **VT\_LPWSTR** values.</span></span>

<span data-ttu-id="22ffd-118">Muitos aplicativos externos ou componentes que se comunicam com seu aplicativo, como alguns aplicativos de Shell, usam a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="22ffd-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="22ffd-119">Esse método fornece uma maneira rápida e fácil de trocar dados com esses programas.</span><span class="sxs-lookup"><span data-stu-id="22ffd-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="22ffd-120">Esse método tem suporte no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="22ffd-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="22ffd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22ffd-121">Requirements</span></span>



| <span data-ttu-id="22ffd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ffd-122">Requirement</span></span> | <span data-ttu-id="22ffd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="22ffd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ffd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22ffd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="22ffd-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="22ffd-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="22ffd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22ffd-126">Library</span></span><br/> | <dl> <span data-ttu-id="22ffd-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22ffd-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ffd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="22ffd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ffd-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="22ffd-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="22ffd-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="22ffd-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span></span>](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




