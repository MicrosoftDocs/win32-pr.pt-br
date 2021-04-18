---
description: O objeto de telefone é a entidade que representa o dispositivo de telefone real e todos os seus controles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Interfaces de objeto de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788047"
---
# <a name="phone-object-interfaces"></a><span data-ttu-id="9c4c7-103">Interfaces de objeto de telefone</span><span class="sxs-lookup"><span data-stu-id="9c4c7-103">Phone Object Interfaces</span></span>

<span data-ttu-id="9c4c7-104">O objeto de telefone é a entidade que representa o dispositivo de telefone real e todos os seus controles.</span><span class="sxs-lookup"><span data-stu-id="9c4c7-104">The Phone object is the entity that represents the actual phone device and all of its controls.</span></span>

<span data-ttu-id="9c4c7-105">As interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) não são diretamente expostas no objeto de telefone, mas estão estreitamente relacionadas a ela e estão listadas aqui para sua conveniência de referência.</span><span class="sxs-lookup"><span data-stu-id="9c4c7-105">The [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) and [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) interfaces are not directly exposed on the Phone object, but are tightly related to it and are listed here for convenience of reference.</span></span>



| <span data-ttu-id="9c4c7-106">Interface</span><span class="sxs-lookup"><span data-stu-id="9c4c7-106">Interface</span></span>                                                  | <span data-ttu-id="9c4c7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c4c7-107">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c4c7-108">**ITPhone**</span><span class="sxs-lookup"><span data-stu-id="9c4c7-108">**ITPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | <span data-ttu-id="9c4c7-109">Permite o acesso ao dispositivo de telefone em um nível comparável ao que está disponível com a TAPI 2. API *x* C.</span><span class="sxs-lookup"><span data-stu-id="9c4c7-109">Allows access to the phone device at a level comparable to that available with the TAPI 2.*x* C API.</span></span>                                      |
| [<span data-ttu-id="9c4c7-110">**ITAutomatedPhoneControl**</span><span class="sxs-lookup"><span data-stu-id="9c4c7-110">**ITAutomatedPhoneControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | <span data-ttu-id="9c4c7-111">Fornece métodos para o controle automatizado de toques e anéis de um telefone e para tratamento automatizado de chamadas com base no estado Hookswitch de um telefone.</span><span class="sxs-lookup"><span data-stu-id="9c4c7-111">Provides methods for automated control of a phone's tones and rings, and for automated call handling based on a phone's hookswitch state.</span></span> |
| [<span data-ttu-id="9c4c7-112">**ITPhoneEvent**</span><span class="sxs-lookup"><span data-stu-id="9c4c7-112">**ITPhoneEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | <span data-ttu-id="9c4c7-113">Recupera a descrição de eventos do telefone.</span><span class="sxs-lookup"><span data-stu-id="9c4c7-113">Retrieves the description of phone events.</span></span>                                                                                                |
| [<span data-ttu-id="9c4c7-114">**IEnumPhone**</span><span class="sxs-lookup"><span data-stu-id="9c4c7-114">**IEnumPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | <span data-ttu-id="9c4c7-115">Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span><span class="sxs-lookup"><span data-stu-id="9c4c7-115">Enumerates [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span></span>                                                                                                    |



 

 

 



