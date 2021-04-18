---
description: A interface ITLocalParticipant é exposta no objeto Stream quando o IPConf MSP dá suporte à chamada.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interface ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788061"
---
# <a name="itlocalparticipant-interface"></a><span data-ttu-id="2cae9-103">Interface ITLocalParticipant</span><span class="sxs-lookup"><span data-stu-id="2cae9-103">ITLocalParticipant interface</span></span>

<span data-ttu-id="2cae9-104">A interface **ITLocalParticipant** é exposta no objeto Stream quando o IPConf MSP dá suporte à chamada.</span><span class="sxs-lookup"><span data-stu-id="2cae9-104">The **ITLocalParticipant** interface is exposed on the stream object when the IPConf MSP supports the call.</span></span> <span data-ttu-id="2cae9-105">O MSP implementa métodos que permitem que um aplicativo obtenha e defina informações do participante.</span><span class="sxs-lookup"><span data-stu-id="2cae9-105">The MSP implements methods that allow an application to get and set participant information.</span></span> <span data-ttu-id="2cae9-106">A interface **ITLocalParticipant** é criada chamando **QueryInterface** no [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="2cae9-106">The **ITLocalParticipant** interface is created by calling **QueryInterface** on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>

## <a name="members"></a><span data-ttu-id="2cae9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2cae9-107">Members</span></span>

<span data-ttu-id="2cae9-108">A interface **ITLocalParticipant** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2cae9-108">The **ITLocalParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2cae9-109">**ITLocalParticipant** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2cae9-109">**ITLocalParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="2cae9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2cae9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2cae9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2cae9-111">Methods</span></span>

<span data-ttu-id="2cae9-112">A interface **ITLocalParticipant** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2cae9-112">The **ITLocalParticipant** interface has these methods.</span></span>



| <span data-ttu-id="2cae9-113">Método</span><span class="sxs-lookup"><span data-stu-id="2cae9-113">Method</span></span>                                                                                     | <span data-ttu-id="2cae9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cae9-114">Description</span></span>                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cae9-115">**obter \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="2cae9-115">**get\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-get-localparticipanttypedinfo.md) | <span data-ttu-id="2cae9-116">Obtém informações do participante, como nome de email ou localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="2cae9-116">Gets participant information, such as e-mail name or geographical location.</span></span><br/> |
| [<span data-ttu-id="2cae9-117">**colocar \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="2cae9-117">**put\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-put-localparticipanttypedinfo.md) | <span data-ttu-id="2cae9-118">Define informações do participante.</span><span class="sxs-lookup"><span data-stu-id="2cae9-118">Sets participant information.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="2cae9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cae9-119">Requirements</span></span>



| <span data-ttu-id="2cae9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cae9-120">Requirement</span></span> | <span data-ttu-id="2cae9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2cae9-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cae9-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="2cae9-122">TAPI version</span></span><br/> | <span data-ttu-id="2cae9-123">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2cae9-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2cae9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2cae9-124">Header</span></span><br/>       | <dl> <span data-ttu-id="2cae9-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cae9-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="2cae9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cae9-126">Library</span></span><br/>      | <dl> <span data-ttu-id="2cae9-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cae9-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2cae9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2cae9-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="2cae9-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cae9-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2cae9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cae9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cae9-131">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="2cae9-131">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

