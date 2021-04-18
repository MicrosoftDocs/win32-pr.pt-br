---
description: A interface ITAudioSettings expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interface ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784093"
---
# <a name="itaudiosettings-interface"></a><span data-ttu-id="d9719-103">Interface ITAudioSettings</span><span class="sxs-lookup"><span data-stu-id="d9719-103">ITAudioSettings interface</span></span>

<span data-ttu-id="d9719-104">\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d9719-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d9719-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="d9719-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d9719-106">A interface **ITAudioSettings** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="d9719-106">The **ITAudioSettings** interface exposes methods that allow an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="d9719-107">Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="d9719-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="d9719-108">Ele é exposto somente quando uma chamada usa esses provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="d9719-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="d9719-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d9719-109">Members</span></span>

<span data-ttu-id="d9719-110">A interface **ITAudioSettings** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d9719-110">The **ITAudioSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d9719-111">**ITAudioSettings** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d9719-111">**ITAudioSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="d9719-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9719-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d9719-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9719-113">Methods</span></span>

<span data-ttu-id="d9719-114">A interface **ITAudioSettings** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d9719-114">The **ITAudioSettings** interface has these methods.</span></span>



| <span data-ttu-id="d9719-115">Método</span><span class="sxs-lookup"><span data-stu-id="d9719-115">Method</span></span>                                              | <span data-ttu-id="d9719-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9719-116">Description</span></span>                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9719-117">**Obter**</span><span class="sxs-lookup"><span data-stu-id="d9719-117">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="d9719-118">Obtém o valor de uma determinada [propriedade de configuração de áudio](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d9719-118">Gets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="d9719-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="d9719-119">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="d9719-120">Obtém o intervalo de valores válidos para uma determinada [propriedade de configuração de áudio](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d9719-120">Gets the range of valid values for a given [audio setting property](audiosettingsproperty.md).</span></span><br/> |
| [<span data-ttu-id="d9719-121">**Definir**</span><span class="sxs-lookup"><span data-stu-id="d9719-121">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="d9719-122">Define o valor de uma determinada [propriedade de configuração de áudio](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d9719-122">Sets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d9719-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9719-123">Requirements</span></span>



| <span data-ttu-id="d9719-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9719-124">Requirement</span></span> | <span data-ttu-id="d9719-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d9719-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9719-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="d9719-126">TAPI version</span></span><br/> | <span data-ttu-id="d9719-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="d9719-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="d9719-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9719-128">Header</span></span><br/>       | <dl> <span data-ttu-id="d9719-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9719-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9719-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9719-130">Library</span></span><br/>      | <dl> <span data-ttu-id="d9719-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9719-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="d9719-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d9719-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="d9719-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9719-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

