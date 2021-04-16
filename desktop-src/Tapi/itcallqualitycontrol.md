---
description: A interface ITCallQualityControl expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para controle de qualidade de chamada.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interface ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754190"
---
# <a name="itcallqualitycontrol-interface"></a><span data-ttu-id="37552-103">Interface ITCallQualityControl</span><span class="sxs-lookup"><span data-stu-id="37552-103">ITCallQualityControl interface</span></span>

<span data-ttu-id="37552-104">\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="37552-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="37552-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="37552-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="37552-106">A interface **ITCallQualityControl** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para controle de qualidade de chamada.</span><span class="sxs-lookup"><span data-stu-id="37552-106">The **ITCallQualityControl** interface exposes methods that allow an application to get and set parameters for call quality control.</span></span>

<span data-ttu-id="37552-107">Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="37552-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="37552-108">Ele é exposto somente quando uma chamada usa esses provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="37552-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="37552-109">Membros</span><span class="sxs-lookup"><span data-stu-id="37552-109">Members</span></span>

<span data-ttu-id="37552-110">A interface **ITCallQualityControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="37552-110">The **ITCallQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="37552-111">**ITCallQualityControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="37552-111">**ITCallQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="37552-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="37552-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="37552-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="37552-113">Methods</span></span>

<span data-ttu-id="37552-114">A interface **ITCallQualityControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="37552-114">The **ITCallQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="37552-115">Método</span><span class="sxs-lookup"><span data-stu-id="37552-115">Method</span></span>                                            | <span data-ttu-id="37552-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="37552-116">Description</span></span>                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37552-117">**Obter**</span><span class="sxs-lookup"><span data-stu-id="37552-117">**Get**</span></span>](itcallqualitycontrol-get.md)           | <span data-ttu-id="37552-118">Obtém o valor de uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="37552-118">Gets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="37552-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="37552-119">**GetRange**</span></span>](itcallqualitycontrol-getrange.md) | <span data-ttu-id="37552-120">Obtém o intervalo de valores válidos para uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="37552-120">Gets the range of valid values for a given [call quality control property](callqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="37552-121">**Definir**</span><span class="sxs-lookup"><span data-stu-id="37552-121">**Set**</span></span>](itcallqualitycontrol-set.md)           | <span data-ttu-id="37552-122">Define o valor de uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="37552-122">Sets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="37552-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37552-123">Requirements</span></span>



| <span data-ttu-id="37552-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="37552-124">Requirement</span></span> | <span data-ttu-id="37552-125">Valor</span><span class="sxs-lookup"><span data-stu-id="37552-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="37552-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="37552-126">TAPI version</span></span><br/> | <span data-ttu-id="37552-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="37552-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="37552-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37552-128">Header</span></span><br/>       | <dl> <span data-ttu-id="37552-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="37552-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="37552-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37552-130">Library</span></span><br/>      | <dl> <span data-ttu-id="37552-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37552-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="37552-132">DLL</span><span class="sxs-lookup"><span data-stu-id="37552-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="37552-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37552-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

