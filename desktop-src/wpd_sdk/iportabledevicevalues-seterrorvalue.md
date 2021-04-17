---
description: O método seterrovalue adiciona um novo valor HRESULT (erro de tipo VT \_ ) ou substitui um existente.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'Método IPortableDeviceValues:: seterrovalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753839"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a><span data-ttu-id="61dda-103">Método IPortableDeviceValues:: SetError</span><span class="sxs-lookup"><span data-stu-id="61dda-103">IPortableDeviceValues::SetErrorValue method</span></span>

<span data-ttu-id="61dda-104">O método **Seterrovalue** adiciona um novo valor **HRESULT** (erro de tipo VT \_ ) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="61dda-104">The **SetErrorValue** method adds a new **HRESULT** value (type VT\_ERROR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="61dda-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61dda-105">Syntax</span></span>


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a><span data-ttu-id="61dda-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61dda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61dda-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61dda-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61dda-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="61dda-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="61dda-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="61dda-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61dda-110">Um **HRESULT** que contém o novo valor.</span><span class="sxs-lookup"><span data-stu-id="61dda-110">An **HRESULT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61dda-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61dda-111">Return value</span></span>

<span data-ttu-id="61dda-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="61dda-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="61dda-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61dda-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="61dda-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="61dda-114">Return code</span></span>                                                                          | <span data-ttu-id="61dda-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="61dda-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="61dda-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61dda-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="61dda-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="61dda-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61dda-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="61dda-118">Remarks</span></span>

<span data-ttu-id="61dda-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="61dda-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="61dda-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61dda-120">Requirements</span></span>



| <span data-ttu-id="61dda-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61dda-121">Requirement</span></span> | <span data-ttu-id="61dda-122">Valor</span><span class="sxs-lookup"><span data-stu-id="61dda-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61dda-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61dda-123">Header</span></span><br/>  | <dl> <span data-ttu-id="61dda-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="61dda-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="61dda-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61dda-125">Library</span></span><br/> | <dl> <span data-ttu-id="61dda-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61dda-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61dda-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="61dda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61dda-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="61dda-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="61dda-129">**IPortableDeviceValues:: geterrovalue**</span><span class="sxs-lookup"><span data-stu-id="61dda-129">**IPortableDeviceValues::GetErrorValue**</span></span>](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




