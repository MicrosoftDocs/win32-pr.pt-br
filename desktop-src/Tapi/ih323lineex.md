---
description: A interface IH323LineEx é implementada pelo H323 MSP e está disponível somente em objetos de endereço H. 323. Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interface IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754739"
---
# <a name="ih323lineex-interface"></a><span data-ttu-id="301b5-104">Interface IH323LineEx</span><span class="sxs-lookup"><span data-stu-id="301b5-104">IH323LineEx interface</span></span>

<span data-ttu-id="301b5-105">\[O **IH323LineEx** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="301b5-105">\[**IH323LineEx** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="301b5-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="301b5-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="301b5-107">A interface **IH323LineEx** é implementada pelo [H323 MSP](h323-msp.md) e está disponível somente em objetos de endereço H. 323.</span><span class="sxs-lookup"><span data-stu-id="301b5-107">The **IH323LineEx** interface is implemented by the [H323 MSP](h323-msp.md) and is available only on H.323 address objects.</span></span> <span data-ttu-id="301b5-108">Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP.</span><span class="sxs-lookup"><span data-stu-id="301b5-108">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span>

> [!Note]  
> <span data-ttu-id="301b5-109">Todos os métodos nesta interface devem ser chamados somente após o registro para chamadas de entrada nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="301b5-109">All methods in this interface should be called only after registering for incoming calls on this address.</span></span>

 

## <a name="members"></a><span data-ttu-id="301b5-110">Membros</span><span class="sxs-lookup"><span data-stu-id="301b5-110">Members</span></span>

<span data-ttu-id="301b5-111">A interface **IH323LineEx** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="301b5-111">The **IH323LineEx** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="301b5-112">**IH323LineEx** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="301b5-112">**IH323LineEx** also has these types of members:</span></span>

-   [<span data-ttu-id="301b5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="301b5-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="301b5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="301b5-114">Methods</span></span>

<span data-ttu-id="301b5-115">A interface **IH323LineEx** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="301b5-115">The **IH323LineEx** interface has these methods.</span></span>



| <span data-ttu-id="301b5-116">Método</span><span class="sxs-lookup"><span data-stu-id="301b5-116">Method</span></span>                                                                                 | <span data-ttu-id="301b5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="301b5-117">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="301b5-118">**Setalias**</span><span class="sxs-lookup"><span data-stu-id="301b5-118">**SetAlias**</span></span>](ih323lineex-setalias.md)                                               | <span data-ttu-id="301b5-119">Configura um alias H. 323 padrão para o endereço.</span><span class="sxs-lookup"><span data-stu-id="301b5-119">Configures a default H.323 alias for the address.</span></span><br/>             |
| [<span data-ttu-id="301b5-120">**SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="301b5-120">**SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md) | <span data-ttu-id="301b5-121">Configura o peso de preferência para os recursos padrão.</span><span class="sxs-lookup"><span data-stu-id="301b5-121">Configures the preference weighting for default capabilities.</span></span><br/> |
| [<span data-ttu-id="301b5-122">**SetExternalT120Address**</span><span class="sxs-lookup"><span data-stu-id="301b5-122">**SetExternalT120Address**</span></span>](ih323lineex-setexternalt120address.md)                   | <span data-ttu-id="301b5-123">Configura um endereço T. 120 externo para troca de dados.</span><span class="sxs-lookup"><span data-stu-id="301b5-123">Configures an external T.120 address for data exchange.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="301b5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="301b5-124">Requirements</span></span>



| <span data-ttu-id="301b5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="301b5-125">Requirement</span></span> | <span data-ttu-id="301b5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="301b5-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="301b5-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="301b5-127">TAPI version</span></span><br/> | <span data-ttu-id="301b5-128">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="301b5-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="301b5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="301b5-129">Header</span></span><br/>       | <dl> <span data-ttu-id="301b5-130"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="301b5-130"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="301b5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="301b5-131">Library</span></span><br/>      | <dl> <span data-ttu-id="301b5-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="301b5-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="301b5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="301b5-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="301b5-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="301b5-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="301b5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="301b5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301b5-136">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="301b5-136">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

