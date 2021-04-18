---
description: O método Clear libera todos os itens da coleção.
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
title: 'Método IPortableDeviceValuesCollection:: Clear (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bf826b8e8a2035a0d84aec76979616fcccee9948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813423"
---
# <a name="iportabledevicevaluescollectionclear-method"></a><span data-ttu-id="29900-103">Método IPortableDeviceValuesCollection:: Clear</span><span class="sxs-lookup"><span data-stu-id="29900-103">IPortableDeviceValuesCollection::Clear method</span></span>

<span data-ttu-id="29900-104">O método **Clear** libera todos os itens da coleção.</span><span class="sxs-lookup"><span data-stu-id="29900-104">The **Clear** method releases all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="29900-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29900-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="29900-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29900-106">Parameters</span></span>

<span data-ttu-id="29900-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="29900-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29900-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29900-108">Return value</span></span>

<span data-ttu-id="29900-109">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="29900-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="29900-110">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="29900-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="29900-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="29900-111">Return code</span></span>                                                                          | <span data-ttu-id="29900-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="29900-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="29900-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="29900-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="29900-114">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="29900-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29900-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="29900-115">Remarks</span></span>

<span data-ttu-id="29900-116">O método libera toda a memória alocada para os itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="29900-116">The method releases all memory that is allocated for the items in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="29900-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29900-117">Requirements</span></span>



| <span data-ttu-id="29900-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="29900-118">Requirement</span></span> | <span data-ttu-id="29900-119">Valor</span><span class="sxs-lookup"><span data-stu-id="29900-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29900-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29900-120">Header</span></span><br/>  | <dl> <span data-ttu-id="29900-121"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="29900-121"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="29900-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29900-122">Library</span></span><br/> | <dl> <span data-ttu-id="29900-123"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29900-123"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29900-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="29900-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29900-125">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="29900-125">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




