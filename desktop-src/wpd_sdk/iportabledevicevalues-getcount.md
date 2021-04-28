---
description: 'Método IPortableDeviceValues:: GetCount – o método GetCount recupera o número de itens na coleção.'
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
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086234"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="c7e5c-103">Método IPortableDeviceValues:: GetCount</span><span class="sxs-lookup"><span data-stu-id="c7e5c-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="c7e5c-104">O método **GetCount** recupera o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="c7e5c-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e5c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7e5c-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="c7e5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7e5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e5c-107">*pcelt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7e5c-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e5c-108">Ponteiro para um **DWORD** que contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="c7e5c-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e5c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c7e5c-109">Return value</span></span>

<span data-ttu-id="c7e5c-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c7e5c-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c7e5c-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7e5c-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c7e5c-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c7e5c-112">Return code</span></span>                                                                          | <span data-ttu-id="c7e5c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7e5c-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c7e5c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7e5c-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c7e5c-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c7e5c-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7e5c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7e5c-116">Requirements</span></span>



| <span data-ttu-id="c7e5c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e5c-117">Requirement</span></span> | <span data-ttu-id="c7e5c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c7e5c-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e5c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7e5c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c7e5c-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e5c-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7e5c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7e5c-121">Library</span></span><br/> | <dl> <span data-ttu-id="c7e5c-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7e5c-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e5c-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c7e5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e5c-124">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c7e5c-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




