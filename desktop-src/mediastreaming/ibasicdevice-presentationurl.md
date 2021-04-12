---
title: Método IBasicDevice PresentationUrl
description: Recupera a URL de apresentação do dispositivo.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- API de streaming de mídia do método PresentationUrl
- API de streaming de mídia do método PresentationUrl, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método PresentationUrl
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89d10187329692c4f279a94cde004455a182733e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364810"
---
# <a name="ibasicdevicepresentationurl-method"></a><span data-ttu-id="0f225-106">IBasicDevice: método resentationUrl de:P</span><span class="sxs-lookup"><span data-stu-id="0f225-106">IBasicDevice::PresentationUrl method</span></span>

<span data-ttu-id="0f225-107">Recupera a URL de apresentação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f225-107">Retrieves the device s presentation URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f225-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f225-108">Syntax</span></span>


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="0f225-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f225-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f225-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0f225-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f225-111">Recebe um ponteiro para a URL de apresentação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f225-111">Receives a pointer to the device s presentation URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f225-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f225-112">Return value</span></span>

<span data-ttu-id="0f225-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0f225-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0f225-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f225-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0f225-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0f225-115">Return code</span></span>                                                                          | <span data-ttu-id="0f225-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f225-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0f225-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f225-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0f225-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0f225-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0f225-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f225-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f225-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="0f225-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





