---
description: O método set define o valor de uma determinada propriedade de configurações de áudio.
ms.assetid: 3132e004-5543-4b21-878d-35197f7077d6
title: 'Método ITAudioSettings:: Set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf947c28d3b5270b3c5dabd4196d0e6b71f57911
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754191"
---
# <a name="itaudiosettingsset-method"></a><span data-ttu-id="8618b-103">Método ITAudioSettings:: Set</span><span class="sxs-lookup"><span data-stu-id="8618b-103">ITAudioSettings::Set method</span></span>

<span data-ttu-id="8618b-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8618b-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8618b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8618b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8618b-106">O método **set** define o valor de uma determinada [**propriedade de configurações de áudio**](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8618b-106">The **Set** method sets the value of a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8618b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8618b-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="8618b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8618b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8618b-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8618b-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8618b-110">Membro da enumeração [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="8618b-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="8618b-111">*lvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8618b-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8618b-112">Valor desejado para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="8618b-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="8618b-113">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8618b-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8618b-114">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* deve ser controlado.</span><span class="sxs-lookup"><span data-stu-id="8618b-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8618b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8618b-115">Return value</span></span>

<span data-ttu-id="8618b-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8618b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="8618b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8618b-117">Return code</span></span>                                                                                   | <span data-ttu-id="8618b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8618b-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8618b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8618b-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8618b-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8618b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8618b-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8618b-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8618b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8618b-123">Requirements</span></span>



| <span data-ttu-id="8618b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8618b-124">Requirement</span></span> | <span data-ttu-id="8618b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8618b-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8618b-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8618b-126">TAPI version</span></span><br/> | <span data-ttu-id="8618b-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8618b-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="8618b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8618b-128">Header</span></span><br/>       | <dl> <span data-ttu-id="8618b-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8618b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8618b-130">Library</span></span><br/>      | <dl> <span data-ttu-id="8618b-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8618b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8618b-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="8618b-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8618b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8618b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8618b-135">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="8618b-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="8618b-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="8618b-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="8618b-137">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="8618b-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




