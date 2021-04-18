---
description: O método SetSignedIntegerValue adiciona um novo valor longo (tipo VT \_ i4) ou substitui um existente.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'Método IPortableDeviceValues:: SetSignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814123"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a><span data-ttu-id="f1975-103">Método IPortableDeviceValues:: SetSignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="f1975-103">IPortableDeviceValues::SetSignedIntegerValue method</span></span>

<span data-ttu-id="f1975-104">O método **SetSignedIntegerValue** adiciona um novo valor **longo** (tipo VT \_ i4) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="f1975-104">The **SetSignedIntegerValue** method adds a new **LONG** value (type VT\_I4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1975-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1975-105">Syntax</span></span>


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a><span data-ttu-id="f1975-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1975-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1975-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1975-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1975-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="f1975-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f1975-109">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f1975-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1975-110">Um **longo** que especifica o novo valor.</span><span class="sxs-lookup"><span data-stu-id="f1975-110">A **LONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1975-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1975-111">Return value</span></span>

<span data-ttu-id="f1975-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f1975-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f1975-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1975-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f1975-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f1975-114">Return code</span></span>                                                                          | <span data-ttu-id="f1975-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1975-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f1975-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1975-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f1975-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f1975-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1975-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1975-118">Remarks</span></span>

<span data-ttu-id="f1975-119">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="f1975-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1975-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1975-120">Requirements</span></span>



| <span data-ttu-id="f1975-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1975-121">Requirement</span></span> | <span data-ttu-id="f1975-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f1975-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1975-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1975-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f1975-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1975-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1975-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1975-125">Library</span></span><br/> | <dl> <span data-ttu-id="f1975-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1975-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1975-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1975-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1975-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f1975-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f1975-129">**IPortableDeviceValues::GetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="f1975-129">**IPortableDeviceValues::GetSignedIntegerValue**</span></span>](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




