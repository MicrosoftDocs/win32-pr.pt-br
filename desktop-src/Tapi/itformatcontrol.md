---
description: A interface ITFormatControl expõe métodos que permitem que um aplicativo recupere informações relacionadas ao formato de um fluxo de recebimento ou de transmissão para uma chamada.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interface ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767755"
---
# <a name="itformatcontrol-interface"></a><span data-ttu-id="4ef62-103">Interface ITFormatControl</span><span class="sxs-lookup"><span data-stu-id="4ef62-103">ITFormatControl interface</span></span>

<span data-ttu-id="4ef62-104">\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4ef62-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4ef62-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4ef62-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4ef62-106">A interface **ITFormatControl** expõe métodos que permitem que um aplicativo recupere informações relacionadas ao formato de um fluxo de recebimento ou de transmissão para uma chamada.</span><span class="sxs-lookup"><span data-stu-id="4ef62-106">The **ITFormatControl** interface exposes methods that allow an application to retrieve information concerning the format of a receive or transmit stream for a call.</span></span>

<span data-ttu-id="4ef62-107">Essa interface é implementada pelo seu [H323 MSP](h323-msp.md) e é exposta somente quando uma chamada usa esse provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="4ef62-107">This interface is implemented by the [H323 MSP](h323-msp.md) and is exposed only when a call uses this service provider.</span></span>

## <a name="members"></a><span data-ttu-id="4ef62-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4ef62-108">Members</span></span>

<span data-ttu-id="4ef62-109">A interface **ITFormatControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4ef62-109">The **ITFormatControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4ef62-110">**ITFormatControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4ef62-110">**ITFormatControl** also has these types of members:</span></span>

-   [<span data-ttu-id="4ef62-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4ef62-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4ef62-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4ef62-112">Methods</span></span>

<span data-ttu-id="4ef62-113">A interface **ITFormatControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4ef62-113">The **ITFormatControl** interface has these methods.</span></span>



| <span data-ttu-id="4ef62-114">Método</span><span class="sxs-lookup"><span data-stu-id="4ef62-114">Method</span></span>                                                                     | <span data-ttu-id="4ef62-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ef62-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="4ef62-116">**GetCurrentFormat**</span><span class="sxs-lookup"><span data-stu-id="4ef62-116">**GetCurrentFormat**</span></span>](itformatcontrol-getcurrentformat.md)               | <span data-ttu-id="4ef62-117">Obtém o formato de mídia do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="4ef62-117">Gets the media format of the current stream.</span></span><br/>                        |
| [<span data-ttu-id="4ef62-118">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4ef62-118">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md) | <span data-ttu-id="4ef62-119">Obtém o número de recursos associados ao formato atual.</span><span class="sxs-lookup"><span data-stu-id="4ef62-119">Gets the number of capabilities associated with the current format.</span></span><br/> |
| [<span data-ttu-id="4ef62-120">**GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="4ef62-120">**GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)                     | <span data-ttu-id="4ef62-121">Obtém os recursos associados a um determinado índice de formato.</span><span class="sxs-lookup"><span data-stu-id="4ef62-121">Gets the capabilities associated with a given format index.</span></span><br/>         |
| [<span data-ttu-id="4ef62-122">**ReleaseFormat**</span><span class="sxs-lookup"><span data-stu-id="4ef62-122">**ReleaseFormat**</span></span>](itformatcontrol-releaseformat.md)                     | <span data-ttu-id="4ef62-123">Libera a estrutura associada ao formato.</span><span class="sxs-lookup"><span data-stu-id="4ef62-123">Releases the structure associated with the format.</span></span><br/>                  |
| [<span data-ttu-id="4ef62-124">**ReOrderCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4ef62-124">**ReOrderCapabilities**</span></span>](itformatcontrol-reordercapabilities.md)         | <span data-ttu-id="4ef62-125">Define um novo pedido para recursos de formato.</span><span class="sxs-lookup"><span data-stu-id="4ef62-125">Sets a new order for format capabilities.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="4ef62-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ef62-126">Requirements</span></span>



| <span data-ttu-id="4ef62-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ef62-127">Requirement</span></span> | <span data-ttu-id="4ef62-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4ef62-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef62-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4ef62-129">TAPI version</span></span><br/> | <span data-ttu-id="4ef62-130">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="4ef62-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="4ef62-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ef62-131">Header</span></span><br/>       | <dl> <span data-ttu-id="4ef62-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ef62-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ef62-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ef62-133">Library</span></span><br/>      | <dl> <span data-ttu-id="4ef62-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ef62-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="4ef62-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4ef62-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="4ef62-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ef62-136"><dt>Tapi3.dll</dt></span></span> </dl> |



 

