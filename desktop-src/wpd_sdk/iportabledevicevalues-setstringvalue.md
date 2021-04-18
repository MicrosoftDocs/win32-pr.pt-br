---
description: O método SetStringValue adiciona um novo valor de cadeia de caracteres (tipo VT \_ LPWSTR) ou substitui um existente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'Método IPortableDeviceValues:: SetStringValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814085"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a><span data-ttu-id="52a89-103">Método IPortableDeviceValues:: SetStringValue</span><span class="sxs-lookup"><span data-stu-id="52a89-103">IPortableDeviceValues::SetStringValue method</span></span>

<span data-ttu-id="52a89-104">O método **SetStringValue** adiciona um novo valor de cadeia de caracteres (tipo VT \_ LPWSTR) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="52a89-104">The **SetStringValue** method adds a new string value (type VT\_LPWSTR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52a89-105">Syntax</span></span>


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a><span data-ttu-id="52a89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a89-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52a89-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52a89-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="52a89-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="52a89-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="52a89-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52a89-110">Um **LPCWSTR** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="52a89-110">A **LPCWSTR** that specifies the new value.</span></span> <span data-ttu-id="52a89-111">A cadeia de caracteres é copiada, portanto, o chamador pode liberar a memória alocada para esse valor depois de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="52a89-111">The string is copied, so the caller can release the memory allocated for this value after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a89-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52a89-112">Return value</span></span>

<span data-ttu-id="52a89-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="52a89-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="52a89-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="52a89-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="52a89-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="52a89-115">Return code</span></span>                                                                          | <span data-ttu-id="52a89-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="52a89-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="52a89-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="52a89-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="52a89-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="52a89-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52a89-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="52a89-119">Remarks</span></span>

<span data-ttu-id="52a89-120">Qualquer memória de chave existente será liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="52a89-120">Any existing key memory will be released appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="52a89-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52a89-121">Examples</span></span>

<span data-ttu-id="52a89-122">Para obter um exemplo de como usar esse método, consulte [especificando informações do cliente](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="52a89-122">For an example of how to use this method, see [Specifying Client Information](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52a89-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52a89-123">Requirements</span></span>



| <span data-ttu-id="52a89-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a89-124">Requirement</span></span> | <span data-ttu-id="52a89-125">Valor</span><span class="sxs-lookup"><span data-stu-id="52a89-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a89-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52a89-126">Header</span></span><br/>  | <dl> <span data-ttu-id="52a89-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a89-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="52a89-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52a89-128">Library</span></span><br/> | <dl> <span data-ttu-id="52a89-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52a89-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a89-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="52a89-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a89-131">Adicionando um recurso a um objeto</span><span class="sxs-lookup"><span data-stu-id="52a89-131">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="52a89-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="52a89-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="52a89-133">**IPortableDeviceValues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="52a89-133">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[<span data-ttu-id="52a89-134">Definindo propriedades para um único objeto</span><span class="sxs-lookup"><span data-stu-id="52a89-134">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="52a89-135">Definindo propriedades para vários objetos</span><span class="sxs-lookup"><span data-stu-id="52a89-135">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> <dt>

[<span data-ttu-id="52a89-136">Especificando informações do cliente</span><span class="sxs-lookup"><span data-stu-id="52a89-136">Specifying Client Information</span></span>](specifying-client-information.md)
</dt> <dt>

[<span data-ttu-id="52a89-137">Gravando Propriedades de objeto de conteúdo</span><span class="sxs-lookup"><span data-stu-id="52a89-137">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




