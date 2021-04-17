---
title: Método IWMDRMDevice GetSecureClockChallenge
description: O método GetSecureClockChallenge recupera o resultado de desafio seguro do relógio.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Método GetSecureClockChallenge Windows Media Gerenciador de Dispositivos
- Método GetSecureClockChallenge Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813205"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a><span data-ttu-id="fc834-106">Método IWMDRMDevice:: GetSecureClockChallenge</span><span class="sxs-lookup"><span data-stu-id="fc834-106">IWMDRMDevice::GetSecureClockChallenge method</span></span>

<span data-ttu-id="fc834-107">O método **GetSecureClockChallenge** recupera o resultado de desafio seguro do relógio.</span><span class="sxs-lookup"><span data-stu-id="fc834-107">The **GetSecureClockChallenge** method retrieves the secure clock challenge result.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc834-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc834-108">Syntax</span></span>


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="fc834-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc834-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc834-110">*ppbChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fc834-110">*ppbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc834-111">Resultado do desafio recuperado.</span><span class="sxs-lookup"><span data-stu-id="fc834-111">Retrieved challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="fc834-112">*pcbChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fc834-112">*pcbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc834-113">Tamanho do resultado do desafio, em bytes.</span><span class="sxs-lookup"><span data-stu-id="fc834-113">Size of the challenge result, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc834-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc834-114">Return value</span></span>

<span data-ttu-id="fc834-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fc834-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fc834-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc834-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fc834-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fc834-117">Return code</span></span>                                                                          | <span data-ttu-id="fc834-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc834-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fc834-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc834-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fc834-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fc834-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fc834-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc834-121">Requirements</span></span>



| <span data-ttu-id="fc834-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc834-122">Requirement</span></span> | <span data-ttu-id="fc834-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fc834-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc834-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc834-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fc834-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc834-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="fc834-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc834-126">Library</span></span><br/> | <dl> <span data-ttu-id="fc834-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc834-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc834-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc834-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc834-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="fc834-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="fc834-130">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="fc834-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





