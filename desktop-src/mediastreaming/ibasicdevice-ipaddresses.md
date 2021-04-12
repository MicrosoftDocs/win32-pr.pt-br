---
title: Método IpAddresses IBasicDevice
description: Retorna um vetor de endereços IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- API de streaming de mídia do método IpAddresses
- API de streaming de mídia do método IpAddresses, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364822"
---
# <a name="ibasicdeviceipaddresses-method"></a><span data-ttu-id="f821a-106">Método IBasicDevice:: IpAddresses</span><span class="sxs-lookup"><span data-stu-id="f821a-106">IBasicDevice::IpAddresses method</span></span>

<span data-ttu-id="f821a-107">Retorna um vetor de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="f821a-107">Returns a vector of IP addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="f821a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f821a-108">Syntax</span></span>


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="f821a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f821a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f821a-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f821a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f821a-111">Recebe uma coleção enumerável de ponteiros para endereços IP.</span><span class="sxs-lookup"><span data-stu-id="f821a-111">Receives an enumerable collection of pointers to IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f821a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f821a-112">Return value</span></span>

<span data-ttu-id="f821a-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f821a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f821a-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f821a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f821a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f821a-115">Return code</span></span>                                                                          | <span data-ttu-id="f821a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f821a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f821a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f821a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f821a-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f821a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f821a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f821a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f821a-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="f821a-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





