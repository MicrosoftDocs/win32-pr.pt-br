---
description: O ITStreamQualityControl expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de qualidade de fluxo.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interface ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789857"
---
# <a name="itstreamqualitycontrol-interface"></a><span data-ttu-id="08f2f-103">Interface ITStreamQualityControl</span><span class="sxs-lookup"><span data-stu-id="08f2f-103">ITStreamQualityControl interface</span></span>

<span data-ttu-id="08f2f-104">\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08f2f-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="08f2f-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="08f2f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="08f2f-106">O **ITStreamQualityControl** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de qualidade de fluxo.</span><span class="sxs-lookup"><span data-stu-id="08f2f-106">The **ITStreamQualityControl** exposes methods that allow an application to get and set parameters for stream quality control.</span></span>

<span data-ttu-id="08f2f-107">Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="08f2f-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="08f2f-108">Ele é exposto somente quando uma chamada usa esses provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="08f2f-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="08f2f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="08f2f-109">Members</span></span>

<span data-ttu-id="08f2f-110">A interface **ITStreamQualityControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="08f2f-110">The **ITStreamQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="08f2f-111">**ITStreamQualityControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08f2f-111">**ITStreamQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="08f2f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="08f2f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="08f2f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="08f2f-113">Methods</span></span>

<span data-ttu-id="08f2f-114">A interface **ITStreamQualityControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="08f2f-114">The **ITStreamQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="08f2f-115">Método</span><span class="sxs-lookup"><span data-stu-id="08f2f-115">Method</span></span>                                              | <span data-ttu-id="08f2f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="08f2f-116">Description</span></span>                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08f2f-117">**Obter**</span><span class="sxs-lookup"><span data-stu-id="08f2f-117">**Get**</span></span>](itstreamqualitycontrol-get.md)           | <span data-ttu-id="08f2f-118">Obtém o valor de uma determinada [propriedade de qualidade de fluxo](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="08f2f-118">Gets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="08f2f-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="08f2f-119">**GetRange**</span></span>](itstreamqualitycontrol-getrange.md) | <span data-ttu-id="08f2f-120">Obtém o intervalo de valores válidos para uma determinada [propriedade de qualidade de fluxo](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="08f2f-120">Gets the range of valid values for a given [stream quality property](streamqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="08f2f-121">**Definir**</span><span class="sxs-lookup"><span data-stu-id="08f2f-121">**Set**</span></span>](itstreamqualitycontrol-set.md)           | <span data-ttu-id="08f2f-122">Define o valor de uma determinada [propriedade de qualidade de fluxo](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="08f2f-122">Sets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="08f2f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f2f-123">Requirements</span></span>



| <span data-ttu-id="08f2f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08f2f-124">Requirement</span></span> | <span data-ttu-id="08f2f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="08f2f-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08f2f-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="08f2f-126">TAPI version</span></span><br/> | <span data-ttu-id="08f2f-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="08f2f-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="08f2f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08f2f-128">Header</span></span><br/>       | <dl> <span data-ttu-id="08f2f-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08f2f-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="08f2f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08f2f-130">Library</span></span><br/>      | <dl> <span data-ttu-id="08f2f-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08f2f-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="08f2f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="08f2f-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="08f2f-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08f2f-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

