---
description: 'A interface IEnumMedia fornece métodos de enumeração de padrão COM para a interface ITMedia. O método ITMediaCollection:: get \_ EnumerationIf retorna um ponteiro para IEnumMedia.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interface IEnumMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759971"
---
# <a name="ienummedia-interface"></a><span data-ttu-id="a3727-104">Interface IEnumMedia</span><span class="sxs-lookup"><span data-stu-id="a3727-104">IEnumMedia interface</span></span>

<span data-ttu-id="a3727-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a3727-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a3727-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a3727-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a3727-107">A interface **IEnumMedia** fornece métodos de enumeração de padrão com para a interface [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="a3727-107">The **IEnumMedia** interface provides COM-standard enumeration methods for the [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="a3727-108">O método [**ITMediaCollection:: get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) retorna um ponteiro para **IEnumMedia**.</span><span class="sxs-lookup"><span data-stu-id="a3727-108">The [**ITMediaCollection::get\_EnumerationIf**](itmediacollection-get-enumerationif.md) method returns a pointer to **IEnumMedia**.</span></span>

## <a name="members"></a><span data-ttu-id="a3727-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a3727-109">Members</span></span>

<span data-ttu-id="a3727-110">A interface **IEnumMedia** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a3727-110">The **IEnumMedia** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a3727-111">**IEnumMedia** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a3727-111">**IEnumMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="a3727-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a3727-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a3727-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a3727-113">Methods</span></span>

<span data-ttu-id="a3727-114">A interface **IEnumMedia** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a3727-114">The **IEnumMedia** interface has these methods.</span></span>



| <span data-ttu-id="a3727-115">Método</span><span class="sxs-lookup"><span data-stu-id="a3727-115">Method</span></span>                            | <span data-ttu-id="a3727-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3727-116">Description</span></span>                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3727-117">**8i**</span><span class="sxs-lookup"><span data-stu-id="a3727-117">**Clone**</span></span>](ienummedia-clone.md) | <span data-ttu-id="a3727-118">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="a3727-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="a3727-119">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="a3727-119">**Next**</span></span>](ienummedia-next.md)   | <span data-ttu-id="a3727-120">Obtém o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="a3727-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="a3727-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a3727-121">**Reset**</span></span>](ienummedia-reset.md) | <span data-ttu-id="a3727-122">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="a3727-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="a3727-123">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="a3727-123">**Skip**</span></span>](ienummedia-skip.md)   | <span data-ttu-id="a3727-124">Ignora o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="a3727-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="a3727-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3727-125">Requirements</span></span>



| <span data-ttu-id="a3727-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3727-126">Requirement</span></span> | <span data-ttu-id="a3727-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a3727-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3727-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a3727-128">TAPI version</span></span><br/> | <span data-ttu-id="a3727-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a3727-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a3727-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3727-130">Header</span></span><br/>       | <dl> <span data-ttu-id="a3727-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3727-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3727-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3727-132">Library</span></span><br/>      | <dl> <span data-ttu-id="a3727-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3727-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a3727-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a3727-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="a3727-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3727-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

