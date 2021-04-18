---
description: O método Get recupera o valor de uma determinada propriedade de configuração de áudio.
ms.assetid: 5ad9a4e8-c5b0-43e9-bf75-6460fd23501a
title: 'Método ITAudioSettings:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2773bf0f1a26978321ed0d02c3c30d8a96fef1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778404"
---
# <a name="itaudiosettingsget-method"></a><span data-ttu-id="499f7-103">Método ITAudioSettings:: Get</span><span class="sxs-lookup"><span data-stu-id="499f7-103">ITAudioSettings::Get method</span></span>

<span data-ttu-id="499f7-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="499f7-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="499f7-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="499f7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="499f7-106">O método **Get** recupera o valor de uma determinada [**propriedade de configuração de áudio**](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="499f7-106">The **Get** method retrieves the value of a given [**audio setting property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="499f7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="499f7-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="499f7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="499f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499f7-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="499f7-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499f7-110">Membro da enumeração [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="499f7-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="499f7-111">*plValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="499f7-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="499f7-112">Valor da *Propriedade* de entrada.</span><span class="sxs-lookup"><span data-stu-id="499f7-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="499f7-113">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="499f7-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="499f7-114">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="499f7-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499f7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="499f7-115">Return value</span></span>

<span data-ttu-id="499f7-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="499f7-116">This method can return one of these values.</span></span>



| <span data-ttu-id="499f7-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="499f7-117">Return code</span></span>                                                                                   | <span data-ttu-id="499f7-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="499f7-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="499f7-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="499f7-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="499f7-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="499f7-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="499f7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="499f7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="499f7-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="499f7-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="499f7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="499f7-123">Requirements</span></span>



| <span data-ttu-id="499f7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="499f7-124">Requirement</span></span> | <span data-ttu-id="499f7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="499f7-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="499f7-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="499f7-126">TAPI version</span></span><br/> | <span data-ttu-id="499f7-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="499f7-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="499f7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="499f7-128">Header</span></span><br/>       | <dl> <span data-ttu-id="499f7-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="499f7-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="499f7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="499f7-130">Library</span></span><br/>      | <dl> <span data-ttu-id="499f7-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="499f7-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="499f7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="499f7-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="499f7-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="499f7-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="499f7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="499f7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499f7-135">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="499f7-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="499f7-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="499f7-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="499f7-137">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="499f7-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




