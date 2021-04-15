---
title: Método IWMDRMDevice SetSecureClockResponse
description: O método SetSecureClockResponse define a resposta de clock seguro.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Método SetSecureClockResponse Windows Media Gerenciador de Dispositivos
- Método SetSecureClockResponse Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método SetSecureClockResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760906"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a><span data-ttu-id="2d230-106">Método IWMDRMDevice:: SetSecureClockResponse</span><span class="sxs-lookup"><span data-stu-id="2d230-106">IWMDRMDevice::SetSecureClockResponse method</span></span>

<span data-ttu-id="2d230-107">O método **SetSecureClockResponse** define a resposta de clock seguro.</span><span class="sxs-lookup"><span data-stu-id="2d230-107">The **SetSecureClockResponse** method sets the secure clock response.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d230-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d230-108">Syntax</span></span>


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="2d230-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d230-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d230-110">*pbResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d230-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d230-111">A resposta do clock seguro a ser definida.</span><span class="sxs-lookup"><span data-stu-id="2d230-111">The secure clock response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="2d230-112">*cbResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d230-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d230-113">O tamanho especificado da resposta do clock seguro, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2d230-113">The specified size of the secure clock response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d230-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d230-114">Return value</span></span>

<span data-ttu-id="2d230-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2d230-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2d230-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d230-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2d230-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2d230-117">Return code</span></span>                                                                          | <span data-ttu-id="2d230-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d230-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2d230-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2d230-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2d230-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2d230-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d230-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d230-121">Requirements</span></span>



| <span data-ttu-id="2d230-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d230-122">Requirement</span></span> | <span data-ttu-id="2d230-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2d230-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d230-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d230-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2d230-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d230-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d230-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d230-126">Library</span></span><br/> | <dl> <span data-ttu-id="2d230-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d230-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d230-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d230-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d230-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="2d230-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="2d230-130">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="2d230-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





