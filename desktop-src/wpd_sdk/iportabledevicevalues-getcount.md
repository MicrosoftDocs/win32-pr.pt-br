---
description: O método GetCount recupera o número de itens na coleção.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'Método IPortableDeviceValues:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751333"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="3186a-103">Método IPortableDeviceValues:: GetCount</span><span class="sxs-lookup"><span data-stu-id="3186a-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="3186a-104">O método **GetCount** recupera o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="3186a-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3186a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3186a-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="3186a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3186a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3186a-107">*pcelt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3186a-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3186a-108">Ponteiro para um **DWORD** que contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="3186a-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3186a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3186a-109">Return value</span></span>

<span data-ttu-id="3186a-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3186a-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3186a-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3186a-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3186a-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3186a-112">Return code</span></span>                                                                          | <span data-ttu-id="3186a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3186a-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3186a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3186a-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3186a-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3186a-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3186a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3186a-116">Requirements</span></span>



| <span data-ttu-id="3186a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3186a-117">Requirement</span></span> | <span data-ttu-id="3186a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3186a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3186a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3186a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3186a-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3186a-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3186a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3186a-121">Library</span></span><br/> | <dl> <span data-ttu-id="3186a-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3186a-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3186a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3186a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3186a-124">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3186a-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




