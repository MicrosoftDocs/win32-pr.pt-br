---
title: Método IWMDRMDevice GetSecureClock
description: O método GetSecureClock recupera o relógio seguro, portanto, as licenças baseadas em tempo podem ser impostas.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Método GetSecureClock Windows Media Gerenciador de Dispositivos
- Método GetSecureClock Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810599"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a><span data-ttu-id="48bdd-106">Método IWMDRMDevice:: GetSecureClock</span><span class="sxs-lookup"><span data-stu-id="48bdd-106">IWMDRMDevice::GetSecureClock method</span></span>

<span data-ttu-id="48bdd-107">O método **GetSecureClock** recupera o relógio seguro, portanto, as licenças baseadas em tempo podem ser impostas.</span><span class="sxs-lookup"><span data-stu-id="48bdd-107">The **GetSecureClock** method retrieves the secure clock, so time-based licenses can be enforced.</span></span>

## <a name="syntax"></a><span data-ttu-id="48bdd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48bdd-108">Syntax</span></span>


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="48bdd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48bdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48bdd-110">*ppbSecureClock* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="48bdd-110">*ppbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48bdd-111">Clock seguro recuperado.</span><span class="sxs-lookup"><span data-stu-id="48bdd-111">Retrieved secure clock.</span></span>

</dd> <dt>

<span data-ttu-id="48bdd-112">*pcbSecureClock* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="48bdd-112">*pcbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48bdd-113">Tamanho do relógio seguro, em bytes.</span><span class="sxs-lookup"><span data-stu-id="48bdd-113">Size of the secure clock, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="48bdd-114">*pdwFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="48bdd-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48bdd-115">Sinalizadores de status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48bdd-115">Device status flags.</span></span> <span data-ttu-id="48bdd-116">Esse valor deve ser um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="48bdd-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="48bdd-117">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="48bdd-117">Flag</span></span>                     | <span data-ttu-id="48bdd-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="48bdd-118">Description</span></span>                            |
|--------------------------|----------------------------------------|
| <span data-ttu-id="48bdd-119">\_ISWMDRM de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="48bdd-119">WMDRM\_DEVICE\_ISWMDRM</span></span>   | <span data-ttu-id="48bdd-120">O dispositivo dá suporte a DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="48bdd-120">The device supports Windows Media DRM.</span></span> |
| <span data-ttu-id="48bdd-121">\_NEEDCLOCK de dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="48bdd-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span> | <span data-ttu-id="48bdd-122">O dispositivo precisa de relógio.</span><span class="sxs-lookup"><span data-stu-id="48bdd-122">The device needs clock.</span></span>                |
| <span data-ttu-id="48bdd-123">\_dispositivo WMDRM \_ revogado</span><span class="sxs-lookup"><span data-stu-id="48bdd-123">WMDRM\_DEVICE\_REVOKED</span></span>   | <span data-ttu-id="48bdd-124">O dispositivo foi revogado.</span><span class="sxs-lookup"><span data-stu-id="48bdd-124">The device has been revoked.</span></span>           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48bdd-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48bdd-125">Return value</span></span>

<span data-ttu-id="48bdd-126">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="48bdd-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="48bdd-127">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="48bdd-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="48bdd-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="48bdd-128">Return code</span></span>                                                                          | <span data-ttu-id="48bdd-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="48bdd-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="48bdd-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48bdd-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="48bdd-131">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="48bdd-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48bdd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48bdd-132">Requirements</span></span>



| <span data-ttu-id="48bdd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="48bdd-133">Requirement</span></span> | <span data-ttu-id="48bdd-134">Valor</span><span class="sxs-lookup"><span data-stu-id="48bdd-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48bdd-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48bdd-135">Header</span></span><br/>  | <dl> <span data-ttu-id="48bdd-136"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48bdd-136"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="48bdd-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48bdd-137">Library</span></span><br/> | <dl> <span data-ttu-id="48bdd-138"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48bdd-138"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48bdd-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="48bdd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48bdd-140">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="48bdd-140">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[<span data-ttu-id="48bdd-141">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="48bdd-141">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> <dt>

[<span data-ttu-id="48bdd-142">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="48bdd-142">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





