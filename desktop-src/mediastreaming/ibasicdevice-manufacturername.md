---
title: Método ManufacturerName do IBasicDevice
description: Recupera o nome do fabricante do dispositivo.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- API de streaming de mídia do método ManufacturerName
- API de streaming de mídia do método ManufacturerName, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ManufacturerName
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105797492"
---
# <a name="ibasicdevicemanufacturername-method"></a><span data-ttu-id="a9fcf-106">Método IBasicDevice:: ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="a9fcf-106">IBasicDevice::ManufacturerName method</span></span>

<span data-ttu-id="a9fcf-107">Recupera o nome do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9fcf-107">Retrieves the device s manufacturer name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fcf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9fcf-108">Syntax</span></span>


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="a9fcf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9fcf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9fcf-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a9fcf-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fcf-111">Recebe um ponteiro para o nome do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9fcf-111">Receives a pointer to the device s manufacturer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9fcf-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9fcf-112">Return value</span></span>

<span data-ttu-id="a9fcf-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a9fcf-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a9fcf-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9fcf-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a9fcf-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a9fcf-115">Return code</span></span>                                                                          | <span data-ttu-id="a9fcf-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9fcf-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a9fcf-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9fcf-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9fcf-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a9fcf-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a9fcf-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9fcf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fcf-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="a9fcf-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





