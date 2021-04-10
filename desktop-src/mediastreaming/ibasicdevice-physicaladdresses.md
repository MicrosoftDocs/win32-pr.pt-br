---
title: Método IBasicDevice PhysicalAddresses
description: Retorna um vetor de endereços físicos.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- API de streaming de mídia do método PhysicalAddresses
- API de streaming de mídia do método PhysicalAddresses, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método PhysicalAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293162"
---
# <a name="ibasicdevicephysicaladdresses-method"></a><span data-ttu-id="0ee37-106">IBasicDevice: método hysicalAddresses de:P</span><span class="sxs-lookup"><span data-stu-id="0ee37-106">IBasicDevice::PhysicalAddresses method</span></span>

<span data-ttu-id="0ee37-107">Retorna um vetor de endereços físicos.</span><span class="sxs-lookup"><span data-stu-id="0ee37-107">Returns a vector of physical addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee37-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ee37-108">Syntax</span></span>


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="0ee37-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ee37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee37-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0ee37-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee37-111">Recebe uma coleção enumerável de ponteiros para endereços físicos.</span><span class="sxs-lookup"><span data-stu-id="0ee37-111">Receives an enumerable collection of pointers to physical addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee37-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ee37-112">Return value</span></span>

<span data-ttu-id="0ee37-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0ee37-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0ee37-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ee37-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0ee37-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0ee37-115">Return code</span></span>                                                                          | <span data-ttu-id="0ee37-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ee37-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0ee37-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ee37-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0ee37-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0ee37-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0ee37-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ee37-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee37-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="0ee37-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





