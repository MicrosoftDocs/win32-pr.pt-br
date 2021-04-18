---
description: A interface ITAudioDeviceControl expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interface ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810140"
---
# <a name="itaudiodevicecontrol-interface"></a><span data-ttu-id="4fe99-103">Interface ITAudioDeviceControl</span><span class="sxs-lookup"><span data-stu-id="4fe99-103">ITAudioDeviceControl interface</span></span>

<span data-ttu-id="4fe99-104">\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4fe99-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4fe99-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4fe99-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4fe99-106">A interface **ITAudioDeviceControl** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="4fe99-106">The **ITAudioDeviceControl** interface exposes methods that enable an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="4fe99-107">Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="4fe99-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="4fe99-108">Ele é exposto quando uma chamada usa esses provedores de serviços ou um provedor de serviços de terceiros que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="4fe99-108">It is exposed when a call uses these service providers or a third party service provider that implements this interface.</span></span> <span data-ttu-id="4fe99-109">Para obter um ponteiro para a interface **ITAudioDeviceControl** , chame **QueryInterface** na interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) que controla o dispositivo de áudio correspondente ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="4fe99-109">To obtain a pointer to the **ITAudioDeviceControl** interface, call **QueryInterface** on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface that controls the audio device corresponding to the stream.</span></span> <span data-ttu-id="4fe99-110">O tipo de mídia da interface **ITStream** deve ser de áudio para que a interface **ITAudioDeviceControl** seja exposta.</span><span class="sxs-lookup"><span data-stu-id="4fe99-110">The media type of the **ITStream** interface must be audio for the **ITAudioDeviceControl** interface to be exposed.</span></span>

## <a name="members"></a><span data-ttu-id="4fe99-111">Membros</span><span class="sxs-lookup"><span data-stu-id="4fe99-111">Members</span></span>

<span data-ttu-id="4fe99-112">A interface **ITAudioDeviceControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4fe99-112">The **ITAudioDeviceControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4fe99-113">**ITAudioDeviceControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4fe99-113">**ITAudioDeviceControl** also has these types of members:</span></span>

-   [<span data-ttu-id="4fe99-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="4fe99-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4fe99-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="4fe99-115">Methods</span></span>

<span data-ttu-id="4fe99-116">A interface **ITAudioDeviceControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4fe99-116">The **ITAudioDeviceControl** interface has these methods.</span></span>



| <span data-ttu-id="4fe99-117">Método</span><span class="sxs-lookup"><span data-stu-id="4fe99-117">Method</span></span>                                              | <span data-ttu-id="4fe99-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4fe99-118">Description</span></span>                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fe99-119">**Obter**</span><span class="sxs-lookup"><span data-stu-id="4fe99-119">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="4fe99-120">Obtém o valor de uma determinada [propriedade de dispositivo de áudio](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4fe99-120">Gets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="4fe99-121">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="4fe99-121">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="4fe99-122">Obtém o intervalo de valores válidos para uma determinada [propriedade de dispositivo de áudio](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4fe99-122">Gets the range of valid values for a given [audio device property](audiodeviceproperty.md).</span></span><br/> |
| [<span data-ttu-id="4fe99-123">**Definir**</span><span class="sxs-lookup"><span data-stu-id="4fe99-123">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="4fe99-124">Define o valor de uma determinada [propriedade de dispositivo de áudio](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4fe99-124">Sets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="4fe99-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fe99-125">Requirements</span></span>



| <span data-ttu-id="4fe99-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fe99-126">Requirement</span></span> | <span data-ttu-id="4fe99-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4fe99-127">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe99-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4fe99-128">TAPI version</span></span><br/> | <span data-ttu-id="4fe99-129">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="4fe99-129">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="4fe99-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fe99-130">Header</span></span><br/>       | <dl> <span data-ttu-id="4fe99-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe99-131"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fe99-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fe99-132">Library</span></span><br/>      | <dl> <span data-ttu-id="4fe99-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fe99-133"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="4fe99-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4fe99-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="4fe99-135"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fe99-135"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe99-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fe99-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe99-137">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="4fe99-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

