---
description: O objeto TAPI é o objeto principal para a TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfaces de objeto TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759040"
---
# <a name="tapi-object-interfaces"></a><span data-ttu-id="23e72-103">Interfaces de objeto TAPI</span><span class="sxs-lookup"><span data-stu-id="23e72-103">TAPI Object Interfaces</span></span>

<span data-ttu-id="23e72-104">O [objeto TAPI](tapi-object.md) é o objeto principal para a TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="23e72-104">The [TAPI Object](tapi-object.md) is the main object for TAPI 3.</span></span>

<span data-ttu-id="23e72-105">A interface [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) não é exposta diretamente no objeto TAPI, mas está intimamente relacionada a ela e está listada aqui para conveniência de referência.</span><span class="sxs-lookup"><span data-stu-id="23e72-105">The [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) interface is not directly exposed on the TAPI Object, but is tightly related to it and is listed here for reference convenience.</span></span>



| <span data-ttu-id="23e72-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="23e72-106">Interfaces</span></span>                                                 | <span data-ttu-id="23e72-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="23e72-107">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23e72-108">**ITTAPI**</span><span class="sxs-lookup"><span data-stu-id="23e72-108">**ITTAPI**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | <span data-ttu-id="23e72-109">Interface primária da TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="23e72-109">Primary TAPI 3 interface.</span></span>                                                                                                                              |
| [<span data-ttu-id="23e72-110">**ITTAPI2**</span><span class="sxs-lookup"><span data-stu-id="23e72-110">**ITTAPI2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | <span data-ttu-id="23e72-111">Deriva de [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); fornece métodos adicionais que dão suporte a dispositivos telefônicos.</span><span class="sxs-lookup"><span data-stu-id="23e72-111">Derives from [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); provides additional methods that support phone devices.</span></span>                                                         |
| [<span data-ttu-id="23e72-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="23e72-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | <span data-ttu-id="23e72-113">Interface de saída usada para receber informações assíncronas sobre eventos TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="23e72-113">Outgoing interface used to receive asynchronous information about TAPI 3 events.</span></span>                                                                       |
| [<span data-ttu-id="23e72-114">**ITTAPICallCenter**</span><span class="sxs-lookup"><span data-stu-id="23e72-114">**ITTAPICallCenter**</span></span>](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | <span data-ttu-id="23e72-115">Fornece uma interface de entrada para controles de Call Center.</span><span class="sxs-lookup"><span data-stu-id="23e72-115">Provides an entry interface into call center controls.</span></span>                                                                                                 |
| [<span data-ttu-id="23e72-116">**ITTAPIObjectEvent**</span><span class="sxs-lookup"><span data-stu-id="23e72-116">**ITTAPIObjectEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | <span data-ttu-id="23e72-117">Fornece métodos para recuperar informações relacionadas a eventos de objeto TAPI.</span><span class="sxs-lookup"><span data-stu-id="23e72-117">Provides methods to retrieve information concerning TAPI object events.</span></span>                                                                                |
| [<span data-ttu-id="23e72-118">**ITTAPIObjectEvent2**</span><span class="sxs-lookup"><span data-stu-id="23e72-118">**ITTAPIObjectEvent2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | <span data-ttu-id="23e72-119">Estende [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); fornece um método para recuperar um ponteiro para o objeto de telefone que causou o evento de objeto TAPI.</span><span class="sxs-lookup"><span data-stu-id="23e72-119">Extends [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); provides a method to retrieve a pointer to the phone object that caused the TAPI object event.</span></span> |



 

 

 
